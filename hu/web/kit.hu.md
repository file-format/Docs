{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a KIT fájlformátumról és az API-król, amelyek KIT fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"KIT fájlformátum - CodeKit fájl",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Mi az a KIT fájl?

A .kit kiterjesztésű fájl egy HTML-fájl, amely a [CodeKit](https://codekitapp.com/) programnyelvi alkalmazással jön létre. A meglévő [HTML](/hu/web/html/) fájlok mellett "importálást" és "változókat" is tartalmaz, így ideális statikus webhelyekhez. A CodeKit a KIT fájlokat HTML formátumba fordítja, amelyek könnyen használhatók statikus webhelyfájlokként.

## KIT fájlformátum

A KIT-fájlok olyan HTML-fájlok, amelyek ezenkívül importokat és változókat is tartalmaznak. Ezeket egyszerű szöveges fájlokként tárolják, és bármilyen szövegszerkesztővel vagy webes fájlszerkesztővel megnyithatók.

### KIT fájl importálása

Szinte bármilyen típusú fájl importálható egy Kit fájlba. A következő az importálási szintaxis, amellyel a fájlokat .kit fájlba importálhatja.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Amikor egy importálást hozzáadunk egy KIT-fájlhoz, és elmentjük, az lecserélődik az importált fájl szövegére. Használhatja az @include használatát is az @import helyett.

### Több importálás egy KIT-fájlban

Egyszerre több fájlt is importálhat egy vesszővel elválasztott lista használatával:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Hivatkozások

* [Mi a Kit?](https://codekitapp.com/help/kit/)

