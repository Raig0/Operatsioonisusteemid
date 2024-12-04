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
