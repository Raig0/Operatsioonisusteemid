# Praktikum 5


Ül. 5-1
a) Kaustal /tmp/kaust peavad omanikul olema õigused: r-x (lugemiseks ja sisenemiseks)
Failil minufail.txt peavad omanikul olema õigused: r-- (lugemiseks)
b) Kataloogis /tmp/kaust oleva faili minufail.txt kustutamiseks:
Kaustal /tmp/kaust peavad omanikul olema õigused: rwx (lugemiseks, kirjutamiseks ja sisenemiseks)
Failil minufail.txt ei ole vaja õigusi kustutamiseks, kuna kustutamine sõltub ainult kausta õigustest.

Ül. 5-2
Käsk chmod a=x skriptifail annab ainult täitmisõiguse, kuid shelli skripti käivitamiseks on vaja ka lugemisõigust. Shell peab suutma skripti sisu lugeda, et käske täita. Ilma lugemisõiguseta ei saa skript töötada.
tuleks kasutada: chmod a=rx skriptifail

Ül. 5-3
Igal kasutajal on omanimeline grupp, et tagada turvalisus, lihtsustada õiguste haldamist ning toetada privaatsust ja koostööd. See loob efektiivse ja struktureeritud lähenemise kasutajaõiguste ja failihaldamisele.

Ül. 5-4
Kataloogis: Kataloogi puhul on vaja r-x õigusi, et pääseda failini ja kuvada selle sisu.
Failis: Failile peab olema antud r-- gruppi kuuluvatele kasutajatele, et nad saaksid sisu lugeda.
![image](https://github.com/user-attachments/assets/219419c5-4513-4b5c-83e0-0da0fd43a24d)
(peeter asemel on raigo1)

Ül. 5-5
Setuid-õigus võimaldab programmil töötada faili omaniku õigustes, mitte kasutaja õigustes, kes seda käivitab. Seda kasutatakse juhul, kui programm vajab kõrgendatud õigusi, näiteks failidele ligipääsuks, millele tavakasutajal muidu pole õigust.
![image](https://github.com/user-attachments/assets/fb95ad58-28b2-48d9-ae44-31080bad4812)

Ül. 5-6
Setuid-i kasutamine võib suurendada süsteemi turvariske, kui sellega antakse kasutajatele liigseid õigusi. Vigaste või ebaturvaliste setuid-programmide kaudu võivad ründajad saada süsteemi. Setuid-i tuleks kasutada ettevaatlikult ja ainult seal, kus see on hädavajalik.

Ül. 5-7
Peeter(faili looja), opetaja(kataloogi looja), root-kasutaja

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
