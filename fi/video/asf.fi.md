{
  "date": "2021-02-15",
  "keywords": [
"asf tiedosto",
"asf-tiedostomuoto",
"mikä on asf-tiedosto",
"tiedosto",
"asf esimerkki",
"asf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ASF - Advanced Systems -tiedostomuoto",
  "description": "Opi ASF-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ASF-tiedostoja.",
  "linktitle": "ASF",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-as-fif"
}
},
  "lastmod": "2021-02-16"
}

## Mikä on ASF-tiedosto?

Tiedosto, jonka pääte on .asf, on multimediatiedostomuoto digitaalisten mediavirtojen tallentamiseen ja toistamiseen verkossa. Se on säilötiedostomuoto, jossa voi olla sekä video- että äänisisältöä suoratoistoa varten verkossa. Löydät harvoin ASF-tiedostoja, ja useammin törmäät Windows Media Audio ([WMA](/audio/wma/)) ja Windows Media Video ([WMV](/video/wmv/)) -tiedostoihin, jotka molemmat määrittelevät ASF-tiedostot, joiden sisältö on koodattu vastaavilla koodekeilla. Windows Media -tiedostoja voidaan luoda ja lukea käyttämällä Windows Media Format SDK:ta.

## ASF tiedostomuoto

ASF-tiedosto voi sisältää useita riippumattomia tai riippuvaisia virtoja. Tämä voi sisältää useita äänivirtoja monikanavaista ääntä tai useita bittinopeusvideovirtoja. Useat bittinopeudet tekevät virroista sopivia lähetettäväksi eri kaistanleveyksillä. Lisäksi ASF-tiedoston streamit voivat olla pakatussa tai pakkaamattomassa muodossa. Paras pakkaus saavutetaan Microsoft Windows Media Audio and Video 9 -sarjan koodekeilla. Täydelliset ASF-tiedostomuodon tiedot ovat saatavilla osoitteessa [Microsoft Website](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### ASF:n huipputason tiedostorakenne

ASF-tiedostot sisältävät loogisesti kolmen tyyppisiä huipputason objekteja:

* "Header Object" - pakollinen ja se on sijoitettava jokaisen ASF-tiedoston alkuun

* `Data Object` - pakollinen ja sen on seurattava otsikkoobjektia

* "Index Object(s)" - valinnainen, mutta hyödyllinen aikaan perustuvan satunnaisen pääsyn tarjoamiseen ASF-tiedostoihin


Seuraava kuva näyttää ASF-tiedostojen ylimmän tason tiedostorakenteen.

!{{HYPERLINKKI1}}

#### ASF:n ylätason otsikkoobjekti

Otsikko-objekti tarjoaa hyvin tunnetun tavusekvenssin ASF-tiedostojen alussa ja voi valinnaisesti sisältää metatietoja, kuten bibliografisia tietoja. Se sisältää kaikki tiedot, joita tarvitaan tietoobjektin tietojen tulkitsemiseen oikein. Otsikkoobjekti voi sisältää useita vakioobjekteja, mukaan lukien, mutta ei rajoittuen:

 * Tiedoston ominaisuudet -objekti - Sisältää yleiset tiedostoattribuutit.
 * Stream Properties Object - Määrittää digitaalisen mediavirran ja sen ominaisuudet.
 * Header Extension Object - Mahdollistaa lisätoimintojen lisäämisen ASF-tiedostoon säilyttäen samalla yhteensopivuuden taaksepäin.
 * Sisältö Kuvaus Objekti - Sisältää bibliografisia tietoja.
 * Script Command Object - Sisältää komennot, jotka voidaan suorittaa toiston aikajanalla.
 * Marker Object - Antaa nimetyt hyppypisteet tiedostossa.

Otsikkoobjekti esitetään seuraavalla rakenteella:

|Kentän nimi |Kentän tyyppi |Koko (bittiä)|
---|---|---|
|Objektin tunnus| GUID| 128|
|Objektin koko| QWORD| 64|
|Otsikkoobjektien määrä| DWORD| 32|
|Varattu1| BYTE| 8|
|Varattu2| BYTE| 8|

#### ASF:n huipputason tietoobjekti

Kaikki ASF-tiedoston digitaaliset mediatiedot sisältyvät tietoobjektiin ja tallennetaan ASF-datapakettien muodossa. Jokainen datapaketti on kiinteäpituinen ja sisältää dataa yhdelle tai useammalle digitaaliselle mediavirralle.

#### ASF:n huipputason indeksiobjektit

ASF-ylemmän tason hakemistoobjekteilla on seuraavat kaksi tyyppiä:

 * Simple Index Object - Sisältää aikaperusteisen indeksin ASF-tiedoston videotiedoista. Indeksimerkintöjen välinen aika on vakio, ja se tallennetaan yksinkertaiseen indeksiobjektiin.
 * Indeksiobjekti - Viittaa indeksiobjektiin, mediaobjektin indeksiobjektiin ja aikakoodiindeksiobjektiin, joiden muodot ovat samanlaiset. Kuten yksinkertainen indeksiobjekti, indeksiobjekti indeksoi ajan mukaan kiinteällä aikavälillä, mutta ei rajoitu videovirtoihin.

## Viitteet

* [ASF-tiedostomuoto – Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)

* [QuickTime-tiedostomuoto - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)


