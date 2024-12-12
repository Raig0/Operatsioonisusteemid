# Praktikum 13

Tegin tööd.

```
# Funktsioon tulemuste väljastamiseks
function valjasta {
    param ($nr, $param, $sisu)
    $fail = ".\tulemus.txt"
    $aeg = Get-Date -Format "yyyy-MM-dd HH:mm:ss.fff"
    if ($sisu -eq $null) {
        $rida = "$nr. [${aeg}] ${param}: NULL"
        Write-Output $rida
        $rida | Out-File -FilePath $fail -Append
    } elseif ($sisu.GetType().Name -eq "Object[]") {
        $rida = "$nr. [${aeg}] ${param}:"
        Write-Output $rida
        $sisu | ForEach-Object { Write-Output "    $_" }
        $rida | Out-File -FilePath $fail -Append
        $sisu | Out-File -FilePath $fail -Append
    } else {
        $rida = "$nr. [${aeg}] ${param}: ${sisu}"
        Write-Output $rida
        $rida | Out-File -FilePath $fail -Append
    }
}

# 1. Masina nimi ja süsteemi põhiinfo
$hostname = hostname
$psVersioon = $PSVersionTable.PSVersion.ToString()
$windowsVersioon = (Get-WmiObject -Class Win32_OperatingSystem).Caption
$systeemiinfo = "Hostname: ${hostname}; PowerShelli versioon: ${psVersioon}; Windowsi versioon: ${windowsVersioon}"
valjasta 1 "Süsteemiinfo" $systeemiinfo

# 2. Võrgu konfiguratsiooni info
$netConfig = Get-NetIPConfiguration
$ipAddress = $netConfig.IPv4Address.IPAddress
$subnetMask = $netConfig.IPv4Address.PrefixLength
$defaultGateway = $netConfig.IPv4DefaultGateway.NextHop
$dhcpStatus = if ($netConfig.Dhcp.Enabled) { "Jah" } else { "Ei" }
$macAddress = $netConfig.NetAdapter.MacAddress

$vorguInfo = "IP: $ipAddress, Mask: /$subnetMask, Gateway: $defaultGateway, DHCP: $dhcpStatus, MAC: $macAddress"

valjasta 2 "Võrgu konfiguratsioon" $vorguInfo

# 3. Protsessor ja RAM
$cpuDescription = (Get-WmiObject -Class Win32_Processor | Select-Object -Property Name).Name
$totalRAM = [math]::Round((Get-WmiObject Win32_PhysicalMemory | Measure-Object -Property Capacity -Sum | Select-Object -Property Sum).Sum / 1GB, 2)
$arvutiInfo = "Protsessor: ${cpuDescription}; RAM: ${totalRAM}GB"
valjasta 3 "Arvutiinfo" $arvutiInfo

# 4. Graafikakaardi info
$videoController = Get-WmiObject -Class Win32_VideoController | Select-Object Name, DriverVersion, VideoModeDescription
valjasta 4 "Graafikakaardi info" $videoController

# 5. Kettad ja partitsioonid
$disks = Get-Disk | ForEach-Object {
    $diskSize = [math]::Round($_.Size / 1GB, 2)
    "Ketas $($_.Number): ${diskSize} GB"
}
$cDriveFreeSpace = [math]::Round((Get-PSDrive C).Free / 1GB, 2)
valjasta 5 "Kettainfo" "$disks; C: kettal vaba: ${cDriveFreeSpace}GB"

# 6. PCI seadmed
$pciDevices = Get-WmiObject -Class Win32_PnpSignedDriver | Where-Object { $_.DeviceID -like "PCI*" } | Select-Object Description, Manufacturer, DriverVersion
valjasta 6 "PCI-seadmete info" $pciDevices

# 7. Kohalikud kasutajad
$localUsers = Get-LocalUser | Select-Object Name, Description, Enabled
valjasta 7 "Lokaalsed kasutajad" $localUsers

# 8. Protsessid ja nende arv
$runningProcessesCount = (Get-Process | Measure-Object).Count
valjasta 8 "Protsesside arv" $runningProcessesCount

# 9. Viimased 10 protsessi
$lastProcesses = Get-Process | Where-Object { $_.StartTime -ne $null } | Sort-Object StartTime -Descending | Select-Object -First 10 Name, Id, StartTime
valjasta 9 "Viimased 10 protsessi" $lastProcesses

# 10. Kuupäev ja kellaaeg
$currentDateTime = Get-Date -Format "dddd, dd MMMM yyyy HH:mm:ss"
valjasta 10 "Kuupäev ja kellaaeg" $currentDateTime
```

[tulemus.txt](https://github.com/user-attachments/files/18115406/tulemus.txt)
