{
  "date": "2019-10-11",
  "keywords": [
"emf-tiedosto",
"emf tiedostomuoto",
"mikä on emf-tiedosto",
"tiedosto",
"emf esimerkki",
"emf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMF - Enhanced Metafile Format",
  "description": "Opi EMF-tiedostomuodoista ja sovellusliittymistä, jotka voivat luoda ja avata EMF-tiedostoja.",
  "linktitle": "EMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on EMF-tiedosto?

**Enhanced metafile format (EMF)** tallentaa graafiset kuvat laitteesta riippumattomasti. EMF:n metatiedostot koostuvat muuttuvapituisista tietueista kronologisessa järjestyksessä, jotka voivat renderöidä tallennetun kuvan sen jälkeen, kun se on jäsennetty millä tahansa tulostuslaitteella. Nämä vaihtelevan pituiset tietueet voivat olla suljettujen objektien määritelmiä, piirustuskomentoja ja grafiikkaominaisuuksia, jotka ovat tärkeitä kuvan hahmontamiseksi tarkasti. Kun laite avaa EMF-metatiedoston käyttämällä omaa grafiikkaympäristöään, alkuperäisen kuvan mittasuhteet, mitat, värit ja muut graafiset ominaisuudet pysyvät samoina avattavan laitteen alustasta riippumatta.

## Lyhyt historia ##

Vuonna 1990 Microsoft suunnitteli kuvatiedostomuodon Windows Metafile ([WMF](/image/wmf/)) Microsoft Windowsille. Windowsin metatiedostot ovat 16-bittisiä, jotka voivat sisältää joitain bittikarttakomponentteja.WMF voi koostua vektorigrafiikasta, ja se on tarkoitettu siirrettäväksi eri sovellusten välillä. Vuonna 1993 Win32/GDI julkisti Enhanced Metafilen (EMF), uudemman version, jossa on parannettu joustavuus ja skaalautuvuus. EMF:ää käytetään myös grafiikkakielen komentoina tulostinajurien suorittamiseen. Microsoft suosittelee nyt parannettua metatiedostomuotoa (EMF) Windows-muodon (WMF) sijaan. Kun Windows XP esiteltiin, Enhanced Metafile Format Plus (EMF+) -versio julkaistiin. Tämä uudempi versio löytää tiensä sarjoittamalla GDI+ API -kutsut, samoin WMF/EMF tallentaa kutsut GDI:lle. EMF:stä on olemassa gzip-pakattu versio, joka tunnetaan nimellä EMZ.

## EMF-metatiedostomuoto ##

Seuraavat ovat parannetun metatiedostomuodon olennaiset osat:

* EMR_HEADER (kuvan versio, koko, resoluutio luomishetkellä)

* Taulukko GDI-objekteille

* Varattu paletti (valinnainen)

* Metatiedostotietueet, jotka on järjestetty taulukkorakenteeseen (ominaisuusasetukset, määritellyt objektit, piirtokomennot)

* EMR_EOF-tietue (viimeinen tietue EMF-metatiedostossa)


## EMF-versiot ##
* **Alkuperäinen**: Alkuperäinen versio määrittää tietueen, joka on tarpeen alkuperäisen kuvan säilyttämiseksi ja sen laiteriippuvuuden säilyttämiseksi. Lisäksi tukee tietuetta, joka sisältää grafiikkaobjekteja ja komentoja piirtämistä varten.

* **Versio 1**: EMF:n toinen versio paransi joustavuutta ja laiteriippumattomuutta lisäämällä tietueen pikselimuodolle ja mahdollisuuden käyttää OpenGL-komentoa.

* **Versio 2**: Kolmas versio paransi tarkkuutta lisäämällä Metric-järjestelmän laitteen pintaetäisyyksien mittaamiseen, jolloin tietueesta tuli entistä skaalautuvampi.


## Enhanced Metafile Records ##

Metatiedostotietueet on järjestetty taulukon muotoon. Näillä tietueilla on ENHMETARECORD-rakenne ja vaihteleva pituus. ENHMETARECORD määrittää tiedot, jotka määrittelevät GDI-funktiot kuvan luomiseksi parannetulla metatiedostomuodolla. **ENHMETAHEADER** rakenne on aina ensimmäinen tietue tässä muodossa. Tämä EMF-otsikko sisältää seuraavat tiedot.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

Jokaisessa metatiedostossa tulee olla vähintään yksi EMF-tietue. Tietueesta toiseen siirtyminen riippuu EMF-tietueista, joten nämä tietueet on järjestettävä vierekkäin. Missä tahansa metatiedoston tietueessa paitsi EOF_record, kyseisen tietueen pituus määritetään siirtymään seuraavaan tietueeseen.

## Parannettu metatiedostojen luonti ##

**CreateEnhMetaFile**-toimintoa käytetään parannetun metatiedoston luomiseen. Tämän funktion argumentteja käytetään kuvan mittaamiseen ja tallentamiseen levylle/muistiin. Lisäksi tämä toiminto vaatii sen laitteen mitat, jossa kuva esiintyi ensimmäisenä (viitelaite) ja vertailulaitteen kontekstin (DC). Joten tämän DC:n käsittelyyn tarvittavien argumenttien on annettava kutsuttaessa **CreateEnhMetaFile**-toimintoa. Toiminnon syntaksi on seuraava:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** kahva referenssilaitteeseen.

**lptoFilename:** Osoitin tiedostonimeen.

**lprc:** Osoitin soikealle rakenteelle määrittää kuvan mitat millimetreinä.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## Parannetut metatiedostotoiminnot ##

Seuraavat ovat työt, jotka voidaan suorittaa käyttämällä parannetun metatiedoston kahvaa.

* Näytä ja muokkaa tallennettua kuvaa.

* Tuota parannettuja metatiedostokopioita.

* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* Kertaa paletin värit.


## Grafiikkaobjektit ##

Piirustus- ja maalausoperaatioissa graafisia objekteja voidaan luoda objektinluontitietueiden avulla ja tallentaa myöhempää käyttöä varten. EMR_SELECTOBJECT-tietue voi noutaa nämä grafiikkaobjektit toistolaitteen kontekstin avulla. Kynät, paletit, siveltimet, väriavaruudet, fontit ja varastoobjektit ovat joitain uudelleenkäytettäviä objektityyppejä.

## Tavujärjestys ##

Little-endian-muotoa käytetään tietojen tallentamiseen metatiedostotietueisiin.

## Versio ##

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. Laajennetut versiot sisältävät OpenGL-tietueet ja valinnaisen kuvaajan sisäiselle pikselimuodolle. Näytettäviä mittoja varten on lisätty mittausmahdollisuus millilitroina.

## Viitteet ##

* [Enhanced-Format metatiedostot | Microsoft Docs](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)

* [Enhanced Metafile Format and Specification](https://msdn.microsoft.com/en-us/library/cc230514.aspx)


