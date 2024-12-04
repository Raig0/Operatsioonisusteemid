#!/bin/bash

IFS=$'\n'
protsess=$1

for i in $(ps -A); do
    i=$(echo " $i" | tr -s ' ')
    pid=$(echo $i | cut -d ' ' -f1)
    pname=$(echo $i | cut -d ' ' -f2-)

    if [ $pname = $protsess ]; then
        echo $pid
        echo $pname
    fi
done
