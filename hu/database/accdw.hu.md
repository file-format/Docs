{
  "date" : "2021-08-30",
  "keywords" :[ "ACCDW", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ az ACCDW fájlformátumról és az API-król, amelyek ACCDW fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"ACCDW – Microsoft Access adatbázis-hivatkozási fájl",
  "linktitle" : "ACCDW",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-30"
}

## Mi az ACCDW fájl?

Az .accdw kiterjesztésű fájl egy Microsoft Access-szel létrehozott hivatkozásfájl, amely információkat tartalmaz az Access-adatbázisfájl, azaz az [ACCDB](/hu/database/accdb/) SharePoint-kiszolgálóról történő letöltéséhez szükséges hivatkozásról. Ez lehetővé teszi a felhasználók számára, hogy megosszák a távolról tárolt adatbázisfájlokat. Az ACCDW fájl megnyitása a hivatkozott ACCDB fájlt helyi másolatként letölti a felhasználó számítógépére. A letöltött fájlt a rendszer az alapértelmezett letöltési helyre menti, és a hozzá való navigációval érhető el. Általában ezeket a fájlokat a „SiteServer.accdb” néven töltik le és tárolják, amely az ügyféladatbázisokra utal.

## ACCDW fájlformátum - További információ

Az ACCDW-fájl egy XML-fájl, amely hivatkozást biztosít arra a SharePoint-webhelyre, ahol az Access Services található. Ez csak egy parancsikon, és internetkapcsolat szükséges a futtatáshoz. Online esetén a SharePoint helyben gyorsítótárazott, hogy lehetőséget biztosítson a későbbi offline módra.

## Hivatkozások

* [Access 2016 Specifications](https://support.microsoft.com/en-us/office/access-specifications-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Melyik Access-fájlformátumot használjam?](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

