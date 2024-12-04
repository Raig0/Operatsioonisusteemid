# Praktikum 12

Ülesanne 3)
```
#!/bin/sh
echo "Sisesta nimi:"
read nimi
echo "Sisesta eriala:"
read eriala
echo "Sisesta matriklinumber:"
read matriklinumber

echo "Nimi: $nimi, Eriala: $eriala, Matriklinumber: $matriklinumber."
```
<img width="245" alt="pilt1" src="https://github.com/user-attachments/assets/55ea00b4-9678-4c6f-bb3a-8ed19df7377b">

Ülesanne 4)
```
#!/bin/bash

laiend_A=$1
laiend_B=$2

for i in $(ls); do
    if [ ${i##*.} = $laiend_A ]; then
        uuendatud=${i%.*}.$laiend_B
        mv $i $uuendatud
    fi
done
```
<img width="277" alt="pilt" src="https://github.com/user-attachments/assets/d6f9b555-e3f4-43ca-900c-aec5a7d3a6d3">


Ülesanne 5)
```
#!/bin/bash

IFS=$'\n'
protsess=$1

for i in $(ps -A); do
    clean=$(echo " $i" | tr -s ' ')
    pid=$(echo $clean | cut -d ' ' -f2)
    pname=$(echo $clean | cut -d ' ' -f5)

    if [[ "$pname" == "$protsess" ]]; then
        echo "PID: $pid"
        echo "Protsess: $pname"
    fi
done
```
<img width="260" alt="pilt2" src="https://github.com/user-attachments/assets/3bda66f5-a106-418b-ba27-8ba4d1e6f2ea">

Ülesanne 6)
```
#!/bin/bash

astenda() {
    a=$1
    b=$2
    vastus=1

    for ((i=0; i<$b; i++)); do
        vastus=$((vastus * $a))
    done
    echo $vastus
}
echo $(astenda 9 5)
```
<img width="243" alt="pilt3" src="https://github.com/user-attachments/assets/12e1b39c-b012-4377-a018-3a31934d7209">

#### Ülesanne 7)
<img width="842" alt="pilt4" src="https://github.com/user-attachments/assets/0628c1d7-656b-4a91-8bb9-9402eed85349">
<img width="837" alt="pilt5" src="https://github.com/user-attachments/assets/fba18cd5-3e1b-4881-b5d9-e6616192e178">
<img width="841" alt="pilt6" src="https://github.com/user-attachments/assets/88b118fd-dbcf-43ac-9e66-2625b6f82155">
