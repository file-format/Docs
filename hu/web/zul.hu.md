{
  "date" : "2021-05-24",
  "keywords" :["zul", "File", "Extension", "File Format", "File Extension", "open"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - ZK felhasználói felület fájl",
  "description":"További információ a ZUL fájlformátumról és az API-król, amelyek ZUL fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Mi az a ZUL fájl?

A .zul kiterjesztésű fájl a felhasználói felület jelölőnyelvével (ZUML) létrehozott webfájl, amely a felhasználói felület elemeinek definícióit tartalmazza. Az Ajax és a Java osztályok támogatják az [XML](/hu/web/xml/) alapú ZUML használatát a szerveroldali fájlok fejlesztéséhez. A ZUL fájlformátumot a ZK fejlesztette ki, egy UI keretrendszer, amely lehetővé teszi web- és mobilalkalmazások készítését a JavaScript vagy az AJAX ismerete nélkül.

## ZUL fájlformátum

A ZUL fájlok XML-alapúak, és különböző elemekből állnak a felhasználói felület felépítéséhez. A ZK betöltő minden XML-elemet felhasznál egy-egy összetevő létrehozásához. Az oldalelemek, például az oldal címe, leírása stb. általános feldolgozását a ZUML minden XML-feldolgozási utasítása írja le.

### ZUL példa

A ZUML kód következő példájában az első sor az oldal címét adja meg, a második sor egy gyökérkomponenst hoz létre címmel és szegéllyel, a harmadik sor pedig egy gombot címkével és eseményfigyelővel.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
A ZUL séma letölthető a http://www.zkoss.org/2005/zul/zul.xsd címről.
## Hivatkozások

* [ZUL – ZK által](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [ZUL-séma](http://www.zkoss.org/2005/zul/zul.xsd)

