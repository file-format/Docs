{
  "date" : "2019-10-11",
  "keywords" :[ "pps-fil", "pps-filformat", "vad är en pps-fil", "fil", "pps exempel", "pps filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PPS - PowerPoint bildspelsfil",
  "description":"Läs mer om PPS-filformat och API:er som kan skapa och öppna PPS-filer.",
  "linktitle" : "PPS",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en PPS fil?

PPS, PowerPoint Slide Show, filer skapas med Microsoft PowerPoint för Slide Show syfte. Läsning och skapande av PPS-filer stöds av Microsoft PowerPoint 97-2003. Den senaste versionen av detta filformat är [PPSX ](/sv/presentation/ppsx/) som är baserat på Office OpenXML-standarder. PPS-filer kan fortfarande läsas av de senaste versionerna av Microsoft PowerPoint, men nyskapade filer kan bara sparas i PPSX-filformat. När en PPS-fil delas med en annan användare och öppnas, startar den som Powerpoint-show till skillnad från [PPT](/sv/presentation/ppt/) fil som öppnas i redigerbart läge.

## Filformat ##

PPS är ett binärt filformat som följer specifikationerna i [MS-PPT](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx) filformat dokumentera. Den består av ett antal strömmar för att representera den övergripande dokumentstrukturen och data. Dessa inkluderar:

* Aktuell användarström
* PowerPoint-dokumentström
* Bildström
* Sammanfattningsinformation och dokumentsammanfattningsinformation (valfritt)

Fullständig information om PPT-filformatet finns i MS-PPT-specifikationsdokumentet som även gäller för PPS.

## Referenser ##

* [PPT-filformatsspecifikationer](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office Common Data Types and Objects Structures](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office Document Cryptography Structure](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [PowerPoint-filformat](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

