{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML-fájlformátum - Haml-forráskódfájl",
  "description":"További információ a HAML-fájlformátumról és az API-król, amelyek HAML-fájlt hozhatnak létre és nyithatnak meg.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## Mi az a HAML fájl?

A HAML-fájl egy HTML-absztrakciós jelölőnyelvi fájl, amely [Haml](https://haml.info/) nyelven írt forráskódot tartalmaz. Használható az ERB (Ruby template scripts) helyettesítésére. A HAML-fájl sablon-forráskódot tartalmaz, amely egy webdokumentum HTML-kódjának előállításához használható. Az ERB-fájlok lecserélhetők, ha egyszerűen lecserélik ezeket a fájlokat az alkalmazás/nézetek mappában a Haml-re, a fájl kiterjesztésének megváltoztatásával. A HAML fájlok bármilyen szövegszerkesztővel megnyithatók, például Microsoft Notepad, Notepad++, Apple TextEdit,

## HAML fájlformátum

A HAML fájlok egyszerű szöveges fájlként lemezre mentett forrásfájlok. HAML szintaxisban írt kódot tartalmaz. A HAML a **<>** címkéket a **%** jelre cseréli, hogy egyszerűbbé és könnyebbé tegye a kódot. Az ERB fájlok beugróan cserélhetők HAML-lel, amint az a következő egyszerű példában látható.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML példa

A következő egy példa a Hello World HAML-re.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
amely a következő HTML-kimenetre jelenik meg.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Hivatkozások

* [HAML – Github](https://github.com/haml/haml)

