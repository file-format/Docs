{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" : [ "fundamentals" ],
  "description": "Portable Document Format (PDF) on ohjelmistosta, laitteistosta ja käyttöjärjestelmästä riippumaton asiakirjojen vakioesitys. PDF-standardeja ovat PDF/A, PDF/E, PDF/UA, PDF/VT ja PDF/X.",
  "title" : "PDF-tiedostomuoto - mikä on PDF-tiedosto?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
"weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) on Adoben 1990-luvulla luoma asiakirja. Tämän tiedostomuodon tarkoituksena oli ottaa käyttöön standardi asiakirjojen ja muun viitemateriaalin esittämiseksi muodossa, joka on riippumaton sovellusohjelmistosta, laitteistosta ja käyttöjärjestelmästä. PDF-tiedostomuodossa on täysi kyky sisältää tietoja, kuten tekstiä, kuvia, hyperlinkkejä, lomakekenttiä, multimediaa, digitaalisia allekirjoituksia, liitteitä, metatietoja, paikkatietoominaisuuksia ja 3D-objekteja, joista voi tulla osa lähdeasiakirjaa.

Useimmissa tapauksissa olemassa olevat asiakirjat muunnetaan PDF-muotoon sen sijaan, että luodaan uusi PDF tyhjästä. Mutta se ei tarkoita, ettei PDF-tiedostojen luomiseen tai käsittelyyn ole ohjelmistoja.

**(Pitäisikö sinun jakaa jotain PDF-tiedostomuodosta? Voit lähettää havainnot [PDF File Format News](https://news.fileformat.com/t/PDF)-osioon.)**

## PDF-tiedostomuoto - lyhyt historia

Nopea läpikäynti aikajanasta {{HYPERLINKKI}} aikajanan suhteen on seuraava:

**1993** - Adobe Systems julkaisi PDF-eritelmät ilmaiseksi

**2008** - PDF julkaistiin avoimena standardina 1. heinäkuuta 2008, ja Kansainvälinen standardointijärjestö julkaisi sen nimellä **ISO 32000-1:2008**.

**2008** – Adobe julkaisi julkisen patenttilisenssin ISO 32000-1 -muotoon rojaltivapaat oikeudet kaikille Adoben omistamille patenteille, jotka ovat tarpeen PDF-yhteensopivien toteutusten tekemiseen, käyttämiseen, myymiseen ja jakeluun.

The first version of PDF designated as PDF 1.0 which later went through revisions up to PDF 1.7. PDF 1.7, josta tuli ISO 32000-1, sisältää joitain standardoimattomia patentoituja tekniikoita sekä kuten Adobe XML Forms Architecture (XFA) ja JavaScript-laajennuksen Acrobatille. Se oli 28. heinäkuuta 2017, kun PDF 2.0, joka tunnetaan nimellä ISO 32000-2:2017, julkaistiin ja joka ei sisällä standardoimattomia tekniikoita.

## PDF-tiedostomuodon tekniset tiedot

PDF-tiedosto on joukko tavuja, jotka voidaan ryhmitellä tunnuksiksi PDF-määritysten määrittelemien syntaksisääntöjen mukaisesti. Kerran tai useampia tokeneita yhdistetään ylemmän tason syntaktisten kokonaisuuksien muodostamiseksi, pääasiassa objekteiksi, jotka ovat perustietoarvoja, joista PDF-dokumentti muodostetaan.

### PDF-tiedostojen tiedostorakenne

PDF-tiedoston sisältö on järjestetty seuraavassa järjestyksessä tiedoston sisällä.

|Otsikko
| Runko
|Ristiviittaustaulukko
| Traileri

#### PDF-tiedoston otsikko ####

PDF-versiosta riippumatta PDF-tiedosto alkaa otsikolla, joka sisältää yksilöllisen PDF-tunnisteen ja muodon version, kuten %PDF-1.x, jossa x on 1-7.

#### Tiedostoteksti ####

PDF-tiedoston runko koostuu sarjasta epäsuoria objekteja, jotka edustavat asiakirjan sisältöä. Yllä kuvatut objektit edustavat asiakirjan osia, kuten fontteja, sivuja ja näytekuvia. PDF 1.5:stä alkaen runko voi sisältää myös objektivirtoja, joista jokainen sisältää sarjan epäsuoria objekteja.

#### Ristiviittaustaulukko ####

Ristiviittaustaulukko sisältää tietoja, jotka mahdollistavat satunnaisen pääsyn tiedoston epäsuoriin objekteihin, joten koko tiedostoa ei tarvitse lukea minkään tietyn objektin löytämiseksi. Taulukossa on oltava yksirivinen merkintä kullekin epäsuoralle objektille, joka määrittää kyseisen objektin tavusiirron tiedoston rungossa. (PDF 1.5:stä alkaen osa tai kaikki ristiviittaustiedot voivat vaihtoehtoisesti sisältyä ristiviittausvirtoihin.

#### Tiedoston traileri ####

PDF-tiedoston trailerin avulla vaatimustenmukainen lukija löytää nopeasti ristiviittaustaulukon ja tietyt erikoiskohteet. Mukavien lukijoiden tulee lukea PDF-tiedosto sen lopusta. Tiedoston viimeinen rivi saa sisältää vain tiedoston loppumerkin, %%EOF. Kahdella edellisellä rivillä on oltava yksi riviä kohden ja järjestyksessä avainsana startxref ja tavupoikkeama dekoodatussa virrassa tiedoston alusta viimeisen ristiviittausosan xref-avainsanan alkuun.

### PDF-objektit ###

PDF-tiedosto sisältää useita erityyppisiä objekteja, jotka ovat seuraavan tyyppisiä

* Boolen arvot - edustavat ehdollista tosi tai epätosi

* Numerot - kokonaisluku- ja reaaliarvot

* Merkkijonot - sisältää merkkejä suluissa

* Nimet - aloita eteenpäin / merkillä esim. /ASomewhatLongerName johtaa ASomewhatPidempiNimi

* Taulukot - PDF tukee yksiulotteisia taulukoita. Mittasuhteiltaan suurempia taulukoita voidaan rakentaa käyttämällä taulukoita sisäkkäisinä elementteinä

* Sanakirjat - kokoelma esineitä avain-arvo pareina. Siinä voi olla nolla merkintää.

* Virrat - edustaa tavujen sarjaa, joka voi olla myös rajoittamattoman pituinen

* Null Object - edustaa nolla-arvoa


Saattaa olla muitakin objekteja, kuten kommentteja, jotka lisätään %-merkillä ja voivat sisältää 8-bittisiä merkkejä.

### Epäsuorat objektit ###

Mikä tahansa PDF-tiedoston objekti voidaan merkitä epäsuoraksi objektiksi. Epäsuoralle kohteelle annetaan yksilöllinen objektitunniste, jolla muut objektit voivat viitata niihin. Ristiviittaukset näihin säilytetään hakemistotaulukossa ja merkitty xref-avainsanalla, joka seuraa päärunkoa ja antaa kunkin epäsuoran objektin tavupoikkeaman tiedoston alusta.

### Lineaariset ja epälineaariset PDF-asettelut ###

PDF-asettelut luokitellaan Llneaarisiin ja epälineaarisiin kohdesovellusten ja muiden tekijöiden mukaan.

Epälineaariset - Epälineaariset PDF-tiedostot käyttävät vähemmän levytilaa kuin lineaariset PDF-tiedostot. Asiakirjan PDF-sivut ovat hajallaan PDF-tiedoston poikki, ja siksi epälineaariset tiedostot ovat hitaampia kuin lineaariset tiedostot.

Lineaarinen PDF - Online-PDF-katseluohjelmiin kohdistetut lineaariset PDF-tiedostot on rakennettu siten, että ne kirjoitetaan levylle lineaarisesti. Tämä ei vaadi selainlaajennuksia, jotta koko asiakirja latautuu ennen näyttöä.

### Esineiden yleiskatsaus ###

Kuten mainittiin, PDF-teksti on kokoelma edellä mainittuja objekteja. PDF perustuu suurelta osin PostScriptiin ilman ohjelmointikielten ohjausominaisuuksia, kuten if- ja loop-komentoja. Postscript-koodin antamat komennot graafisen sisällön luomiseksi kerätään ja tunnistetaan asiakirjan viittaamien tiedostojen, grafiikan tai fonttien lisäksi. Kaikki nämä sisällöt kerätään yhdeksi tiedostoksi, jolloin tuloksena on koostettu PostScript-tulostus.

#### Teksti ####

Text in PDF is represented by text elements which are actually displayed with glyphs from fonts.   A  glyph  is  a  graphical  shape  and  is  subject  to  all  graphical  manipulations,  such  as  coordinate transformation. Because of the importance of text in most page descriptions, PDF provides higher-level facilities to describe, select, and render glyphs conveniently and efficiently.

#### Grafiikka ####

PDF-sisältövirroissa käytetyt grafiikkaoperaattorit kuvaavat rasteritulostuslaitteella toistettavien sivujen ulkoasua. Tilat on tarkoitettu sekä tulostin- että näyttösovelluksiin. Grafiikkaoperaattorit muodostavat kuusi pääryhmää:

* Grafiikkatilan operaattorit manipuloivat datarakennetta, jota kutsutaan grafiikkatilaksi, globaaliksi kehykseksi, jossa muut grafiikkaoperaattorit suorittavat. Grafiikkatila sisältää nykyisen muunnosmatriisin (CTM), joka kartoittaa PDF-sisältövirrassa käytetyt käyttäjätilan koordinaatit tulostuslaitteen koordinaatteiksi. Se sisältää myös nykyisen värin, nykyisen leikkauspolun ja monia muita parametreja, jotka ovat maalausoperaattoreiden implisiittisiä operandeja.

* Polun rakennusoperaattorit määrittävät polut, jotka määrittävät muodot, viivaradat ja erityyppiset alueet. Ne sisältävät operaattorit uuden polun aloittamiseksi, osien ja käyrien lisäämiseksi siihen ja sen sulkemiseksi.

* Reitin maalausoperaattorit täyttävät polun värillä, maalaavat viivan sitä pitkin tai käyttävät sitä leikkausrajana.

* Muut maalausoperaattorit maalaavat tiettyjä itsekuvaavia grafiikkaobjekteja. Näitä ovat näytekuvat, geometrisesti määritellyt varjostukset ja kokonaiset sisältövirrat, jotka puolestaan sisältävät grafiikkaoperaattoreiden sarjoja.

* Text operators select and show character glyphs from fonts (descriptions of typefaces for representing text characters). Because PDF treats glyphs as general graphical shapes, many of the text operators could be grouped with the graphics state or painting operators. However, the data structures and mechanisms for dealing with glyph and font descriptions are sufficiently specialized.
* Merkityn sisällön operaattorit yhdistävät korkeamman tason loogiset tiedot sisältövirran objekteihin. Nämä tiedot eivät vaikuta sisällön renderoituun ulkoasuun. se on hyödyllinen sovelluksille, jotka käyttävät PDF-tiedostoa asiakirjojen vaihtoon.


## Viitteet ##

* [PDF-tiedostomuoto: perusrakenne](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)

* [PDF – Wikipedia](https://en.wikipedia.org/wiki/PDF)

* [PDF-viite – Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)


