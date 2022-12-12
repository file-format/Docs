{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů KIT a rozhraních API, která mohou vytvářet a otevírat soubory KIT.",
  "title" :"Formát souboru KIT - soubor CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Co je soubor KIT?

Soubor s příponou .kit je soubor HTML vytvořený pomocí aplikace programovacího jazyka [CodeKit](https://codekitapp.com/). Kromě existujících [HTML](/cs/web/html/) souborů obsahuje `importy` a `proměnné`, takže je ideální pro statické weby. CodeKit kompiluje soubory KIT do HTML, které lze snadno použít jako statické soubory webových stránek.

## Formát souboru KIT

Soubory KIT jsou soubory HTML, které navíc obsahují importy a proměnné. Ty jsou uloženy jako prosté textové soubory a lze je otevřít pomocí libovolného textového editoru nebo editoru webových souborů.

### Import souborů KIT

Do souboru Kit lze importovat téměř jakýkoli typ souboru. Následuje syntaxe importu používaná k importu souborů do souboru .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Když je import přidán do souboru KIT a uložen, je nahrazen textem importovaného souboru. Místo @import můžete také použít @include.

### Vícenásobné importy v souboru KIT

Můžete také importovat více než jeden soubor najednou pomocí seznamu odděleného čárkami:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Reference

* [Co je sada?](https://codekitapp.com/help/kit/)

