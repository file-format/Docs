{
  "date": "2020-11-11",
  "keywords": [
"NSF",
"laajennus",
"tiedosto",
"tiedosto muoto",
"Tietokannan tiedostotyyppi",
"Tietokannan tiedostomuoto",
"Tietokantatiedostot"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Opi NSF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata NSF-tiedostoja.",
  "title": "NSF-tiedostomuoto - Lotus Notes -tietokantamuoto",
  "linktitle": "NSF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ns-fif"
}
},
  "lastmod": "2020-08-12"
}

## Mikä on NSF-tiedosto?

Tiedosto, jonka laajennus on .nsf (Notes Storage Facility), on {{HYPERLINKKI}}:n käyttämä tietokantatiedostomuoto, joka tunnettiin aiemmin nimellä Lotus Notes. Se määrittelee skeeman erilaisten objektien, kuten sähköpostien, tapaamisten, asiakirjojen, lomakkeiden ja näkymien, tallentamiseksi. Kaikki nämä tiedot sisältyvät yhteen NSF-tiedostoon yritysyhteistyötä varten, joka on samanlainen kuin PST/OST-tiedosto. Joitakin sovelluksia, jotka voivat avata NSF-tiedostoja, ovat IBM Lotus Notes ja IBM Domino.

## NSF-tiedostomuodon tekniset tiedot

NSF-tiedostot ovat luonteeltaan binaarisia, ja niiden tekniset tiedot ovat saatavilla Joachim Metziltä osoitteesta [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc). Näiden tietojen mukaan NSF-tiedosto sisältää:

 * Tiedoston otsikko
 * Tietokannan otsikko

Lisäksi se koostuu:

 * Superblock
 * Kauhan kuvaajalohko
 * Bittikartta
 * Record Relocation Vector ämpäri
 * Yhteenveto kauhat
 * Muut kuin yhteenvetoryhmät


### NSF-tiedoston otsikko

NSF-tiedoston otsikko on kooltaan 6 tavua. Se koostuu:

|Offset|Koko|Arvo|Kuvaus|
---|---|---|---|
0|2|0x1a 0x00|Allekirjoitus|
2|4| |Tietokannan otsikon koko|

### Tietokannan otsikko

NSD-tietokannan otsikko sisältää seuraavat vahvistetut arvot.

 * Tietokannan tiedot
   * Tietokannan tunniste (DBID)
 * Replikointitiedot
 * Tietokannan tietopuskurin liput
   * Otsikko
   * Luokat
   * Luokka
   * Suunnitteluluokka (mallin nimi)
 * Erityiset huomautustunnisteet
 * Pehmuste
 * Tietokannan tiedot 2
 * Tietokannan tiedot 3
 * Tietokannan tiedot 4
 * Tietokannan tiedot 5
 * Pehmuste
 * Tietokannan ilmentymän tunniste (DBIID)
 * Replikointihistoria

## Viitteet

 * [NSF-muoto – Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

