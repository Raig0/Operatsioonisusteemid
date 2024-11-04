# Praktikum 7

Selles praktikumis õppisin ma haakimisest. Kõigepealt lahendasin ülesanded teemadel Windowsi kettahaldus ning Windowsi võrgukettad. Praktikumi lõpus lahendasin ülesande: ketta automaatne ühendamine arvuti käivitumisel.

1) Andmekandjad vajavad lähtestamist, et eemaldada vanad andmed, lahendada võimalikke tõrkeid ja luua uus failisüsteem, mis teeb need uuesti kasutuskõlblikuks.

2) i. Rohkem partitsioone: GPT toetab kuni 128 partitsiooni ilma loogilisi sektsioone vajamata, samas kui MBR piirab tavaliselt 4 primaarse partitsiooniga.
ii. Suurem ketta maht: GPT võimaldab hallata kettaid, mille maht on üle 2 TB, samas kui MBR toetab maksimaalselt 2 TB suuruseid kettaid.
iii. Usaldusväärsus ja andmete terviklikkus: GPT salvestab partitsioonitabeli mitmes kohas kettal ja sisaldab sisseehitatud veakontrolli, mis aitab andmeid paremini kaitsta ja vigu avastada.

3) https://kodu.ut.ee/~raigoleesment/opsys/hdd.png

4) <img width="295" alt="pilt1" src="https://github.com/user-attachments/assets/994e11d3-c031-42ad-a42d-2ae027f8a5c1">

5) Mida mõjutasid mount-käsu parameetrid -o ro ja -t auto? - Parameeter -o ro määrab, et seade haagitakse ainult lugemiseks (read-only), mistõttu ei saa andmeid muuta. Parameeter -t auto laseb operatsioonisüsteemil automaatselt tuvastada ja valida sobiva failisüsteemi tüübi, mida kasutada.

6) Leidke mount-käsu väljundist üles, mis väärtusega asendas Ubuntu auto-parameetri. - Asendati exfat-iga.

7) <img width="364" alt="pilt2" src="https://github.com/user-attachments/assets/e39676a4-05b5-413c-b3c7-bff3a11d01e9">
