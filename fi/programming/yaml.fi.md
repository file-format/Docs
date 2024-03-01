{
  "date": "2019-10-11",
  "keywords": [
"yaml",
".yaml",
"mikä on yaml-tiedosto",
"kuinka avata yaml-tiedosto",
"laajennus",
"tiedosto",
"yaml tiedosto",
"yaml-tiedostomuoto",
".yaml laajennus",
"yaml vs json",
"Esimerkki YAML-tiedostosta",
"docker yaml-tiedosto esimerkki"
],
  "author": {
    "display_name": "Muhammad Ahmad Chishti"
},
  "draft": "false",
  "toc": true,
  "description": " Opi YAML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata YAML-tiedoston.",
  "title": "YAML tiedostomuoto",
  "linktitle": "YAML",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-yam-fil"
}
},
  "lastmod": "2021-05-05"
}

## Mikä on YAML-tiedosto? ##

**YAML-tiedosto** koostuu kielestä YAML (YAML Ain't Markup Language), joka on Unicode-pohjainen tietojen serialointikieli; käytetään määritystiedostoihin, Internet-viesteihin, objektien pysyvyyteen jne. YAML käyttää tiedostoissaan .yaml-laajennusta. Sen syntaksi on riippumaton tietystä ohjelmointikielestä. Pohjimmiltaan YAML on suunniteltu ihmisten vuorovaikutukseen ja toimimaan hyvin nykyaikaisten ohjelmointikielten kanssa. Tuki mielivaltaisten alkuperäisten tietorakenteiden sarjoittamiselle lisäsi YAML-tiedostojen luettavuutta, mutta se on tehnyt jäsennys- ja tiedostojen luontiprosessista hieman monimutkaisen.

## Lyhyt historia ##

YAML ehdotettiin ensimmäisen kerran vuonna 2001, ja sen kehittivät Clark Evans, Ingy döt Net ja Oren Ben-Kiki. YAML:n sanottiin ensin tarkoittavan Yet Another Markup Language osoittamaan sen tarkoitusta merkintäkielenä. Myöhemmin se muutettiin nimellä YAML Aint Markup Language osoittamaan sen tarkoitusta datasuuntautuneeksi.


## YAML-tiedostomuoto ##

YAML-tiedosto koostuu seuraavista tietotyypeistä

- **Skalaarit**: Skalaarit ovat arvoja, kuten merkkijonot, kokonaisluvut, loogiset luvut jne.
- **Sekvenssit**: Jaksot ovat luetteloita, joissa jokainen kohta alkaa yhdysmerkillä (-). Listat voidaan myös sisäkkäin.
- **Mappings**: Kartoitus antaa mahdollisuuden luetella avaimet arvoineen.

### Syntaksi ###

- **Tyhjäväli**: Välilyöntien sisennystä käytetään osoittamaan sisäkkäisyyttä ja yleistä rakennetta.

``` yaml
nimi: John Smith
ottaa yhteyttä:
koti: 1012355532
toimisto: 5002586256
osoite:
katu: |
123 Tornado Alley
Sviitti 16
kaupunki: East Centerville
valtio: KS
```

- **Kommentit**: Kommentit kirjoitetaan alkaen #-symbolilla.

``` yaml
# Tämä on YAML-kommentti
```

- **Listat**: Tavuviivaa (-) käytetään osoittamaan luettelon jäseniä, joissa jokainen jäsen on erillisellä rivillä. Listan jäsenet voidaan myös sulkea hakasulkeissa ([...]) ja jäsenet erotettuina pilkuilla (,).

``` yaml
  - "A"
  - "B"
  - "C"
```

``` yaml
[A, B, C]
```

- **Associative Array**: Assosiatiivista taulukkoa ympäröivät kiharat hakasulkeet ({...}). Avaimet ja arvot erotetaan kaksoispisteellä (:) ja kukin pari on erotettu pilkulla (,).

``` yaml
{nimi: John Smith, ikä: 20}
```

- **Jousut**: Merkkijono voidaan kirjoittaa lainausmerkeillä () tai lainausmerkeillä (') tai ilman niitä.

``` yaml
Näytemerkkijono
"Näytemerkkijono"
Näytemerkkijono
```

- **Skalaarilohkon sisältö**: Skalaarisisältö voidaan kirjoittaa lohkomerkinnällä käyttämällä seuraavaa:
  - "**|**: Kaikki suorat tauot ovat merkittäviä."
  - "**>**: Jokainen rivinvaihto on taitettu välilyöntiin. Se poistaa jokaiselta riviltä johtavan välilyönnin."

``` yaml
tiedot: |
YAML
(YAML ei ole kuvauskieli)
on tietojen serialisointikieli
```

``` yaml
tiedot: ?
YAML (YAML ei ole kuvauskieli)
on tietojen serialisointikieli
```

- **Useita asiakirjoja**: Useat asiakirjat erotetaan kolmella yhdysviivalla (---) samassa virrassa. Tavuviivat osoittavat asiakirjan alun. Tavuviivoja käytetään myös erottamaan käskyt asiakirjan sisällöstä. Asiakirjan loppu on merkitty kolmella pisteellä (...).

``` yaml
  ---
Asiakirja 1
  ---
Asiakirja 2
...
```

- **Tyyppi**: Arvon tyypin määrittämiseen käytetään kaksoishuutomerkkejä (!!).

``` yaml
a: !!kelluke 123
b: !!str 123
```

- **Tunniste**: Tunnisteen määrittämiseksi muistiinpanoon käytetään et-merkkiä (&) ja solmuun viitattaessa käytetään tähteä (*).

``` yaml
nimi: John Smith
laskutusosoite: &id01
katu: |
123 Tornado Alley
Sviitti 16
kaupunki: East Centerville
valtio: KS

toimitusosoite: *id01
```

- **Direktiivit**: YAML-asiakirjoja voidaan edeltää virrassa olevia ohjeita. Ohjeet alkavat prosenttimerkillä (%), jota seuraa nimi ja sitten parametrit välilyönnillä erotettuina.

``` yaml
%YAML 1.2
  ---
Asiakirjan sisältö
```
## Esimerkki YAML-tiedostosta
Tässä näet **docker yaml -tiedoston esimerkin** alla:

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML vs JSON
Pohjimmiltaan sekä JSON että YAML on kehitetty tarjoamaan ihmisen luettavissa oleva tiedonsiirtomuoto. YAML on toteutettu JSON-muodon superjoukkona. Se tarkoittaa, että voimme jäsentää JSONia YAML-jäsennin avulla. Vaikka tämän teorian käytännön toteutus on vähän hankalaa. Siksi alla on joitain peruseroja YAML:n ja JSON:n välillä:

|YAML| JSON|
---|---|
|Monimutkainen ja aikaa vievä sarjoitettujen tietojen jäsennysprosessi |JSON-sarjamuotoisten tietojen jäsentäminen nopeasti ja helposti yksinkertaisemmalla suunnittelulla|
|Vähemmän yhteisön tukea| Suurempi yhteisön tuki ja suosio|
|Tukee kommentteja| Ei tue kommentteja|
|Kyky käyttää viittauksia muihin tietoobjekteihin| Monimutkaisten rakenteiden sarjoittaminen objektiviittauksilla on mahdotonta|
|Hierarkia merkitään käyttämällä kaksoisvälimerkkejä. Sarkainmerkit eivät ole sallittuja|Objektit ja taulukot on merkitty aaltosulkeilla.|
|Lausausmerkit ovat valinnaisia, mutta se tukee kerta- ja kaksoislainausmerkkejä.|Merkijonojen on oltava lainausmerkeissä.|
|Juurisolmu voi olla mikä tahansa kelvollisista tietotyypeistä|Juurisolmun on oltava joko array tai objekti.|


## Viitteet ##

- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

