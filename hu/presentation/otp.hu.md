{
  "date" : "2021-01-21",
  "keywords" :[ "otp fájl", "otp fájlformátum", "mi az otp fájl", "fájl", "otp példa", "otp fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTP – OpenDocument bemutatósablon",
  "description":"További információ az OTP fájlformátumról és az API-król, amelyek OTP-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OTP",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2021-01-21"
}

## Mi az az OTP fájl?

Az .otp kiterjesztésű fájlok az alkalmazások által OASIS OpenDocument szabványos formátumban létrehozott prezentációs sablonfájlokat képviselik. Az ilyen fájl tartalma prezentációs információkat tartalmaz, szöveget, képeket, alakzatokat, multimédiás tartalmakat, átmenet-effektusokat és egyéb diaelemeket tartalmazó diák formájában. Ezek a sablonfájlok új bemutatók gyors létrehozására szolgálnak a sablonban tárolt stílusinformációk alapján. Az OTP-fájlok számos különböző alkalmazással hozhatók létre és menthetők, például az OpenOffice csomaghoz tartozó Impress-szel és a Microsoft PowerPoint-tal. Az OTP fájlformátum hasonló a Microsoft PowerPoint sablonfájljaihoz [.pot](/hu/presentation/pot/) és [.potx](/hu/presentation/potx/).

## OTP fájlformátum

Az OTP fájlformátum az OpenDocument szabványon alapul, amely támogatja a dokumentumok egyetlen XML-dokumentumként történő megjelenítését, valamint több aldokumentum egyetlen tömörített csomagban történő gyűjtését [ZIP](/hu/compression/zip/) formátumban. A fájl tartalma több, egymásba csomagolt xml-fájlban oszlik meg. Ez a több [XML](/hu/web/xml/) fájl információkat tartalmaz a dokumentum stílusáról, tartalmáról, metainformációiról és beállításairól, az alábbiak szerint.

* `content.xml` – Dokumentumtartalom és a tartalomban használt automatikus stílusok.
* `styles.xml` – A dokumentumtartalomban használt stílusok és magukban a stílusokban használt automatikus stílusok.
* `meta.xml` – A dokumentum metainformációi, például a szerző vagy az utolsó mentési művelet ideje.
* `settings.xml` – Alkalmazás-specifikus beállítások, például az ablak mérete vagy a nyomtató információi.

## Hivatkozások

* [OpenDocument – Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

