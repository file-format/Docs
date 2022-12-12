{
  "date" : "2021-05-24",
  "keywords" :["xht", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "rozšířený hypertextový značkovací jazyk"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHT",
  "description":"Další informace o formátu souboru XHT a rozhraních API, která mohou vytvářet a otevírat soubory XHT.",
  "linktitle" : "XHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Co je soubor XHT?

Soubor s příponou .xht je webový soubor spojený s typem souboru [XHTML](/cs/web/xhtml/) (Extended Hypertext Markup Language), který sám o sobě je souborem značek založených na [XML](/cs/web/xml/). Oba tyto soubory jsou podobné HTML, ale mají přísnější syntaxi podobnou XML. Soubory XHT jsou navrženy tak, aby byly strukturovanější, vyžadují méně skriptování a jsou generické kromě použití stávajících možností XML.

## Formát souboru XHT

Soubor XHT je vytvořen a uložen jako prostý textový soubor s kódováním UTF-8 ve výchozím nastavení. Obsahuje kompletní zdrojový kód dokumentu XHTML, který lze otevřít a upravit pomocí libovolného textového editoru, který podporuje kódování Unicode. Kromě textových editorů je formát souboru XHT srozumitelný pro většinu moderních webových prohlížečů a lze jej pomocí nich otevřít.

## Příklad XHT

Následující příklad dokumentu XHT definuje deklarace XML.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

## Reference ##

* [Historie XHTML: Od 90. let do dneška](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

