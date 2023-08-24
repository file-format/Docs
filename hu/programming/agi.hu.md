{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI File - Asterisk Gateway Interface File Format",
  "description":"Tudjon meg többet arról, hogy mi az AGI fájlformátum, példákkal és API-kkal, amelyek AGI fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Mi az AGI fájl?

Az AGI-fájl a nyílt forráskódú telefonrendszer, az Asterisk által használt szkriptfájl. A folyamatok automatizálására és az Asterisk tárcsázási tervre használható információkat tartalmaz. Az AGI script fájlok használatával kapcsolatok létesíthetők relációs adatbázisokkal, mint például a PostgreSQL vagy a MySQL. Ezenkívül az AGI-szkriptek más külső erőforrások elérésére is használhatók. Az AGI-szkriptek átadhatják a tárcsázási terv vezérlését egy külső AGI-szkriptre, lehetővé téve az Asterisk számára, hogy összetett feladatokat hajtson végre.

## AGI fájlformátum - További információ

Az AGI szkriptfájlok szöveges fájlként kerülnek mentésre, és bármilyen szövegszerkesztőben megnyithatók módosítások elvégzéséhez.

### Az AGI kommunikáció szabványos mintája

Az AGI szkript betölti az Asterisk által neki küldött változókat és azok értékeit. E változók általános megjelenése a következő.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Ezeket a változókat az Asterisk által küldött üres sor követi, jelezve, hogy az AGI-szkript most átveheti a tárcsázási tervet.

### Programozási nyelv AGI Script Files számára

Az AGI-szkriptek általában Perl, [PHP](/hu/programming/php/), [C](/hu/programming/c/), Pascal vagy Bourne Shell nyelven írhatók.

## Hivatkozások

* [Asterisk AGI Script](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

