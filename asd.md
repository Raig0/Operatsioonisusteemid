#!/bin/bash

IFS=$'\n'
protsess=$1

for i in $(ps -A); do
    if echo " "$i | tr -s ' ' | cut -d ' ' -f5 = $protsess
    then
        echo $i | cut -d ' ' -f5
        echo $i | cut -d ' ' -f2
    fi
done
