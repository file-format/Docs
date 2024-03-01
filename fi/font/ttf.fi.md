{
  "date": "2020-08-20",
  "keywords": [
"ttf tiedosto",
"ttf tiedostomuoto",
"mikä on ttf-tiedosto",
"tiedosto",
"ttf esimerkki",
"ttf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TTF - TrueType-fonttitiedostomuoto",
  "description": "TrueType-fontit (TTF) perustuvat Apple, Inc:n alun perin suunnittelemiin digitaalisen kirjasintekniikan spesifikaatioihin. Sekä Apple että Microsoft käyttivät TTF:ää Mac- ja Windows-käyttöjärjestelmissä.",
  "linktitle": "TTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-fif"
}
},
  "lastmod": "2020-09-21"
}

## Mikä on TTF-tiedosto?

Tiedosto, jonka tunniste on .ttf, edustaa kirjasintiedostoja, jotka perustuvat TrueType-määritysten kirjasintekniikkaan. Sen alun perin suunnitteli ja lanseerasi Apple Computer, Inc Mac OS:lle, ja myöhemmin Microsoft otti sen käyttöön Windows-käyttöjärjestelmälle. TrueType-fontit tarjoavat korkealaatuisen näytön tietokoneen näytöillä ja tulostimilla ilman, että ne ovat riippuvaisia resoluutiosta. Kaikki nykyaikaiset fontteja käyttävät sovellukset pystyvät toimimaan TTF-tiedostojen kanssa. TTF-fonttitiedostot ovat vapaasti saatavilla Internetissä, ja ne voidaan myös muuntaa muihin fonttitiedostomuotoihin, kuten OTF ja WOFF.

## Lyhyt historia

Designed by Apply Computer, Inc in 1980s for MacOS, the TTF font format was aimed at resolving some technical limitations by Adobe's Type 1 format. Apple included support for TrueType fonts in Mac in 1991. TTF-fonttien suunnittelutavoitteena oli varastoinnin ja käsittelyn tehokkuus sekä laajennettavuus. Tämän laajennettavuuden perusteella olemassa olevat kirjasimet voidaan muuntaa TrueType-muotoon.

Microsoft käytti TrueType-fontteja ensimmäisen kerran Windows 3.1:ssä huhtikuussa 1992 sen jälkeen, kun Apple suostui lisensoimaan TrueTypen Microsoftille. Se paransi rasterointimekanismia ja paransi sen tehokkuutta ja suorituskykyä.

## True Type -tiedostomuodon tiedot

TrueType-fonttitiedosto on binääritiedosto, joka koostuu ketjutettujen taulukoiden sarjasta. Jokainen taulukko on sanasarja, ja sen nimi tunnetaan nimellä Tag. Jokainen tagi on uint32-tietotyyppiä ja koostuu neljästä merkistä. Tiedoston ensimmäinen taulukko on fonttihakemisto, joka antaa pääsyn muihin fonttitiedoston taulukoihin. Fonttitiedot sisältyvät muihin taulukoihin, jotka seuraavat fonttihakemistotaulukon jälkeen. Koska jokaiseen taulukkoon pääsee käsiksi sen tagilla, taulukot voivat näkyä missä tahansa järjestyksessä tiedostossa.

Tarvittavat taulukot ja niiden tunnisteiden nimet näkyvät seuraavassa taulukossa.

|**Tag**|**Taulukko**|
---|---|
|'cmap'| merkistä kuvioon kartoitus|
|'glyf'| glyph data|
|'pää'| fontin otsikko|
|'hhea'| vaakasuora otsikko|
|'hmtx'| vaakasuuntaiset mittarit|
|'loca'| hakemisto sijaintiin|
|'maxp'| maksimiprofiili|
|'nimi'| nimeäminen|
|'postittaa'| PostScript|

### Tietotyypit
TrueType-kirjasimet käyttävät vakiokokonaislukuja ja muita tietotyyppejä, jotka on lueteltu seuraavassa taulukossa.

|**Tietotyyppi** | **Kuvaus** |
---|---|
|shortFrac| 16-bittinen etumerkillinen murtoluku|
|Kiinteä| 16,16-bittinen etumerkillinen kiinteän pisteen numero|
|FWord| 16-bittinen etumerkillinen kokonaisluku, joka kuvaa suuren FU-yksiköissä, pienin mitattava etäisyys em-avaruudessa.|
|uFWord| 16-bittinen etumerkitön kokonaisluku, joka kuvaa suuren FU-yksiköissä, pienin mitattava etäisyys em-avaruudessa.|
|F2Piste14| 16-bittinen etumerkillinen kiinteä luku, jossa alhainen 14 bittiä edustaa murto-osaa.|
|longDateTime|	The long internal format of a date in seconds since 12:00 midnight, January 1, 1904. It is represented as a signed 64-bit integer.|

### Fonttihakemisto

Ensimmäinen TrueType-fontin taulukko on kirjasinhakemisto, joka tarjoaa pääsyn tietoihin, joita tarvitaan muiden taulukoiden tietojen käyttämiseen. Se koostuu lisäksi:

 * Offset-alitaulukko - pitää kirjaa taulukoista fontissa ja tarjoaa offset-tiedot hakemiston jokaiseen taulukkoon pääsyä varten
 * `Table Directory` - Sisältää merkinnät jokaiselle fontin taulukolle

#### Offset-alitaulukko
Offset-alitaulukko on esitetty alla.

|**Tyyppi**|**Nimi**|**Kuvaus**|
---|---|---|
|uint32| skaalaustyyppi| Tunniste, joka ilmaisee tämän fontin rasterointiin käytettävän OFA-skaalaimen; katso lisätietoja alla olevasta skaalaimen tyyppiä koskevasta huomautuksesta.|
|uint16| numTables| taulukoiden määrä|
|uint16| hakualue| (maksimiteho 2 <= numTables)*16|
|uint16| entrySelector| log2(maksimiteho 2 <= numTables)|
|uint16| rangeShift| numTables*16-searchRange|

#### Taulukkohakemisto
Taulukkohakemisto tulee heti offset-alitaulukon jälkeen. Sen rakenne on seuraavan taulukon mukainen.

|**Tyyppi**|**Nimi**|**Kuvaus**|
---|---|---|
|uint32| tag| 4-tavuinen tunniste|
|uint32| tarkistussumma| tämän taulukon tarkistussumma|
|uint32| offset| offset sfnt|:n alusta
|uint32| pituus| tämän taulukon pituus tavuina (todellinen pituus ei täytettyä pituutta)|

Jokaisella fonttitiedoston taulukolla on oltava oma taulukkohakemistonsa. Taulukon merkinnät on lajiteltava nousevaan järjestykseen tunnisteen mukaan.


## Viitteet
 * [TrueType Font Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
 * [TrueType Overview](https://learn.microsoft.com/en-us/typography/truetype/)

