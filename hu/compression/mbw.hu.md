{
  "date" : "2021-05-28",
  "keywords" :[ "MBW", "MBRWizard", "file", "format", "extension", "compressed", "Firesage Solutions" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBW fájlformátum",
  "description":"További információ az MBW fájlformátumról és az API-król, amelyek MBW fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "MBW",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-05-28"
}

## Mi az MBW fájl? ##

Az .mbw kiterjesztésű fájl elsősorban a Firesage Solutions MBRWizard programjához kapcsolódik. A Master Boot Record Wizard (MBRWizard) biztonsági másolatot készít a számítógép MBR-éről, és elmenti azt egy MBW fájlba, amely szükség esetén visszaállítható. Az MBR és VBR (Volume Boot Record) másolatokon kívül ezek a fájlok GPT-t, felhasználó által definiált szektorokat vagy teljes lemezképeket tartalmazhatnak. Az MBR egy létfontosságú, 512 bájt hosszú rekord a merevlemezen, amely lehetővé teszi az operációs rendszer indítását. Tartalmazhatja a partíciós táblát és a lemez adathordozóját azonosító 32 bites aláírást is.

## Támogatott operációs rendszerek ##

Az MPW fájlformátumot csak a Windows operációs rendszer támogatja.

## Lehetséges problémák a ## fájl megnyitásakor

Ha nem tudja megnyitni és futtatni az MBW fájlt, az alábbi lehetséges problémák egyike lehet:

* Sérült MBW fájl
* Rossz hivatkozások az MBW fájlra a rendszerleíró bejegyzésekben
* Az MBW leírása törölve a Windows rendszerleíró adatbázisából
* Nemkívánatos kártevőt tartalmazó fertőzött fájl
* A számítógép nem rendelkezik elegendő hardvererőforrással az MBW fájl működtetéséhez
* A számítógép által az MBW fájl megnyitásához használt illesztőprogramok elavultak

