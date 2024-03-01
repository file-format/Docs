{
  "date": "2021-03-30",
  "keywords": [
"PMLZ",
"Zipped Palm Markup Language File",
"laajennus",
"Tiedosto",
"muoto",
"e-kirja",
"Palm Markup Language"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi PMLZ-tiedostomuodosta, Palm Markup Languagesta ja API:ista, jotka voivat luoda ja avata PMLZ-tiedostoja.",
  "title": "PMLZ - Zipped Palm Markup Language File",
  "linktitle": "PMLZ",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pml-fiz"
}
},
  "lastmod": "2021-03-30"
}

## Mikä on PMLZ-tiedosto?

Palm Inc esitteli eBook-tiedostotyypin; tunnetaan nimellä PMLZ-tiedostomuoto, joka on pakattu versio [PML](/ebook/pml/)-tiedostomuodosta, minkä vuoksi .pmlz-tunnisteiset tiedostot tunnetaan nimellä **Zipped Palm Markup Language File**. PMLZ-tiedosto on vain zip-säilö tiedostosta, joka kokoaa [PDB](/programming/pdb/)-tiedostoja asiakirjojen luomiseksi **eReaderille** (tunnetaan e-kirjojen lukulaitteena, kuten tablettitietokoneena). PML-tiedosto antaa asettelun PDB-tiedostolle (sisältää useita datatiedostoja) näytettäväksi Palm-laitteella. PDB-tiedosto on tietokantatiedosto, jota käyttävät useat sovellukset, kuten Quicken, Pegasus, Microsoft Visual Studio ja Palm Pilot. Lyhyesti sanottuna PMLZ on pakattu säiliö PML- ja PDB-tiedostoista.


## Palm Markup Language -kielen tuntemus
Seuraava taulukko määrittää PML-komennot:

|Komento|Kuvaus|
---|---|
| \p | Uusi sivu |
| \x | Uusi luku; aiheuttaa myös uuden sivunvaihdon. Liitä luvun otsikko (ja mahdolliset tyylikoodit) \x ja \x |
| \Xn | Uusi luku, sisennetty n tasoa (n välillä 0 ja 4 mukaan lukien) Luku-valintaikkunassa; ei aiheuta sivukatkoja. Liitä luvun otsikko (ja mahdolliset tyylikoodit) \Xn ja \Xn |
| \Cn=Luvun otsikko | Lisää luvun otsikko lukuluetteloon tasolla n (kuten \Xn). Tekstiä ei näytetä sivulla, eikä se pakota sivunvaihtoon. Tämä voi joskus olla hyödyllistä lisätä kappalemerkki esimerkiksi luvun johdannon alkuun. |
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
| \b | Vaihda boldFontiin; sulje \b palataksesi normaaliin fonttiin (vanhentunut; käytä sen sijaan kirjasinta \B) |
| \l | Vaihda suureen fonttiin; sulje \l palataksesi normaaliin fonttiin |
| \B | Merkitse teksti lihavoiduksi. Toisin kuin tagi \b, \B ei muuta fonttia, joten voit käyttää suurta lihavointia. Et voi sekoittaa \b ja \B samassa PML-tiedostossa. |
| \Sp | Merkitse teksti yläindeksiksi. Ei saa sekoittaa muihin tyyleihin, kuten lihavointiin, kursivointiin jne. Liitä yläindeksiin merkitty teksti \Sp. |
| \Sb | Merkitse teksti alaindeksiksi. Ei saa sekoittaa muihin tyyleihin, kuten lihavointiin, kursivointiin jne. Liitä alaviite tekstiin \Sb. |
| \k | Tee suljettu teksti pienikokoisiksi; sulje kirjaimella \k. Kaikki \k-tunnisteiden sisällä olevat merkit (mukaan lukien ne, joissa on aksenttimerkit) muutetaan isoiksi ja hahmonnetaan pienemmällä pistekoolla kuin tavalliset isot kirjaimet. |
| \\ | Edustaa yhtä kenoviivaa |
| \aXXX | Lisää ei-ASCII-merkki, jonka Windows-1252-koodi on desimaali XXX. Katso lisätietoja PML-merkkitaulukosta. |
| \UXXXX | Lisää ei-ASCII-merkki, jonka Unicode-koodi on heksadesimaali XXXX. Katso lisätietoja laajennetusta PML-merkkitaulukosta. |
| \m=kuvanimi.png | Lisää nimetty kuva. Katso kuvat alla olevasta osiosta. |
| \q=#linkanchorJotkin tekstiä\q | Viittaa linkkiankkuriin, joka on asiakirjan toisessa kohdassa. Merkkijono ankkurimäärittelyn jälkeen ja ennen \q-merkkiä alleviivataan tai muuten näytetään linkkinä dokumenttia katseltaessa. |
| \Q=linkanchor | Määritä asiakirjaan linkkiankkuri. |
| \- | Aseta pehmeä yhdysviiva. Pehmeä yhdysmerkki näkyy vain, jos on tarpeen katkaista sana rivin yli. |
| \Fn=alaviite11\Fn | Yhdistä 1 alaviitteeseen, jonka nimi on alaviite1, joka on merkitty PML-asiakirjan loppuun. Katso alaviitteet ja sivupalkit alta. |
| \Sd=sivupalkki1Sivupalkki\Sd | Linkitä Sivupalkki-teksti sivupalkkiin, jonka nimi on sidebar1 ja joka on merkitty PML-dokumentin loppuun. Katso alaviitteet ja sivupalkit alta. |
| \I | Merkitse viiteindeksikohdaksi. Liitä indeksikohde (ja mahdolliset tyylikoodit) \I- ja \I.|-merkkeihin


## Viitteet

* [Palm Markup Language – MobileRead](https://wiki.mobileread.com/wiki/EReader)

* [E-Reader - MobileRead](https://en.wikipedia.org/wiki/E-reader)


