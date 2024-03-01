{
  "date": "2019-10-11",
  "keywords": [
"osm tiedosto",
"mikä on osm-tiedosto",
"tiedosto",
"osm esimerkki",
"osm tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OSM - OpenStreetMap-tiedostomuoto",
  "description": "Opi OSM-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OSM-tiedostoja.",
  "linktitle": "OSM",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-os-fim"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on OSM-tiedosto?

OpenStreetMap (OSM) on valtava kokoelma vapaaehtoisia maantieteellisiä tietoja, jotka tallennetaan eri tyyppisiin tiedostoihin, jotka käyttävät erilaisia koodausmenetelmiä tietojen muuntamiseen biteiksi ja tavuiksi. OSM on yhteistyöprojekti ilmaisen muokattavan maailmankartan luomiseksi. Tämän yhteistyön ensisijainen tulos on maantieteellinen tieto eikä itse kartta. Maantieteellisten tietojen käytön tai saatavuuden rajoitukset suuressa osassa maailmaa laukaisevat tarpeen luoda OSM.

OSM:ltä saatavilla oleva data on valmis korvaamaan Google Mapsin klassisissa sovelluksissa (Facebook, Craigslist jne.) ja oletustiedot GPS-vastaanottimien sovelluksissa. Vaikka tiedon laatu vaihtelee eri puolilla maailmaa, OpenStreetMap-tietoja voidaan verrata kätevästi patenttitietolähteisiin.

## OSM-tiedostomuodon lyhyt historia

Wikipedian menestyksen innoittamana brittiläinen yrittäjä Steve Coast loi vuonna 2004 tämän yhteisöpohjaisen maailmankartoitusprojektin Isossa-Britanniassa. Hän keskittyi aluksi Yhdistyneen kuningaskunnan kartoittamiseen. OpenStreetMap Foundation perustettiin ensimmäisen kerran huhtikuussa 2006 tukemaan ilmaisten geospatiaalien kehitystä, laajentumista ja levitystä kenelle tahansa. Joulukuussa 2006 Yahoo auttoi OpenStreetMapia sen ilmakuvauksessa karttatuotantoa varten.

Automotive Navigation Data (AND) toimitti OSM:lle huhtikuussa 2007 täydelliset Alankomaiden tietiedot sekä Intian ja Kiinan valtatietiedot. Joulukuussa 2007 Oxfordin yliopisto oli merkittävin organisaatio, joka integroi OpenStreetMap-tiedot pääsivustoonsa. Siitä lähtien yli 2 miljoonaa rekisteröityä käyttäjää on lisännyt tietoja tähän projektiin käyttämällä GPS-laitteita, ilmakuvausta ja manuaalisia tutkimuksia. Tämä yhteisön tuottama data on saatavilla Open Database -lisenssillä. Englannissa rekisteröity voittoa tavoittelematon OpenStreetMap Foundation -järjestö ylläpitää OSM-sivustoa.

## OSM-tiedostomuoto

Maantieteellisten tietojen tallentamiseen on monia tapoja ja tiedostomuotoja, mutta **OSM**-tiedostomuoto on rajoitettu OpenStreetMapiin. OSM on erityisesti suunniteltu vakiomuoto, joka on tarkoitettu helposti siirrettäväksi Internetin yli. Jäsennelty järjestetty muoto, joka on koodattu XML:llä, muodostaa .osm-tiedoston. OpenStreetMapissa on neljä pivot-elementtiä topologisen tietorakenteen tallentamiseen:

{{< figure src="../OSM.png" alt="OSM-tiedostomuoto" >}}


|Solmut|Tavat|Suhteet|Tagit
---|---|---|---|
|<ul><li> Edustaa maantieteellistä sijaintia, joka on tallennettu leveys- ja pituusasteen pareina.</li><li> Käytetään edustamaan karttakohteita ilman kokoa, kuten vuorenhuippuja.</li></ul> |<ul><li> Lajiteltu luettelot solmuista, jotka merkitsevät polylinjaa tai monikulmiota</li><li> Edustavat lineaarisia piirteitä, kuten teitä ja jokia, ja vyöhykkeitä, kuten pysäköintialueita viidakoita ja puistoja.</li></ul> |<ul><li> Lajiteltu luettelo solmuista ja tavoista edustaa niiden suhdetta, kuten esteet ja u-käännökset teillä, moottoritiet kattavat erilaisia olemassa olevia reittejä ja reikiä sisältäviä alueita.</li></ul> |<ul><li> Tallenna karttaobjektien metatiedot.* Aina liitettynä mihin tahansa solmuun, tapaan tai suhteeseen</li></ul>


Tags are used to characterize on ground physical features (buildings and roads etc.) in OpenStreetMap. Each tag relates a geographic characteristic of the feature represented by that specific node or relation. In this free tagging system, to describe a feature, unlimited number of attributes can be included in a map. Specific key and value combinations endorsed by registered users act as informal standards for the frequent used tags. However, new tags can be created whenever new aspects require to analyze previously unmapped attributes of the features. Most features use only a small number of tags for description.

OSM käyttää kolmen tyyppisiä tiedostoja tärkeimpien tietojensa tallentamiseen.

OSM käsittelee kaikkia näitä tiedostoja niiden muotoilutietojen kanssa. Mutta nämä tiedostot tuottavat samat sisäiset objektit. Datatiedostoille OSM-objektien näkyvä lippu on aina tosi, mikä ei koske historia- ja muutostiedostoja.

Yleisessä käytössä OSM-tiedostomuodot ovat erilaisia. Tiedostomuodot määrittävät levyn tai langan sisällön koodauksen bitteinä ja tavuina. OSM pystyy lukemaan ja kirjoittamaan maksimissaan näitä formaatteja.

**XML**

Alkuperäinen OSM-muoto on XML-pohjainen. OSM-päätietokannan API:n palautustiedot ovat XML-muodossa.

**PBF**

Protocol Buffers -koodaus on binäärimuodossa ja yksi kompakteimmista formaateista.

**O5M/O5C**

Binäärimuotoon perustuva yksinkertaisempi muoto, mutta suhteellisen vähemmän käytetty. OSM osaa lukea, mutta ei voi kirjoittaa tätä muotoa.

**OPL**

Yksinkertainen muoto, jota ehdotetaan käytettäväksi tavallisten UNIX-komentorivityökalujen kanssa. Lähellä CSV-tiedostoja, sallii yhden OSM-entiteetin yhdellä rivillä.

**DEBUG**

Tekstipohjainen muoto, joka on tarkoitettu luotavaan virheenkorjausta varten. OSM osaa kirjoittaa tätä muotoa, mutta ei voi lukea.

**MUSTA AUKKO**

Tekevä muoto, joka poistaa kaikki tiedot. OSM osaa kirjoittaa tätä muotoa, mutta ei voi lukea.

## OSM Data Storage ##

OSM:n **PostgreSQL**-päätietokanta säilyttää pääkopion OSM-tiedoista PostGIS-laajennuksella. Päätietokanta ylläpitää jokaiselle dataprimitiiville taulukkoa, jonka rivit tallentavat yksittäisiä objekteja. Kaikki muokkaukset päivittävät tätä tietokantaa ja kaikki muut muodot muodostetaan tätä tietokantaa käyttäen. Lukuisia ladattavia tietokantapooleja luodaan tietojen siirtämiseksi paikasta toiseen. Kaksi muotoa, joista toinen käyttää XML:ää ja toinen Protocol Buffer Binary Format (PBF) -muotoa, määrittää nämä poolit. Täydelliset tiedot tallennetaan tiedostoon nimeltä planet.osm

## Pakkaus OSM-tiedostoissa ##

Tekstipohjaiset muodot (XML, OPL ja Debug) käyttävät valinnaisesti gzip- tai bzip2-pakkausta.

## Viitteet ##

* [OSM-tiedostomuotojen käsikirja](https://osmcode.org/file-formats-manual/#file-types)

* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)

* [Opi OSM](https://learnosm.org/en/osm-data/getting-data/)


