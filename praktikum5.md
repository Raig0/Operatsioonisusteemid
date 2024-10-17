# Praktikum 5
jojo tegin praktikumi

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
Igal kasutajal on omanimeline grupp, et tagada turvalisus, lihtsustada õiguste haldamist ning toetada privaatsust ja koostööd. See loob efektiivse ja struktureeritud lähenemise kasutajaõiguste ja failihaldamisele, mis on oluline igasugustes UNIX-põhistes süsteemides.

Ül. 5-4
Kataloogis: Kataloogi puhul on vaja r-x õigusi, et pääseda failini ja kuvada selle sisu.
Failis: Failile peab olema antud r-- gruppi kuuluvatele kasutajatele, et nad saaksid sisu lugeda.
