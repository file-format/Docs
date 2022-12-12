{
  "date" : "2019-10-11",
  "keywords" :[ "dhtml", "soubor dhtml", "formát souboru dhtml", "typ souboru dhtml", "soubor", "typ", "co je soubor dhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DHTML - dynamický formát souboru HTML",
  "description":"Další informace o formátu souborů DHTML a rozhraních API, která mohou vytvářet a otevírat soubory DHTML.",
  "linktitle" : "DHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor DHTML?

Soubor s příponou .dhtml je dynamický [HTML](/cs/web/html/) soubor, který se používá k vytváření dynamického obsahu webové stránky. Webový prvek vytvořený v DHTML je řízen událostmi a nevyžaduje opětovné načítání stránky. Ve většině případů se soubor DHTML používá k vytvoření dynamického obsahu webové stránky, jako jsou rozevírací nabídky, plovoucí vrstvy, tlačítka pro přejetí myší a další dynamický obsah. Na dynamické html prvky narazíte téměř denně ve svém životě, když najedete myší na položku nabídky a otevře se další možnosti podnabídky. DHTML využívá webové technologie jako [HTML](/cs/web/html/), [Javascript](/cs/web/js/), HTML DOM, HTML události a [CSS](/cs/web/css/) k dosažení dynamické chování prvků.

## Formát souboru DHTML

Soubory DHTML jsou soubory ve formátu prostého textu, které obsahují kód DHTML pro implementaci dynamického chování webových prvků.


### DHTML DOM

Objektový model dokumentu DHTML (DOM) je založen na HTML DOM, což je stromová struktura s prvky, atributy a textem, jak je znázorněno na následujícím obrázku.

{{< figure src="../dhtml.png" alt="HTML DOM" >}}

Uzel `Dokument` lze použít k volání několika funkcí pro implementaci různých funkcí. Následující příklad jednoduše používá metodu document.write() JavaScriptu v DHTML.

```
<HTML>  
<head>  
<title>  
Method of a JavaScript  
</title>  
</head>  
<body>  
<script type="text/javascript">  
document.write("Hello World");  
</script>  
</body>  
</html>  
```

Tento kód zapíše text "Hello World" na výstup v prohlížeči.

### Události DHTML

|Č.č.|Událost|Výskyt|
---|---|---|
|1|onabort|Nastane, když uživatel přeruší načítání stránky nebo mediálního souboru.|
|2|onblur|Nastane, když uživatel opustí objekt HTML.|
|3|onchange|Nastane, když uživatel změní nebo aktualizuje hodnotu objektu.|
|4|onclick|Nastane nebo se spustí, když jakýkoli uživatel klikne na prvek HTML.|
|5|ondblclick|Nastane, když uživatel klikne na prvek HTML dvakrát současně.|
|6|onfocus|Nastane, když se uživatel zaměří na prvek HTML. Tato obsluha události funguje opačně než onblur.|
|7|onkeydown|Spustí se, když uživatel stiskne klávesu na zařízení s klávesnicí. Tato obsluha události funguje pro všechny klíče.|
|8|onkeypress|Spustí se, když uživatelé stisknou klávesu na klávesnici. Tato obsluha události se nespouští pro všechny klíče.|
|9|onkeyup|Nastane, když uživatel uvolní klávesu z klávesnice po stisknutí objektu nebo prvku.|
|10|onload|Nastane, když je objekt zcela načten.|
|11|onmousedown|Nastane, když uživatel stiskne tlačítko myši nad prvkem HTML.|
|12|onmousemove|Nastane, když uživatel přesune kurzor na objekt HTML.|
|13|onmouseover|Nastane, když uživatel přesune kurzor nad objekt HTML.|
|14|onmouseout|Nastane nebo se spustí, když se ukazatel myši přesune mimo prvek HTML.|
|15|onmouseup|Nastane nebo se spustí, když je tlačítko myši uvolněno nad prvkem HTML.|
|16|onreset|Slouží uživatelem k resetování formuláře.|
|17|onselect|Nastane po výběru obsahu nebo textu na webové stránce.|
|18|onsubmit|Spustí se, když uživatel po odeslání formuláře klikne na tlačítko.|
|19|onunload|Spustí se, když uživatel zavře webovou stránku.|

## Reference

* [Dynamic HTML – Wikipedia](https://en.wikipedia.org/wiki/Dynamic_HTML)

