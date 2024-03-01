{
   "date":"2023-10-18",
   "keywords":[
"vihje",
"vihjetiedosto",
"cue cdrwin cue-arkkitiedosto",
"kuinka avata cue-tiedosto",
"tiedosto",
"cue tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CUE-tiedostomuoto - CDRWIN Cue Sheet",
   "description":"Opi CUE CDRWIN Cue Sheet -tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CUE-tiedostoja.",
   "linktitle":"CUE CDRWIN",
   "menu":{
      "docs":{
         "identifier":"disc-and-media-cue-cdrwin-fi",
         "parent":"disc-and-media"
}
},
   "lastmod":"2023-10-18"
}

## Mikä on CUE-tiedosto?

**.CUE**-tiedosto, joka tunnetaan myös nimellä **CDRWIN Cue Sheet**, on pelkkä tekstitiedosto, joka sisältää tietoja CD-äänilevyn tai levykuvan kappaleista ja asettelusta, tyypillisesti BIN- tai ISO-muodossa. Näitä tiedostoja käytetään usein kuvaamaan levyn rakennetta ja sisältöä, jolloin CD-polttoohjelmisto tai virtuaaliasemaohjelmisto voi toistaa alkuperäisen levyn tarkasti.

## Esimerkki CUE-tiedostosta

Tässä on esimerkki siitä, miltä .cue-tiedosto voi näyttää:

```
PERFORMER "Artist Name"
TITLE "Album Title"
FILE "DiscImage.bin" BINARY
  TRACK 01 AUDIO
    TITLE "Track 1 Title"
    PERFORMER "Artist Name"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "Track 2 Title"
    PERFORMER "Artist Name"
    INDEX 01 03:45:21
  TRACK 03 AUDIO
    TITLE "Track 3 Title"
    PERFORMER "Artist Name"
    INDEX 01 07:28:17
  TRACK 04 AUDIO
    TITLE "Track 4 Title"
    PERFORMER "Artist Name"
    INDEX 01 12:15:40
  (Additional tracks go here...)
```

## CDRWIN Cue Sheet

CDRWIN Cue Sheet on erityinen muunnelma .cue-tiedostomuodosta, jota CDRWIN-ohjelmisto käyttää. CDRWIN on CD/DVD-poltto- ja -luontiohjelmisto ja sen .cue-arkit on suunniteltu käytettäväksi tämän ohjelmiston kanssa. Nämä .cue-arkit sisältävät tietoja, joita CDRWIN tarvitsee CD- tai DVD-levyn tarkkaan luomiseen tai polttamiseen.

Tässä on joitain tärkeitä tietoja CDRWIN Cue Sheetsistä:

1.  **Ainutlaatuinen CDRWINille**: CDRWINin .cue-arkit ovat CDRWIN-ohjelmiston omaa muotoa. Vaikka niillä on yhtäläisyyksiä tavallisten .cue-tiedostojen kanssa, ne on räätälöity toimimaan CDRWINin ominaisuuksien ja asetusten kanssa.
    
2.  **Käyttäjäystävällinen käyttöliittymä**: CDRWIN tarjoaa helppokäyttöisen käyttöliittymän .cue-arkkien luomiseen ja muokkaamiseen. Käyttäjät voivat lisätä tai muokata tietoja kappaleista, indekseistä, aukoista ja muista parametreista käyttäjäystävällisellä tavalla.
    
3.  **Yhteensopivat levytyypit**: CDRWIN Cue Sheets -levyjä käytetään ensisijaisesti erityyppisten CD- ja DVD-levyjen luomiseen, mukaan lukien datalevyt, ääni-CD-levyt, sekamuotoiset levyt ja paljon muuta. Muoto sallii käyttäjien määrittää luotavan levyn tyypin ja sisällön.
    
4.  **Levyn asettelun hallinta**: CDRWIN Cue Sheets tarjoaa yksityiskohtaisen hallinnan levyn asettelusta ja rakenteesta, mukaan lukien raitajärjestys, tauko-/väliasetukset ja muut käyttäjän erityisasetukset.
    
5.  **ISO- ja BIN-tuki**: CDRWIN voi toimia sekä ISO- että BIN-levykuvamuotojen kanssa. .cue-arkki määrittää, mitä kuvatiedostoa käytetään levylle, mikä varmistaa oikean synkronoinnin vihjeiden ja kuvan välillä.
    
6.  **Poltto ja kopiointi**: Nämä .cue-arkit ovat tärkeitä poltettaessa levyjä tai kopioitaessa raitoja levyiltä CDRWIN-tekniikalla. Ne auttavat varmistamaan, että lopputuote vastaa suunniteltua asettelua ja sisältöä.
    
7.  **Varmuuskopiointi ja palautus**: CDRWIN-käyttäjät luovat usein .cue-arkkeja tehdessään varmuuskopioita CD- tai DVD-levyistään. Näitä arkkeja voidaan myöhemmin käyttää levyn sisällön palauttamiseen, mukaan lukien kappaleiden asettelu ja ajoitus.

## Kuinka avata CUE -tiedosto?

CDRWIN Cue Sheets on erityisesti suunniteltu CDRWIN-ohjelmistoa varten, joten ne on tyypillisesti tarkoitettu avattavaksi ja käytettäväksi CDRWINissä.

Ohjelmat, jotka avaavat CUE-tiedostoja tai viittaavat niihin

- CDRWIN
- Smart Projects IsoBuster
- EZB Systems UltraISO

## Muut CUE-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cue**-tiedostotunnistetta.

**Levy ja media**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

## Viitteet
* [CDRWIN](https://en.wikipedia.org/wiki/CDRWIN)


