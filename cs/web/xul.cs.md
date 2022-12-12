{
  "date" : "2021-05-24",
  "keywords" :["xul", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "Jazyk uživatelského rozhraní XML"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XUL - XML User Interface Language File",
  "description":"Další informace o formátu souboru XUL a rozhraních API, která mohou vytvářet a otevírat soubory XUL.",
  "linktitle" : "XUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Co je soubor XUL?

Soubor s příponou .xul ([XUL](https://wiki.mozilla.org/XUL:Home_Page) znamená jazyk uživatelského rozhraní XML) je soubor značkovacího jazyka založený na [XML](/cs/web/xml/) pro vytváření uživatelských rozhraní. Byl vyvinut společností Mozilla pro vývojáře, aby vytvořili prvky grafického uživatelského rozhraní podobné jiným značkovacím jazykům používaným pro tvorbu webových stránek. XUL široce používala Mozilla ve svém prohlížeči Firefox, kde používala kódovou základnu Mozilly. Vykreslování XUL se provádí pomocí
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). Vidlice Firefoxu jako Pale Moon, Basilisk a Waterfox si zachovávají podporu pro doplňky XUL. Soubory XUL jsou identifikovány typem MIME: application/vnd.mozilla.xul+xml.

## Formát souboru XUL

Soubory XUL jsou psány jako prostý text na základě formátu souboru XML a jsou vykreslovány pomocí enginu Gecko. Tři hlavní části struktury XUL jsou:

* `Obsah` – zahrnuje deklarace okna a prvky uživatelského rozhraní v nich obsažené.
* "Skin" - Zahrnuje všechny šablony stylů, obrázky a další soubory související s tématem. Vzhled okna je popsán v šablonách stylů.
* `Locale` - Text zobrazený v okně je uložen samostatně a uživatelé mohou používat více sad jazykových souborů.

### Příklad XUL

Následující příklad vytvoří tři tlačítka, která jsou naskládána na sebe ve svislém směru.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## Reference

* [XUL – podle Wikipedie](https://en.wikipedia.org/wiki/XUL)
* [Archivovaná dokumentace XUL – od Mozilly](https://wiki.mozilla.org/XUL:Home_Page)

