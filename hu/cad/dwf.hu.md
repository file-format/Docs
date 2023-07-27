{
  "date" : "2020-03-16",
  "keywords" :[ "DWF", "Fájlformátum", "Megnyitás", "Olvasás", "Létrehozás", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"További információ a DWF fájlformátumról és az API-król, amelyek DWF-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"DWF fájlformátum",
  "linktitle" : "DWF",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## Mi az a DWF fájl?

A Design Web Format (DWF) tömörített formátumú 2D/3D rajzot jelent a tervfájlok megtekintésére, áttekintésére vagy nyomtatására. Grafikát és szöveget tartalmaz a tervezési adatok részeként, és csökkenti a fájl méretét tömörített formátuma miatt. A csökkentett fájlméret hatékonyabbá teszi a gazdag tervezési adatok terjesztését és kommunikációját. A DWF-nek nem kell tudnia a címzettnek az eredeti rajzot létrehozó CAD-szoftver használatáról. A DWF fájlformátum tartalma lehet egyszerű, és csak egyetlen lapot tartalmazhat, vagy elég összetett ahhoz, hogy betűtípusokat, színeket és képeket tartalmazzon.

## Rövid története ##

Az Autodesk 1995-ben vezette be a DWF fájlformátumot a Netscape Navigation beépülő modul, a WHIP részeként. A formátum a csak 2D formátumból fejlődött ki, hogy az idő múlásával 3D tartalmakat is tartalmazzon. Sok harmadik féltől származó alkalmazás is használja ezt a formátumot.

## DWF fájlformátum ##

A DWF egy nyílt, biztonságos formátum, amelyet kifejezetten gazdag mérnöki tervezési adatok megosztására terveztek. Ez független a tervezési adatok létrehozásához használt eredeti alkalmazásszoftvertől, hardvertől és operációs rendszertől. Ez lehetővé teszi, hogy a csapattagok, akik nem használnak CAD-alkalmazásokat, részt vegyenek a digitális folyamatokban épület-, GIS- vagy terméktervek megtekintésével. A DWF-fájlarchívum több XML- és bináris fájlból áll, amelyek egy [ZIP](/hu/compression/zip/) tömörítéssel létrehozott tömörített archívumba vannak csomagolva. A DWF fájl kiterjesztését átnevezheti ZIP-re, és megtekintheti a fájl tartalmát. A DWF-csomag sokféle tervezési adatot tartalmazhat, például 2D-s grafikát, 3D-s grafikát, csomag- és szakasz-metaadatokat és egyéb erőforrás-fájlokat.

**DWF-metaadatfájlok** – XML-fájlok, amelyek a metaadatokra és a szerkezetre (szerző, cím, létrehozási idő, szakaszfüggőségek, szakaszok sorrendje, erőforrásfájl-leírások, szerepek, mime-típusok stb.) és a szakaszra (oldalra) vonatkozó információkat tartalmaznak. információk, tervezési metaadatok stb.). A szerkezeti metaadatok logikai objektumok létrehozására szolgálnak (fájlgyűjtemények egy rész vagy oldal ábrázolására stb.).

**Forrásfájlok** – média- vagy egyéb tartalomfájlok, amelyekre a csomag/szakasz metaadataiból hivatkoznak, és általában a tervezési adatok különböző formátumú megjelenítései (ZGL, W2D, [JPG](/hu/image/jpeg/), [PNG]). (/hu/image/png/), AVI, XML, [TXT](/hu/word-processing/txt/), [DOC](/hu/word-processing/doc/) stb.)

### Fájlformátum részletei ###

A DWF-fájlok három fő részre vannak rendezve, az alábbiak szerint.

* Fájlazonosító fejléc
* Fájl adatblokk
* Fájllezáró trailer

#### Fájlazonosító fejléc ####

A fájlazonosító fejléc lehetővé teszi a DWF-fájlok alkalmazások általi azonosítását. Azt is azonosítja, hogy a DWF specifikációk melyik verzióját használták a fájl kódolásához. Ez egy 12 bájtos fejléc, amely a következőképpen van elrendezve:


|Bájt|0|1|2|3|4|5|6|7|8|9|10|11
--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- | --- |--- |
|Karakter|(|D|W|F|(szóköz)|V|0|0|.|3|0|)

Íme a táblázat összefoglalása:

* A fejléc első hat bájtja mindig ASCII karaktereket jelent "(DWF V"
* A következő 5 bájt információkat tartalmaz a verziószámról, pl. "00.30" a formátum fő- és mellékverziójának értékével együtt

A DWF-fájlt létrehozó alkalmazásoknak a lehető legalacsonyabb verziószámot kell megadniuk, amelyet az olvasó alkalmazásnak támogatnia kell az adatok megfelelő felhasználásához.

#### Fájl adatblokk ####

A fájl adatblokk a DWF-fájl 13. bájtjával kezdődik, és műveleti kód és operandus párok sorozata, a következő táblázat szerint.

|1.mező|2.mező|3.mező|4.mező|5.mező|5.mező
--- | --- |--- | --- |--- | --- |
|opcode|operand|opcode|operand|opcode|operand

A DWF-fájlok opkód-operandus párokat tartalmazhatnak olvasható ASCII-ként, valamint bináris kódként vagy ezek keverékeként. Minden DWF-műveletnek van olvasható ASCII műveletkód/operandus formája, és a legtöbb műveletnek van kódolt bináris műveletkód/operandus formája is. Az opkódok egyetlen bájtban vannak, így több mint 200 műveletet tesz lehetővé. A kiterjesztett ASCII és a kiterjesztett bináris kivételes esetek. Az Opcodes értéke 0 és 255 között lehet, néhány kivételtől eltekintve. A két speciális kiterjesztett ASCII és kiterjesztett bináris műveleti kód kivételével a fájlolvasónak tudnia kell az operandus hosszának kiszámítását.

##### Tiltott opkódok #####

Az alábbi ASCII-reprezentációk nem használhatók műveleti kódként:

A következő ASCII-reprezentációk nem használhatók műveleti kódként:

* Szóköz (0x20)
* Tab (0x09)
* Kötőjel (0x2D)
* ASCII számjegyek 0-9 (0x30 - 0x39)
* Kocsi vissza (0x0D)
* Soremelés (0x0A)
* Egyetlen idézőjel (0x27)
* Dupla idézőjel (0x22)
* Időszak (0x2E)
* Zárójel (0x28 és 0x29)
* Göndör zárójelek (0x7B és 0x7D)
* Szögletes zárójelek (0x5B és 0x5D)
* Fordított perjel (0x5C)

#### Fájlmegszakító előzetes ####

A DWF fájllezáró előzetese egyszerűen egy speciális műveleti kód, amely a fájl végét jelzi. Egyes alkalmazások nem DWF-adatokat tárolhatnak a befejezési műveleti kódot követően. Az előzetes az alábbiak szerint néz ki:


|Bájt|0|1|2|3|4|5|6|7|8|9
---|---|---|---|---|---|---|---|---|---|---|
|Karakter|(|E|n|d|0|f|D|W|F|)

## Hivatkozások ##

* [DWF – a Wikipedia által](https://en.wikipedia.org/wiki/Design_Web_Format)
* [WHIP adatformátum](http://paulbourke.net/dataformats/whip/)
* [https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1](https://learn.microsoft.com/en-us/archive/blogs/opc/adventures-in-packaging-episode-1)

