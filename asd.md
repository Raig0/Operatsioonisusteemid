#!/bin/bash

laiend_A =$1
laiend_B =$2

for i in $(ls); do
    if [ ${i##*.} = $laiend_A ]; then
        uuendatud=${i%.*}.$laiend_B
        mv $i $uuendatud
    fi
done
