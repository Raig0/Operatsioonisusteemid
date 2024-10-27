# Praktikum 6

Praktikumi esimeses osas ma lahendasin ülesanded protsesside ja signaalide teemal. Teises osas käisin läbi protsessi sisendi ja väljundi ülesanded.

Ül.1)
<img width="260" alt="pilt1" src="https://github.com/user-attachments/assets/5023c512-805a-4f41-b1b2-745f261cf471">

Ül.2)
<img width="365" alt="pilt2" src="https://github.com/user-attachments/assets/2c57a57a-cace-40b6-9003-04358345e8d8">

Ül.3) ps -axu | grep daemon | grep -v grep | tr -s ' ' | cut -d ' ' -f11-
<img width="602" alt="pilt3" src="https://github.com/user-attachments/assets/aaa56e50-3a82-443c-a722-611479450364">

Ül.4) ip a | grep 'inet ' | grep -v '127.0.0.1' | awk '{print $2}' | cut -d '/' -f1 

ip a | grep 'inet ' | grep -v '127.0.0.1' | awk '{print $2}' | cut -d '/' -f1 > ipaddress.txt

xargs -n1 ping -c 2 < ipaddress.txt

<img width="566" alt="pilt4" src="https://github.com/user-attachments/assets/7b82255d-c966-42a6-8f45-45d40a442679">
