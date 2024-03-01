{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCL",
  "description": "Opi PCL-tiedostomuodosta ja API:ista, jotka voivat luoda ja avata PCL-tiedostoja.",
  "linktitle": "PCL",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-pc-fil"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on PCL-tiedosto? ##

PCL on lyhenne sanoista Printer Command Language, joka on Hewlett Packardin (HP) julkaisema sivun kuvauskieli. HP loi PCL:n tarjoamaan tehokkaan tavan hallita tulostimen ominaisuuksia useissa eri tulostuslaitteissa. Muoto kehitettiin alun perin HP:n pistematriisi- ja mustesuihkutulostimia varten, mutta se on ajan myötä ollut osa erilaisia lämpö-, matriisi- ja sivutulostimia. Muotoille tehtiin useita eri versioita, joiden tuloksena syntyi erilaisia versioita, joissa jokaista versiota parannettiin vastaamaan tulostimen ohjausominaisuuksien aikavaatimuksia. Nykyään PCL on laajimmin levinnyt tulostinkieli uusimpien tulostimien markkinoilla.

## PCL-versiot ##

PCL-versiot eroavat toiminnallisuudeltaan (esim. fonttityyppituki: bittikarttafontit, skaalautuvat fontit (Intellifonts, TrueType-fontit), rasterigrafiikkapakkausmenetelmät, HP-GL/2-grafiikkatuki).

**PCL 1:** noin 1980 - Print and Space -toiminto on toimintojen perusjoukko yksinkertaiseen, kätevään, yhden käyttäjän työasematulostukseen.

**PCL 2:** around 1980 - EDP (Electronic Data Processing)/Transaction functionality is a superset of PCL 1. Lisättiin toimintoja yleiskäyttöistä, usean käyttäjän järjestelmätulostusta varten.

**PCL 3**: 1984 - Office Word Processing functionality is a superset of PCL 2. Lisättiin toimintoja korkealaatuista toimistoasiakirjojen tuotantoa varten ja dpi nostettiin 300 dpi:iin. Se salli rajoitetun määrän bittikarttafontteja ja -grafiikkaa käytön ja tuki HP-GL:ää. Muut tulostinvalmistajat jäljittelivät PCL 3:a laajalti, ja nämä yritykset kutsuivat sitä LaserJet Plus -emulaatioksi.
(Tulostimet: HP DeskJet -perhe, HP LaserJet -sarjan tulostin, HP LaserJet Plus -sarjan tulostin)

**PCL3+:** DeskJet- ja DesignJet-tulostimien käyttämä.

**PCL3c:** DeskJet- ja DesignJet-tulostimien käyttämä.

**PCL3e**: DeskJet- ja DesignJet-tulostimien käyttämä. Nyt käytössä myös PhotoSmartissa.

**PCL3GUI**: Käyttää RTL:ää, ja sitä käyttävät DeskJet- ja DesignJet-tulostinperheet.

**PCLSLEEK**: Käyttää RTL:ää, ja sitä käyttävät DeskJet- ja DesignJet-tulostinperheet.

**PCL 4**: 1985 - Page formatting functionality is a superset of PCL 3. Tuetut makrot, suuremmat bittikarttafontit ja grafiikka. (Tulostimet: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing functionality is a superset of PCL 4. Uusia julkaisuominaisuuksia ovat fonttien skaalaus ja HP-GL/2 (vektori)grafiikka. (Tulostimet: HP LaserJet III)

**PCL 5e:** 1994 - Tämä on merkittävä versio, joka sisältää uusia ominaisuuksia, kuten Adaptive Compression System, 2-tavuinen merkkikoodaus, tuen vektorifontteja ja kaksisuuntaisia konfigurointikomentoja. Sisältää loogiset operaatiot (vastaa GDI ROP:ita) Windowsin tuen parantamiseksi ennen leikkauspolkuja. (Tulostimet: HP LaserJet 4)

**PCL 5j:** Uusia ominaisuuksia, kuten 2-tavuinen merkkituki japanilaisille skaalautuville fonteille, pystykirjoitus, japanilaiset paperikoot ja kirjasinjonot. (Tulostimet: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Colour support and Logical Operations was added to PCL5. PCL5c predates PCL5e. Some models also support clipping paths. (Printers: HP Colour LaserJet, HP PaintJet 300 XL (first printer with PCL5c), HP DeskJet 1200C/1600C (these model numbers have been re-used and the newer models are not PCL 5c)

**PCL 5ce:** Tukee Agfa Microtypen skaalattavia kirjasintyyppejä. (Tulostimet: HP 2500c Pro Printer)

**PCL 6 / XL:** 1996 - PCL 6 tai PCL XL on vuonna 1995 esitelty uusi muoto, joka ei ole yhteensopiva PCL:n aiempien versioiden kanssa. (Tulostimet: HP LaserJet 5, 5M ja 5N)

## PCL 6:n yleiskatsaus ##

HP esitteli PCL 6:n vuonna 1996, joka oli PCL-kielen ja siihen liittyvien teknologioiden seuraava kehitys. Siinä on seuraavat komponentit:

**PCL 6 Enhanced:** tarjoaa optimoidun version tulostamiseen graafisista käyttöliittymistä (GUI), kuten MS Windowsista ja OS/2:sta

**PCL 6 -standardi:** tarjoaa täydellisen taaksepäin yhteensopivuuden aiempien HP LaserJet -tulostimien kanssa

**PCL Font Synthesis:** tarjoaa skaalattavia fontteja, kirjasinten hallinnan ja lomakkeiden ja fonttien tallennuksen.

Laajennettu versio PCL XL on lähempänä GDI:tä, jota monet sovellukset käyttävät. Se varmistaa, että käännöksiä tehdään vähemmän, mikä lisää WYSIWYG-ominaisuuksia ja parantaa suorituskykyä sovelluksilla, jotka tukevat Enhanced-ohjaimen toteuttamia pakotuksia. Enhanced (PCL XL) -ohjaimen lähtö ei välttämättä ole sama kuin vakioohjaimen lähtö. Jos tulos ei ole odotusten mukainen, valitse sen sijaan Standard (PCL5e) -ohjain.

PCL 6 Enhanced -komennot on suunniteltu vastaamaan optimaalisesti GUI-pohjaisten sovellusten grafiikan tulostusvaatimuksia. Useimmissa tapauksissa jokaiselle grafiikan tulostuskomennolle, jonka GUI haluaa suorittaa, on vastaava PCL 6 Enhanced -komento. Tämä vähentää grafiikkasivun kuvaamiseen tarvittavien komentojen määrää. Jokainen PCL 6 Enhancedin komento on suunniteltu vaatimaan mahdollisimman vähän tiedonsiirtoa isäntätietokoneesta tulostimeen. Tämä vähentää sivun kuvaamiseen tarvittavan tiedon määrää.

Useimpien HP LaserJet -tulostimien Windows-tulostusjärjestelmässä on kaksi erillistä ohjainta: Standard ja Enhanced. Standard-ohjain tarjoaa taaksepäin yhteensopivuuden käyttämällä PCL 6 Standard (PCL5e) -komentoja yksinkertaisen tekstin tai sekateksti- ja grafiikkasivujen tulostamiseen. Enhanced-ohjain käyttää PCL 6 Enhanced -komentoja, jotka on optimoitu monimutkaisten grafiikkasivujen tulostamiseen.

## PCL 6 -luokan versiot ##

#### Luokka 1.1 ####

**Piirtotyökalut:** Tukee piirustusviivoja, kaaria/ellipsiä/sointuja, (pyöristettyjä) suorakulmioita, polygoneja, Bezier-polkuja, leikattuja polkuja, rasterikuvia, skannausviivoja, rasteritoimintoja.
**Värien käsittely:** Tukee 1/4/8-bittisiä paletteja, RGB/harmaa väriavaruutta. Tukee mukautettuja rasterikuvioita (enintään 256 kuviota).
**Pakkaus:** Tukee RLE:tä.
**Mittayksiköt:** tuuma, millimetri, millimetrin kymmenesosa.
**Paperinkäsittely:** Tukee mukautettuja tai ennalta määritettyjä paperityyppejä, mukaan lukien tavalliset Letter, Legal, A4 jne. Voit valita paperin käsinsyötöstä, lokeroista ja kaseteista. Paperi voidaan tulostaa kaksipuolisesti vaaka- tai pystysuoraan. Paperi voidaan suunnata pysty-, vaaka- tai 180 asteen kiertosuuntaan.
**Font:** Supports bitmap or TrueType fonts, 8 or 16-bit code points. Choosing character set uses different symbol set code from PCL 5. Kun käytetään bittikarttafonttia, monet skaalauskomennot eivät ole käytettävissä. Kun käytetään TrueType-fonttia, vaihtuvapituisia kuvauksia, jatkolohkoja ei tueta. Outline-fonttia voidaan kiertää, skaalata tai leikata.

#### Luokka 2.0 ####

**Pakkaus:** Lisätty oma JPEG-pakkaus nimeltä JetReady.
**Paperinkäsittely:** Materiaali voidaan ohjata eri tulostelokeroihin (enintään 256). Lisätty A6 ja japanilainen B6 esiasetetut materiaalikoot. Lisätty kolmas kasetin esiasetus, 248 ulkoisen lokeron materiaalilähdettä.
**Fontti:** Teksti voidaan kirjoittaa pystysuunnassa.

#### Luokka 2.1 ####

**Värien käsittely:** Lisätty värinsovitusominaisuus.
**Pakkaus:** Lisätty Delta-rivi.
**Paperinkäsittely:** Suunta, materiaalikoko ovat valinnaisia uuden sivun ilmoittamisen yhteydessä. Lisätty B5, JIS 8K, JIS 16K, JIS Exec paperityypit.

#### Luokka 3.0 ####

**Värien käsittely:** Salli eri rasteriasetusten käyttö vektori- tai rasterigrafiikassa, tekstissä. Tukee mukautuvaa puolisävytystä.
**Protocol:** Supports PCL passthrough, allowing PCL 5 features to be used by PCL 6 streams. However, some PCL 6 states are not preserved when using this feature.
**Fontti:** Tukee PCL-fontteja.
**Viewer/Converter:** PCLReader (ilmainen ohjelmisto) voi tarkastella, muuntaa tai tulostaa minkä tahansa PCL 6 -tason (mukaan lukien JetReady) mille tahansa tulostimelle.

## Viitteet ##

* [PCL - Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)


