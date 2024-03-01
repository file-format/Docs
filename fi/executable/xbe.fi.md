{
  "date": "2021-08-31",
  "keywords": [
"xbe tiedosto",
"xbe tiedostomuoto",
"mikä on xbe-tiedosto",
"tiedosto",
"xbe esimerkki",
"xbe tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi XBE-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata XBE-tiedostoja.",
  "title": "XBE - iOS-sovelluspakettitiedosto",
  "linktitle": "XBE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-xb-fie"
}
},
  "lastmod": "2021-08-31"
}

## Mikä on XBE-tiedosto?
Tiedosto, jonka pääte on .xbe, on suoritettava sovellus Xbox-videopelilevyltä. XBE-tiedostot ovat tärkeimpiä Xbox-järjestelmässä suoritettavia tiedostoja, joita ei ole tarkoitus avata tavallisesti tietokoneella, mutta ne voidaan avata PC:llä Xbox-emulointiohjelmalla. Nämä tiedostot ovat yleensä pelien kehittäjien luomia ja Microsoftin allekirjoittamia. Tiedostorakenne on samanlainen kuin Windows PE-tiedostot, mutta joitain tärkeitä XBox-asetusten mukaisia muutoksia tehdään, jotta se voidaan suorittaa XBoxissa.

## XBE tiedostomuoto
XBE-tiedosto koostuu kuvan otsikosta, joukosta osiootsikoita, sertifikaattia, säiettä paikallista tallennustiedoista, kokoelmasta kirjastoversioita, Microsoftin bittikarttasta ja osioista, jotka sisältävät koodin ja resurssit.

### Kuvan otsikko
Kuvan otsikko sisältää tiedot, jotka selittävät missä muut suoritettavan tiedoston komponentit sijaitsevat tiedostossa ja kuinka ajettavaa tiedostoa tulee käsitellä ja ladata.

### TLS-taulukko
TLS-taulukko koostuu kaikista tiedoista, joita XBE tarvitsee säikeen paikallisen tallennustilan oikean määrittämiseen. Se on pohjimmiltaan ainutlaatuinen PE32-tiedostoista löytyvälle TLS-hakemistolle, ja se voidaan kopioida suoraan sieltä. Tämä taulukko voidaan jättää pois, jos XBE-tiedosto ei käytä säikeen paikallista tallennustilaa ja vastaava kenttä kuvan otsikossa on nolla.

| Offset | Koko | Nimi | Kuvaus |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Raakatietojen aloitus | Ohjelmakuvan TLS-muuttujan datan absoluuttinen (eli ei RVA) aloitusosoite. |
| 0x0004 | 0x0004 | Raw Data End | Ohjelmakuvan TLS-muuttujan datan lopun absoluuttinen (eli ei RVA) osoite. |
| 0x0008 | 0x0004 | Indeksin osoite | TLS-indeksimuuttujan absoluuttinen (eli ei RVA) osoite. |
| 0x000C | 0x0004 | Takaisinsoittojen osoite | Nollapäätetyn TLS-takaisinkutsun funktiotaulukon absoluuttinen (eli ei RVA) osoite. |
| 0x0010 | 0x0004 | Nollatäytön koko | Raakadataa seuraavien tavujen määrä, joka tulee asettaa nollaan muistissa. |
| 0x0014 | 0x0004 | Ominaisuudet | Kuvaa kohdistusta. |

### Todistus

 A a certificate is mandatory for each Xbox executable that contains information about the titles:
 
- Varmenteen luomisaika ja päivämäärä
- Otsikkotunnus
- Otsikon nimi
- Vaihtoehtoiset nimikkeiden tunnukset
- Sallitut mediatyypit, joista suoritettavaa tiedostoa voidaan ajaa (HD, DVD, CD jne.)
- Pelialue
- Pelien arvosanat
- Levyn numero
- Versio
- LAN-avaimen raakadata, jota käytetään System Linkissä
- Allekirjoitusavaimen raakadata (käytetään tallennuspelien allekirjoittamiseen)
- Vaihtoehtoiset allekirjoitusavaimet
- Todistuksen alkuperäinen koko
- Online-palvelun nimi (ei ole varhaisissa suoritettavissa tiedostoissa)
- Ajonaikaiset suojausliput (ei ole varhaisissa suoritettavissa tiedostoissa)
 
### Sallitut mediatyypit
Mediatyypit, joista suoritettava tiedosto sallii ajamisen. Seuraavat arvot tunnetaan:
| Mediatyyppi | Arvo |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Osat
Osat ilmaistaan osion otsikoilla. Osion otsikot alkavat heti varmenteen jälkeen ja sisältävät tiedot, missä tiedostossa varsinaiset osiot ovat. Xbox-suoritettavassa tiedostossa on aina vähintään kaksi osiota:
- .teksti
- .rdata


## Viitteet 

* [Xbe - XBox Executable](https://xboxdevwiki.net/Xbe)



