{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIM-filformat - OpenZIM-arkivfil",
  "description":"Läs mer om ZIM-filformat och API:er som kan skapa och öppna ZIM-filer.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Vad är ZIM fil? ##

Filer med filtillägget .zim är arkiv skapade för att lagra Wiki-innehåll offline. Det anses vara det mest lämpliga öppna filformatet för att lagra Wikipedia på en USB. Den lagrar webbplatsens innehåll i ett kompakt format. Dess namn kommer från "Zeno IMproved" som var det tidigare Zeno-filformatet. ZIM underhålls av projektet [openZIM ](https://openZim.org/) som sponsras av Wikimedia CH och stöds av Wikimedia Foundation. ZIM-filer kan öppnas av applikationer som Kiwix och ZIMReader. OpenZIM-projektet har varit värd för implementeringen av ZIM-filformatet på [Github](https://github.com/openzim) för bidrag från OpenSource-gemenskapen.

## Specifikationer för ZIM-filformat

ZIM-filformatet utvecklades ovanpå [Zeno-filformat](https://openzim.org/wiki/Zeno_file_format) och är inte bakåtkompatibelt. Formatspecifikationerna för ZIM-filformat är [tillgängliga online](https://openzim.org/wiki/ZIM_file_format) av openZIM för utvecklarens referens. OpenZIM har tillhandahållit C++-implementering med öppen källkod, [LibZim](https://openzim.org/wiki/Zimlib), för att läsa och skriva ZIM-filer.

Filformatet ZIM använder LZMA2-komprimering för att göra innehållet kompakt.

{{< figure src="../ZIM_File_Format.jpeg" alt="ZIM filformat" >}}


### ZIM Header

En ZIM-fil börjar med en rubrik som har offset 0. Alla beståndsdelar är baserade på little-endian och alla heltal är heltal utan tecken, dvs uint_16, uint_32, uint_64.

|Fältnamn |Typ| Offset| Längd| Beskrivning|
---|---|---|---|---|
|magicNumber| heltal| 0| 4| Magiskt nummer för att känna igen filformatet måste vara 72173914 (0x44D495A)|
|majorVersion| heltal| 4| 2| Huvudversionen av ZIM-filformatet (5 eller 6)|
|minorVersion| heltal| 6| 2| Mindre version av ZIM-filformatet|
|uuid| heltal| 8| 16| unikt ID för denna zim-fil|
|articleCount| heltal| 24| 4| totalt antal artiklar|
|clusterCount| heltal| 28| 4| totalt antal kluster|
|urlPtrPos| heltal| 32| 8| positionen för katalogpekarlistan sorterad efter URL|
|titlePtrPos| heltal| 40| 8| positionen för katalogpekarlistan sorterad efter Titel|
|clusterPtrPos| heltal| 48| 8| position för klusterpekarlistan|
|mimeListPos| heltal| 56| 8| position för MIME-typlistan (även rubrikstorlek)|
|huvudsida| heltal| 64| 4| huvudsida eller 0xffffffff om ingen huvudsida|
|layoutsida| heltal| 68| 4| layoutsida eller 0xffffffffff om ingen layoutsida|
|checksumPos| heltal| 72| 8| pekare till md5checksummen för denna fil utan själva checksumman. Detta pekar alltid 16 byte före slutet av filen.|

## Referenser ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

