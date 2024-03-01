{
  "date": "2021-08-24",
  "keywords": [
"wdb-tiedosto",
"wdb-tiedostomuoto",
"mikä on wdb-tiedosto",
"tiedosto",
"wdb esimerkki",
"wdb tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi WDB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WDB-tiedostoja.",
  "title": "WDB - SQL Server Trace File",
  "linktitle": "WDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-wd-fib"
}
},
  "lastmod": "2021-08-24"
}

## Mikä on WDB-tiedosto?
Tiedosto, jonka pääte on .wdb, on itse asiassa Microsoft Worksin luoma tietokantatiedosto, jota käytettiin tietokannan hallintajärjestelmän kaltaisten toimintojen suorittamiseen. WDB-tiedosto on samanlainen kuin Access Database ([MDB](/database/mdb/)) -tiedosto, mutta se on vähemmän tehokas ja rajoituksetta suurempi. WDB-tiedostoja ei voi avata Microsoft Accessilla. Voit kuitenkin avata WDB-tiedoston Microsoft Worksissa ja viedä sen sitten MDB-tiedostoksi, jotta WDB-tiedosto voidaan avata MS Accessissa.

## WDB tiedostomuoto
Microsoft Works Database on Microsoft Works -toimistopaketin alkuperäinen tietokantamuoto. Formaatin patentoidun luonteen ja joidenkin rajoitusten vuoksi. WDB-tiedostoja ei voi avata millään muulla ohjelmistolla kuin Microsoft Worksilla. Tiedostomuodossa toistuva 10-tavuinen otsikko löytyy ennen jokaista ASCII-tekstijonoa, joka edustaa niiden kenttien arvoja, jotka päättyivät NULL-arvoon. Otsikko alkaa yleensä **\x0f**-tavulla ja NULL:lla, jota seuraa 4 datatavua vuorotellen NULL:illa.

### Tiedoston rakenne

WDB-tiedoston rakenne on annettu alla:
- **1. otsikko**: tiedoston alusta, joka päättyy \x25\x00\xf2 ja 244 NULL tavua
- **2. otsikko**: alkaa \xffT - eli \xff\x54 ja jatkuu 4096 tavua, joka sisältää sarakkeiden/kenttien nimet ja muita asioita ja näyttää alkavan tavun paikasta 6144.
- **Field**: value has a 10 byte header, with the following format: {type byte} {type byte, part 2} {data byte 1} \x00 {db 2} \x00 {db 3} {db 3, part 2} {db 4} \x00. datatavu 2 on kentän numero, datatavu 3 on tietueen numero (lisätään datatavu 3, osa 2, kun se ylittää 256 tietuetta).


## Viitteet ##

* [Käyttäjä:JesseW/wdb-muoto](https://en.wikipedia.org/wiki/User:JesseW/wdb_format)


