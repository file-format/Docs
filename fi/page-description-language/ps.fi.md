{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PS tiedostomuoto",
  "description": "Opi PS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata PS-tiedostoja.",
  "linktitle": "PS",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-p-fis"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on .PS-tiedosto? ##

PostScript (PS) is a general-purpose page description language used in the business of desktop and electronic publishing. The main focus of PostScript (PS) is to facilitate the two-dimensional graphic design. Most languages require a distinct compilation stage before the code execution while Post Script (PS) format support a runtime straight forward interpretation. Its early version defines the graphical shapes, different text appearances and modelled imageries on printed pages or displayed pages, following the rules of Adobe imaging model. A program of PS is able to intercommunicate a document description between a composition and printing system keeping the device independent and high-level. Moreover this program is also capable of governing the appearance of text and graphics on a display.

PostScript page description is available to be rendered, displayed on printer and other output device with the help of the PostScript interpreter of the device. As the commands to print characters, graphical shapes and images are executed by interpreter, for that specific device, the high-level PostScript description converts into the low level raster data format. Generally, different applications such as illustrators, document composition systems and computer-aided design (CAD) are automated to generate PostScript page descriptions. Generally programmers have to write PostScript programs at the time of new applications creation.  However, a programmer can take advantage of the capabilities of the PostScript language that are not accessible in any application by writing a PS a program for that special situation.

## Lyhyt historia ##

The concept of the PostScript language was first introduced by John Warnock. In 1966 he was working on a project of New York Harbor. He was trying to develop an interpreter for a large three-dimensional graphics for the database of that project. For processing these graphics, John Warnock conceived the Design System language. Meanwhile Xerox PARC were looking for a standard means of defining page images for their first laser printer. Though Bob Sproull and William Newman in 1975-76 developed the Press format (data format) to drive laser printers yet a language was needed for more flexibility. In 1978 Warnock joined Martin Newell in Xerox PARC and rewrote the interpretive language, JaM which was later grew and extended into the Interpress language. Warnock founded Adobe Systems in December 1982 with Chuck Geschke, Doug Brotz, Ed Taft and Bill Paxton. They started working on a simpler language called PostScript similar to Interpress, which released commercially in 1984. Steve Jobs Applesta vieraili heidän luonaan ja neuvoi heitä mukauttamaan PostScriptin lasertulostimien ohjaamiseen.

Maaliskuussa 1985 ensimmäinen tulostin, jossa oli upotettu PostScript-tulkki, oli Applen LaserWriter, joka mullisti työpöytäjulkaisun (DTP). Tekninen vakavuus ja laaja saatavuus teki PostScriptistä suositun kielen pöytäkone- ja sähköiseen julkaisuun. Vuonna 1990 PostScript-kielen tulkki oli olennainen osa lasertulostimia.

## Pääpiirteet ##

The capabilities of the PostScript language to deal with interactive graphics and page description possess the following features:

**Muodot:** luonteeltaan mielivaltaisia, voivat koostua suorista viivoista, kaarevista, neliöistä ja kuutiokäyristä, jotka voivat olla sekä itsestään kulkevia että irrotettuja (osissa ja reikissä).

**Maalausoperaattorit:** sallivat minkä tahansa paksuuden, värin tai täytön muodon ääriviivat tai sallivat muodon piirtämisen leikkeenä minkä tahansa muun grafiikan rajaamisen mahdollistamiseksi.

**Värit:** ovat erilaisia, kuten harmaasävy, RGB, CMYK ja CIE. Erikoisvärejä mallinnetaan eri ominaisuuksiksi: spottivärit, värikartoitus, tasaiset varjostukset ja toistuvat kuviot.

**Teksti:** täysin integroitu grafiikkaan. Lisäksi Adobe-kuvausmalli mahdollistaa tekstin merkkien näyttämisen graafisina muotoina, joita kaikki normaalit grafiikkaoperaattorit voivat käyttää.

**Otekuvat**: poimittu alkuperäisistä lähteistä (skannatut valokuvat) tai voidaan tuottaa synteettisesti. PostScript-kieli tarjoaa monipuoliset keinot kuvien regeneroimiseen millä tahansa resoluutiolla ja eri värimallien mukaan tulostuslaitteella.

Yleiskäyttöinen ohjelmointikieli voi hyödyntää PostScript-kielen grafiikkaominaisuuksia upottamalla Ps:n puitteisiinsa. Primitiiviset tietotyypit, kuten numerot, merkit, taulukot ja merkkijonot; ohjausprimitiivit, kuten silmukat, menettelyt ja ehdolliset; ja jotkut epätavalliset ominaisuudet, kuten sanakirjat, on määritetty kielessä. Nämä ominaisuudet auttavat ohjelmoijia kirjoittamaan komentoja korkeamman tason toimintojen käynnistämiseksi. Nämä korkean tason toiminnot täyttävät monimutkaisten sovellusten tarpeet. Tällainen käytäntö on kompaktimpi ja tehokkaampi kuin kiinteän perustoimintosarjan käyttäminen.

PostScriptillä kirjoitettuja ohjelmia voidaan tuottaa, välittää ja tulkita ASCII-lähdetekstin muodossa. Koko kieli voidaan määritellä tulostettavien merkkien ja välilyöntien muodossa. Tämä esitys tukee ohjelmoijia luomaan, käsittelemään ja ymmärtämään kieltä helposti. Lisäksi tiedostojen tallennus ja siirto eri tietokoneiden ja käyttöjärjestelmien välillä säilyi kätevänä koneriippumattomuuden ansiosta.

Kielen binäärikoodatut muodot ovat mahdollisia, kun ohjelmalle taataan täysin läpinäkyvä viestintäpolku PostScript-tulkkiin. Adobe suosittelee tiukkaa yhtenäisyyttä PS-ohjelmien ASCII-esityksen kanssa asiakirjojen vaihtoa tai arkistointia varten.

## Versiot ##

PS(.ps) is the file extension for a PostScript document. UK National Archives categorize five chronological versions of PostScript file, defined in the DSC version: versions 1.0, 2.0, 2.1, 3.0, 3.1. Jokainen versio määrittelee tärkeät jäsentelykommentit. Encapsulated PostScript File (EPS) on PostScript-tiedoston erityinen alatyyppi, joka käyttää kieltä määrittämään suorakaiteen muotoisen grafiikan. PostScript Language Reference Manual kuvailee EPS:ää seuraavasti: Kapseloitu PostScript (EPS) -tiedosto on PostScript-ohjelma, joka kuvaa enintään yhden sivun muodossa, jonka muut sovellukset voivat tuoda sisällytettävään asiakirjaan. PostScript-asiakirjatiedosto voi kapseloida EPS-tiedoston siihen. PostScriptin lisäkäyttö mainitaan nimellä Display PostScript (DPS). DPS luo näyttögrafiikkaa grafiikkamoottorilla, joka hyödyntää PostScript-kuvausmallia ja -kieltä.

## Viitteet ##

* [PostScript-muotoperhe](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)


