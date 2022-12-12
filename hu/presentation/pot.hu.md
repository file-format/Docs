{
  "date" : "2019-10-11",
  "keywords" :[ "pot fájl", "pot fájl formátum", "mi az a pot fájl", "fájl", "pot példa", "pot fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POT – Microsoft PowerPOint sablonfájlformátum",
  "description":"További információ a POT fájlformátumról és az API-król, amelyek POT fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "POT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a POT fájl?

A .POT kiterjesztésű fájlok a PowerPoint 97-2003 verziói által létrehozott Microsoft PowerPoint sablonfájlokat képviselik. A Microsoft PowerPoint ezen verzióival létrehozott fájlok bináris formátumúak, összehasonlítva az Office OpenXML fájlformátumokkal, a PowerPoint magasabb verzióival. A létrehozott fájlok tehát felhasználhatók olyan prezentációk létrehozására, amelyek azonos elrendezéssel és más beállításokkal rendelkeznek, amelyek új fájlokra vonatkoznak. Ezek a beállítások tartalmazhatnak stílusokat, háttereket, színpalettát, betűtípusokat és alapértelmezett értékeket. Az ilyen fájlok a hivatalos használatra kész sablonfájlok létrehozása érdekében jönnek létre.

## Fájlformátum specifikációi ##

A POT-fájlformátumra vonatkozó fájlformátum-specifikációkat a Microsoft nem különíti el. A sablon formátuma azonban megegyezik a bináris [PPT](/hu/presentation/ppt/) fájlformátuméval, és szerkesztés céljából megnyitható az MS PowerPointban. A POT fájlt a következő HEX azonosító azonosítja:

```
D0 CF 11 E0 A1 B1 1A E1 00 00 00 00
```

A POT fájlformátumhoz társított MIME típusok a következők:

* application/vnd.ms-powerpoint [hivatalos]
* Application/mspowerpoint
* Application/x-mspowerpoint
* alkalmazás/powerpoint
* Application/x-powerpoint
* application/x-dos_ms_powerpnt
* alkalmazás/edény
* Application/x-soffic

## Referenciák ##

* [PPT fájlformátum specifikációi](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office Common Data Types and Objects Structures](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] – Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint fájlformátumok](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

