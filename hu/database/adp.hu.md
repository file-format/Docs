{
  "date" : "2021-09-06",
  "keywords" :[ "adp", "extension", "file", "file format", "Database File Type", "Database File Format", "Access Project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az ADP fájlformátumról és az API-król, amelyek ADP-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"ADP - Access Database File",
  "linktitle" : "ADP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Mi az ADP fájl?

Az .adp kiterjesztésű fájl egy Microsoft Access projektfájl, amely OLE DB komponens architektúrát használ, hogy közvetlen és hatékony kapcsolatot biztosítson a Microsoft SQL Server adatbázissal. Az ilyen fájlok nem tartalmazzák a tényleges táblákat, adatbázis-diagramokat vagy más adatbázis-elemeket. Az ADP fájlok az Access 2007 és 2010 programmal hozhatók létre. Az Access korábbi verzióival létrehozott fájlok az Access 2007 és 2010 programokkal is megnyithatók. Az ADP fájlok a Microsoft Access 365 használatával nyithatók meg.

## ADP fájlformátum - További információ

Az ADP-ként létrehozott Access-projektek lehetővé teszik az SQL-kiszolgáló objektumok, például táblák és nézetek tervezési módosításait. Lehetővé teszi az SQL-szolgáltatások, például adatbázis-diagramok, tárolt eljárások és a felhasználó által definiált függvények létrehozását, szerkesztését és használatát. Ez előnyt jelent az SQL szerver adatbázishoz való hivatkozással szemben, ahol nem módosítható a tervezés, és csak az SQL szerver tábláira és nézeteire tud hivatkozni.

### Adattípusok és diagramok támogatása

**Dátum/Idő adattípusok**

Az Access 2010 a következő új dátum/idő adattípusokat támogatja.

* IDŐ
* DÁTUM
* DATETIME2
* DATETIMEOFFSET

**Változó hosszúságú adattípusok**

A következő változó hosszúságú adattípusok használhatók az Access 2010 projektekben:

*VARBIN(MAX)
* VARCHAR(MAX)
* NVARCHAR(MAX)

## Hivatkozások

* [Access-projekt létrehozása](https://support.microsoft.com/en-us/office/create-an-access-project-89c48da0-55a4-45d4-9ee5-95f67383d4cb)

