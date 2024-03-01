{
  "date": "2019-12-10",
  "keywords": [
"XLM",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Microsoft Excel -makrotiedosto",
"Laskentataulukko"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tiedostomuoto-oppaasi tietääksesi, mikä on XLM-makrotiedosto ja API:t, jotka voivat luoda ja avata XLM-tiedostoja.",
  "title": "Mikä on XLM-tiedosto?",
  "linktitle": "XLM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-fim"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on XLM-tiedosto?

XLM, Excel-makrolle, on eräänlainen taulukkolaskentatiedosto, jota käytetään makrojen tallentamiseen. Sovelluksen näkökulmasta makro on joukko ohjeita, joita käytetään prosessien automatisointiin. Makroa käytetään tallentamaan vaiheet, jotka suoritetaan toistuvasti [XLS](/spreadsheet/xls/)-tiedostomuodolle, ja se helpottaa toimintojen suorittamista suorittamalla makro uudelleen. Makrot ohjelmoidaan Microsoftin Visual Basic for Applications (VBA) -ohjelmalla Excel-työkirjasta Visual Basic Editorin avulla, ja ne voidaan suorittaa/virheenkorjata suoraan sieltä.

## Lyhyt historia ##

Microsoft Excel supported programming of macros since its first public launch. The features of macros remained the same through subsequent versions fo Excel with extension as per new features. XLM was the default macro language for Excel through Excel 4.0. Excel 5.0 tallensi makrot oletusarvoisesti VBA:ssa, mutta versiossa 5.0 XLM-tallennus oli edelleen sallittu vaihtoehtona. Version 5.0 jälkeen tämä vaihtoehto poistettiin. Kaikki Excel-versiot, mukaan lukien Excel 2010, pystyvät suorittamaan XLM-makroa, vaikka Microsoft ei suosittele niiden käyttöä.

## Makron tallentaminen XLM-muodossa ##

Excel tarjoaa helppokäyttöiset vaiheet makron tallentamiseen. Se edellyttää, että sinulla on asennettuna kehittäjätyökalut, jotta voit työskennellä makrojen kanssa. Kun makrotallennus on käynnissä, se tallentaa jokaisen käyttäjän toiminnon toistettavaksi myöhemmin. Makrotallennus sisältää itse asiassa kaikki vaiheet, jotka käyttäjä suorittaa tallennuksen alkamisen jälkeen. Jos siis lihavoidaan ja kursivoitu solun sisältö ja asetat sen tekstin tasauksen sen jälkeen, kun makrotallennus on aloitettu, kaikki nämä komennot tallennetaan. Jokaiselle tallennetulle makrolle voidaan määrittää myös pikakuvake nopeaa toistoa varten myöhemmin. Makrotallennus luo VBA-koodin makron muodossa, jota voidaan muokata Visual Basic Editorilla (VBE).

## Excel-objektimalli ##

Makrot käyttävät VBA-rutiineja takanaan ja noudattavat [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) tätä tarkoitusta varten. Tämä malli tunnistaa laskentataulukon objektit vuorovaikutusta varten laskentataulukon kanssa käyttäjän määrittämien komentotyökalurivien, komentorivien tai viestiruutujen kautta. Esimerkiksi pääsy työkirjan ominaisuuksiin myönnetään Työkirja-objektilla. Samoin mallissa on Työkirja-objekti, joka toimii työkirjan laskentataulukoiden kanssa ohjelmallisesti.

## Makrot ja suojaus ##

VBA mahdollistaa pääsyn kaikille sovellusalueille sekä tiedostojärjestelmään ja voi olla myös vaarallinen. Tämä herättää huolta, kun jaat työkirjan sellaisen henkilön kanssa, joka voi suorittaa tiedoston lopussa. Eli Microsoft Excel varoittaa tällaisen tiedoston avaamisesta. Makrot voidaan sertifioida digitaalisella allekirjoituksella, jotta muut käyttäjät voivat varmistaa niiden luotettavuuden. Siten makrot voidaan ottaa käyttöön niiden lähteen tarkistamisen jälkeen.

## Viitteet ##

* [[MS-XLS] - Excelin binaaritiedostomuotorakenne](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [Makroohjelmointi](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)


