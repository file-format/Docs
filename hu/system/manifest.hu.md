{
"dátum": "2023-03-07",
  "keywords": [
"manifest fájl",
"mi az a manifest fájl",
"fájl",
"manifest fájl kiterjesztése",
"kiterjesztés"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "MANIFEST Fájlformátum - Windows Alkalmazás Manifest fájl",
  "description":"További információ a MANIFEST formátumról és az API-król, amelyek MANIFEST fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle": "MANIFEST",
  "menu": {
    "docs": {
      "identifier": "system-manifest",
      "parent": "system"
}
},
"lastmod": "2023-03-07"
}

## Mi az a MANIFEST fájl?

A jegyzékfájl olyan fájl, amely egy szoftveralkalmazásról vagy -csomagról tartalmaz információkat. A fájl elnevezése általában .manifest fájlkiterjesztés. A jegyzékfájl információkat tartalmaz a csomagban található fájlokról, azok verziószámáról, valamint a csomag egyéb szoftverösszetevőktől való függőségeiről.

A jegyzékfájlokat általában a Windows platformon használják annak biztosítására, hogy a szoftveralkalmazások megfelelően telepítve és konfigurálva legyenek. Használhatók olyan dolgok meghatározására, mint például, hogy a megosztott könyvtárak mely verzióit kell használni, mely konfigurációs fájlokat kell belefoglalni, és mely rendszerleíró kulcsokat kell módosítani a telepítés során.

A Windowson kívül a jegyzékfájlok más környezetben is használhatók, például webalkalmazásokhoz vagy Android-alkalmazásokhoz. A jegyzékfájl konkrét formátuma és tartalma a platformtól és a csomagolt alkalmazástól függ.

## Több információ

A jegyzékfájlok XML formátumúak. Az XML egy széles körben használt jelölőnyelv strukturált dokumentumok és adatok létrehozására, és gyakran használják a szoftverfejlesztésben konfigurációk, beállítások és egyéb metaadatok leírására.

Szoftveralkalmazásokkal kapcsolatban a manifeszt XML-fájl jellemzően információkat tartalmaz az alkalmazás függőségeiről, verzióinformációiról és egyéb konfigurációs beállításairól. A fájl annak biztosítására szolgál, hogy az alkalmazás megfelelően legyen telepítve, és hogy minden szükséges összetevővel és erőforrással rendelkezzen a megfelelő futtatáshoz.

A jegyzék XML-fájl az alkalmazáscsomagban vagy külön fájlként is szerepelhet, amelyet a telepítés során tölt le. Általában ".manifest" fájlkiterjesztéssel nevezik el, és egy adott formátumot követ, amelyet az a platform vagy keretrendszer határoz meg, amelyre az alkalmazás épül.

A Microsoft .NET-keretrendszerben például egy manifest XML-fájlt használnak az alkalmazások függőségei és verzióinformációinak leírására, és általában az alkalmazás összeállításának részeként szerepel. A fájlt a Common Language Runtime (CLR) használja a betöltendő összeállítások megfelelő verziójának meghatározására és az alkalmazás megfelelő futásának biztosítására.

## Hivatkozások
* [Manifest fájl](https://en.wikipedia.org/wiki/Manifest_file)

