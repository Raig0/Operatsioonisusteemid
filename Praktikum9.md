# Praktikum 9 <br>


|Küsimus|Linux|Windows|Linuxis kasutatud käsklus|Windowsis kasutatud tööriist|
|---|---|---|---|---|
|Mitu protsessi kokku arvutis käib? | 216 | 180 | ps -aux | wc -l
|Milline on kõige esimesena käivitatud protsess? | systemd | System | ps axo pid,cmd,comm,etime | Task manager
|Milliste kasutajate protsesse arvutis käib? | raigo, root, system-oom, systemd-resolve, systemd-timesync, messagebus, syslog, kernoops, rtkit, colord | Raigo | ps -eo user | Task manager
|Kui kaua on arvuti järjest töötanud? | 23min | 8h 33min | uptime | Task manager
|Milline protsess käivitati kõige hiljem? | ps | Discord.exe | ps -eo pid,etime,comm --sort=-etime | Process manager
|Milline on kõige rohkem protsessoriaega võttev protsess ja kui mitu protsenti protsessoriajast ta tarbib? | gnome-shell 12.5% | Discord.exe 8% | htop | Task Manager
|Milline on kõige rohkem virtuaalmälu võttev protsess? | gnome-shell | msedgewebview2.exe | ps -eo pid,vsz,comm --sort=-vsz | Process manager - virtual size
|Milline on kõige rohkem füüsilist mälu võttev protsess? | gnome-shell | msedge.exe | ps -eo pid,rss,comm --sort=-rss | Process manager 
|Kui palju füüsilisest mälust on vaba ja kui palju hõivatud? | 860Mi hõivatud, 1,8Gi vaba | 10300MB kasutusel, 6000mb vaba | free -h | Resource monitor
|Kui palju on põhikettal vaba ruumi mahult (GB) ja protsentuaalselt? | 11.1GB, 46% | 76GB, 16% | df -h | This PC - Devices and drives
|Milline on kõige suurem arvutis olev fail ja kõige rohkem andmemahtu hõivav kaust? | | Riot Games kaust, hiberfil.sys| | Windirstat
|millisele CPU alamtegevusele kulub enim protsessori aega kummagi käsu puhul? | 1) 98% ning 2) 96%  sy | | sha1sum /dev/zero sha1sum /dev/zero, sha1sum /dev/urandom sha1sum /dev/urandom |
|Milline protsess kõige rohkem salvestusseadmele kirjutab? | | System | | Resource monitor
|Millisesse faili eelmise küsimuse protsess kõige rohkem kirjutab? | | pagefile.sys | | Process monitor
|Milline protsess kõige rohkem salvestusseadmelt loeb? | | svchost.exe | | Resource monitor
|Millisest failist eelmise küsimuse protsess kõige rohkem loeb? | | C:\pagefile.sys | | Process monitor
|Millise protsessi poolt tekitatud võrguliiklus on suurima mahuga? | | 2001:bb8:2003:f:7435:6391:4472:cdd5 60890 2600:1901:1:38:: 443 | | Resource monitor
|Sõber kurdab, et tema arvuti on oluliselt aeglasemaks muutunud. Milliseid konkreetseid programme või käsureakäske kasutad põhjustaja tuvastamiseks | | Task Manager (Windows) Mida jälgida: Protsessori (CPU) kasutus, mälu (RAM) kasutus, ketta kasutus, võrgu kasutus. Resource monitor - Mida jälgida: Täpsemalt jälgida protsesside ja süsteemi ressursside kasutust. Samuti Virus and threat protection-is quick scan.  | | Task manager
<br>


#### 12. <br> 
![image](https://github.com/user-attachments/assets/b8612d14-8eb9-4d57-8b21-1e9f8376b959)



#### 14. <br>
