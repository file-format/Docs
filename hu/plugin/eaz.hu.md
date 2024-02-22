{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ fájl - Mi az EAZ fájl és hogyan lehet megnyitni?",
  "description":"Ismerje meg az EAZ fájlformátumot és az API-kat, amelyek EAZ-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-huz"
}
},
  "lastmod" : "2023-12-23"
}

## Mi az EAZ fájl?

Az EAZ fájl egy bővítményfájl, amelyet az ArcGIS Explorer, az ESRI által a térképek felfedezésére, megjelenítésére és megosztására kifejlesztett ingyenes alkalmazás használja. Tartalmaz egy tömörített fájlarchívumot, amely egy [XML file](/web/xml/)-ot, egy lefordított kódot és a bővítményhez szükséges támogató fájlokat tartalmaz. Ezek a fájlok a szoftver alapfunkcióinak bővítésére szolgálnak új gombok, dokkolható ablakok és egyéb bővítmények beépítésével.

## EAZ fájlformátum - További információ

Az EAZ fájlok az ArcGIS Explorer SDK használatával jönnek létre, amely egy fejlesztőkészlet, amelyet az ArcGIS Exploreren belüli egyedi funkciók létrehozására terveztek. Ezek a fájlok [ZIP](/compression/zip/) tömörítést használnak a tartalmuk hatékony csomagolásához. Az archívum középpontjában az **Addins.xml** fájl a gyökérkönyvtárban található, és létfontosságú összetevőként szolgál, amely felvázolja és részletezi az EAZ-fájlba ágyazott különféle testreszabásokat.

Az Addins.xml fájl lényegében útitervként működik, betekintést nyújtva az EAZ fájl által az ArcGIS Explorerbe bevezetett speciális fejlesztésekbe, módosításokba és bővítményekbe. Ezen az átfogó struktúrán keresztül a fejlesztők új funkciókat, gombokat és dokkolható ablakokat integrálhatnak és zökkenőmentesen integrálhatnak, javítva az ArcGIS Explorer alkalmazás általános funkcionalitását és felhasználói élményét.

## Hivatkozások

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
