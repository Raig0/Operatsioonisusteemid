# Praktikum 5
Käesolevas praktikumis sain ülevaate Unixi failiõigustest. Lõin erinevaid kasutajaid ning andsin neile õiguseid.

Ül. 5-1
a) Kaustal r-x õigused. Failil r--
b) Kaustal rwx õigused. Faili kustutamiseks ei ole eraldi õiguseid vaja.

Ül. 5-2
Käsk chmod a=x skriptifail annab ainult käivitamisõiguse, kuid on vaja ka lugemisõigust.

Ül. 5-3
Igal kasutajal on omanimeline grupp, et tagada turvalisus, lihtsustada õiguste haldamist ning toetada privaatsust ja koostööd. See loob efektiivse ja struktureeritud lähenemise kasutajaõiguste ja failihaldamisele.

Ül. 5-4
On vaja r-x õiguseid.
![image](https://github.com/user-attachments/assets/219419c5-4513-4b5c-83e0-0da0fd43a24d)
(peeter asemel on raigo1)

Ül. 5-5
Setuid-õigus võimaldab programmil töötada faili omaniku õigustes, mitte kasutaja õigustes, kes seda käivitab. Seda kasutatakse juhul, kui programm vajab kõrgendatud õigusi, näiteks failidele ligipääsuks, millele tavakasutajal muidu pole õigust.
![image](https://github.com/user-attachments/assets/fb95ad58-28b2-48d9-ae44-31080bad4812)

Ül. 5-6
Setuid-i kasutamine võib suurendada süsteemi turvariske, kui sellega antakse kasutajatele liigseid õigusi. Vigaste või ebaturvaliste setuid-programmide kaudu võivad ründajad saada süsteemi. Setuid-i tuleks kasutada ettevaatlikult ja ainult seal, kus see on hädavajalik.

Ül. 5-7
raigo1, opetaja, root

Ül. 5-8
 file: hinded.txt
 owner: opetaja
 group: opetaja
user::rw-
group::rw-
group:direktor:rw-
mask::rw-
other::---

Ül. 5-9
Kui chattr +i on määratud, siis keegi ei saa faili muuta ega kustutada. 
Faili saab kustutada: (sudo chattr -i testfail-2) ning siis (rm testfail-2)
