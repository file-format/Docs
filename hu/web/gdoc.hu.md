{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC fájl - Google Dokumentumok parancsikon",
  "description":"További információ arról, hogy mi az a GDOC-fájl és az API-k, amelyek GDOC-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Mi az a GDOC fájl?

A GDOC-fájl egy parancsikonfájl, amely a Google Drive-ban, egy felhőalapú dokumentumtárolási szolgáltatásban található fájlra mutat. Amikor a Google Drive kliens telepítve van egy számítógépre, és egy dokumentumot létrehoznak benne, a meghajtó létrehoz egy dokumentumot az online felhőtárolóban, és beírja ennek a dokumentumnak a [URL]-jét (/hu/web/url/) a helyi Google GDOC fájljába. Drive mappa. Ha erre a parancsikonfájlra duplán kattint, az alapértelmezett webböngésző megnyitja a dokumentumot a [URL](/hu/web/url/) helyről. Ha ezt a parancsikonfájlt áthelyezi ebből a mappából, az online dokumentumra mutató hivatkozás megszakad.

## GDOC fájlformátum - További információ

A GDOC fájl parancsikont tartalmaz a [JSON](/hu/web/json/) fájlformátumban írt online dokumentumhoz. A GDOC-fájlokat megnyitó böngésző beolvassa az URL-információkat, és megjeleníti a hivatkozott dokumentumot, feltéve, hogy a felhasználó bejelentkezett abba a Google-fiókba, ahol a dokumentumot tárolják. A GDOC fájlok nem tartalmazzák a dokumentum tartalmát.

### GDOC fájl példa

A GDOC fájl megnyitható egy szövegszerkesztőben, és a tartalma a következőképpen néz ki.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Amint látható, a tartalom JSON-ban van formázva, amely a dokumentum URL-címével és a kapcsolódó dokumentumazonosítóval rendelkezik.

## Hivatkozások

* [A Google Dokumentumok nem nyitja meg sem a gdoc, sem a docx fájlokat](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=hu )

