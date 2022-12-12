{
  "date" : "2021-05-24",
  "keywords" :["zul", "Soubor", "Přípona", "Formát souboru", "Přípona souboru", "otevřít"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZUL - Soubor uživatelského rozhraní ZK",
  "description":"Další informace o formátu souborů ZUL a rozhraních API, která mohou vytvářet a otevírat soubory ZUL.",
  "linktitle" : "ZUL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Co je soubor ZUL?

Soubor s příponou .zul je webový soubor vytvořený pomocí jazyka ZUML (User Interface Markup Language) a obsahuje definice prvků uživatelského rozhraní. Třídy Ajax a Java podporují použití ZUML založeného na [XML](/cs/web/xml/) pro vývoj souborů na straně serveru. Formát souboru ZUL byl vyvinut společností ZK, rozhraním uživatelského rozhraní, které vám umožňuje vytvářet webové a mobilní aplikace bez znalosti JavaScriptu nebo AJAX.

## Formát souboru ZUL

Soubory ZUL jsou založené na XML a skládají se z různých prvků pro vytvoření uživatelského rozhraní. Zavaděč ZK používá každý prvek XML k vytvoření komponenty. Celkové zpracování prvků stránky, jako je název stránky, popis atd., je popsáno v každé instrukci zpracování XML ZUML.

### Příklad ZUL

V následujícím příkladu kódu ZUML první řádek určuje název stránky, druhý řádek vytváří kořenovou komponentu s nadpisem a okrajem a třetí řádek vytváří tlačítko s popiskem a posluchačem události.

```
<?page title="Super Application"?>
<window title="Super Hello" border="normal">
    <button label="hi" onClick='alert("hi")'/>
```
Schéma ZUL lze stáhnout z http://www.zkoss.org/2005/zul/zul.xsd.
## Reference

* [ZUL – od ZK](https://www.zkoss.org/wiki/ZK_Getting_Started/Tutorial)
* [Schéma ZUL](http://www.zkoss.org/2005/zul/zul.xsd)

