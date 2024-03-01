{
  "date": "2021-03-08",
  "keywords": [
"PML",
"eReader",
"laajennus",
"muoto",
"eBook",
"Palm Markup Language"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi PML-tiedostomuodosta, Palm Markup Languagesta ja API-liittymistä, jotka voivat luoda ja avata PML-tiedostoja.",
  "title": "PML - Palm Markup Language File",
  "linktitle": "PML",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pm-fil"
}
},
  "lastmod": "2021-03-08"
}

## Mikä on PML-tiedosto?

Palm Inc esitteli PML-tiedostomuodon, joka tarkoittaa Palm Markup Language File -tiedostoa. Sen tarkoituksena on luoda asiakirjoja eReaderille, joka on tablettitietokoneen kaltainen e-kirjan lukulaite. PML-tiedosto antaa asettelun [PDB](/programming/pdb/)-tiedostolle (sisältää useita datatiedostoja) Palm-laitteella näytettäväksi.

## PML-tiedostojen tekniset tiedot

PML-tiedostojen rakenne koostuu tunnisteista eBook-asetusten luomista varten, mukaan lukien kappaleet, otsikot, sisennykset ja viittaukset. Se sallii myös muotoilutunnisteet, kuten lihavoitu, pienet kirjaimet ja yläindeksi. Kehittäjät voivat myös lisätä kuvia e-kirjoihin.

### Palm Markup Language
Seuraava taulukko määrittää PML-komennot:

|Komento|Kuvaus|
---|---|
| \p | Uusi sivu |
| \x | Uusi luku; aiheuttaa myös uuden sivunvaihdon. Liitä luvun otsikko (ja mahdolliset tyylikoodit) \x ja \x |
| \Xn | Uusi luku, sisennetty n tasoa (n välillä 0 ja 4 mukaan lukien) Luku-valintaikkunassa; ei aiheuta sivukatkoja. Liitä luvun otsikko (ja mahdolliset tyylikoodit) \Xn ja \Xn |
| \Cn=Luvun otsikko | Lisää luvun otsikko lukuluetteloon tasolla n (kuten \Xn). Tekstiä ei näytetä sivulla, eikä se pakota sivunvaihtoon. Tämä voi joskus olla hyödyllistä lisätä lukumerkki esimerkiksi luvun johdannon alkuun. |
| \c | Keskitä tämä tekstilohko; sulje \c rivin alussa |
| \r | Oikea tasaustekstilohko; sulje \r rivin alussa |
| \i | Kursivoi lohko; sulje \i |
| \u | Alleviivaa lohko; sulje \u |
| \o | Overstrike estää; sulje \o |
| \v | Näkymätön teksti; sulje kirjaimella \v (voidaan käyttää kommenteissa) |
| \t | Sisennyslohko. Aloita rivin alusta, lopeta kirjaimella \t rivin lopussa |
| \T=50% | Sisennä määritetyn prosenttiosuuden näytön leveydestä, tässä tapauksessa 50 %. Jos nykyinen piirustuspaikka on jo määritetyn näytön sijainnin ohi, tämä tunniste ohitetaan. |
| \w=50% | Upota vaakasuuntainen sääntö tietyn näytön leveyden prosentteina, tässä tapauksessa 50 %. Tämä tagi aiheuttaa rivinvaihdon ennen ja jälkeen sitä. Sääntö on keskitetty. Prosenttimerkki on pakollinen. |
| \n | Vaihda normaaliin fonttiin, jonka käyttäjä määrittää |
| \s | Vaihda stdFontiin; sulje \s palataksesi normaaliin fonttiin |
| \b | Vaihda boldFontiin; sulje \b palataksesi normaaliin fonttiin (vanhentunut; käytä \B sen sijaan) |
| \l | Vaihda suureen fonttiin; sulje \l palataksesi normaaliin fonttiin |
| \B | Merkitse teksti lihavoiduksi. Toisin kuin tagi \b, \B ei muuta fonttia, joten voit käyttää suurta lihavointia. Et voi sekoittaa \b ja \B samassa PML-tiedostossa. |
| \Sp | Merkitse teksti yläindeksiksi. Ei saa sekoittaa muihin tyyleihin, kuten lihavointiin, kursivointiin jne. Liitä yläindeksiin merkitty teksti \Sp. |
| \Sb | Merkitse teksti alaindeksiksi. Ei saa sekoittaa muihin tyyleihin, kuten lihavointiin, kursivointiin jne. Liitä alaviite tekstiin \Sb. |
| \k | Tee suljettu teksti pienikokoisiksi; sulje kirjaimella \k. Kaikki \k-tunnisteiden sisällä olevat merkit (mukaan lukien aksenttimerkit) muutetaan isoiksi ja hahmonnetaan pienemmällä pistekoolla kuin tavalliset isot kirjaimet. |
| \\ | Edustaa yhtä kenoviivaa |
| \aXXX | Lisää ei-ASCII-merkki, jonka Windows-1252-koodi on desimaali XXX. Katso lisätietoja PML-merkkitaulukosta. |
| \UXXXX | Lisää ei-ASCII-merkki, jonka Unicode-koodi on heksadesimaali XXXX. Katso lisätietoja laajennetusta PML-merkkitaulukosta. |
| \m=kuvanimi.png | Lisää nimetty kuva. Katso kuvat alla olevasta osiosta. |
| \q=#linkanchorJotkin tekstiä\q | Viittaa linkin ankkuriin, joka on asiakirjan toisessa kohdassa. Merkkijono ankkurimäärittelyn jälkeen ja ennen \q-merkkiä alleviivataan tai muuten näytetään linkkinä dokumenttia tarkasteltaessa. |
| \Q=linkanchor | Määritä asiakirjaan linkkiankkuri. |
| \- | Aseta pehmeä yhdysviiva. Pehmeä yhdysmerkki näkyy vain, jos on tarpeen katkaista sana rivin yli. |
| \Fn=alaviite11\Fn | Linkitä 1 alaviitteeseen, jonka nimi on alaviite1, joka on merkitty PML-asiakirjan loppuun. Katso alaviitteet ja sivupalkit alta. |
| \Sd=sivupalkki1Sivupalkki\Sd | Linkitä Sivupalkki-teksti sivupalkkiin, jonka nimi on sidebar1 ja joka on merkitty PML-dokumentin loppuun. Katso alaviitteet ja sivupalkit alta. |
| \I | Merkitse viiteindeksikohdaksi. Liitä hakemistokohde (ja mahdolliset tyylikoodit) \I- ja \I.|-merkkeihin
 

## Viitteet

* [Palm Markup Language – MobileRead](https://wiki.mobileread.com/wiki/EReader)

* [E-Reader - MobileRead](https://en.wikipedia.org/wiki/E-reader)


