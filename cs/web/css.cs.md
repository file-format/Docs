---
date: 2019-10-11
keywords: css, .css, formát souboru css, jak otevřít soubory css, kaskádové styly
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formát souboru CSS
linktitle: CSS
description: "Přečtěte si o formátu souborů CSS a rozhraních API, která mohou vytvářet a otevírat soubory CSS."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## Co je soubor CSS? ##

CSS (Cascading Style Sheets) jsou soubory, které popisují, jak se prvky HTML zobrazují na obrazovce, na papíře atd. Pomocí HTML můžete mít buď vložené styly, nebo lze styly definovat v externí šabloně stylů. Pro vložení stylů, \ <style>\</style> používají se značky. Externí šablony stylů jsou uloženy v souborech s příponou .css. Pomocí externího CSS jej můžete zahrnout na více stránek HTML a aktualizovat styl těchto stránek. Dokonce i jediný soubor CSS lze použít ke stylování kompletní webové stránky.

## Stručná historie ##

CSS1 bylo vydáno v roce 1996 s Bertem Bosem jako spoluautorem. Pracovní skupina CSS začala pracovat na problémech, které nebyly řešeny v CSS1. To vedlo k vytvoření CSS2 v listopadu 1997, který byl publikován jako doporučení W3C dne 12. května 1998. Tato verze přidala podporu pro zařízení specifická pro média, jako jsou tiskárny, stahovatelná písma, tabulky a umístění prvků. V červnu 1999 se CSS3 stalo doporučením W3C. To rozdělilo dokumentaci do modulů, kde každý modul měl funkce rozšíření definované v CSS2.

## Jak používat CSS soubory ##

Chcete-li použít soubor CSS, zahrňte jej do sekce head dokumentu HTML. Pomocí značky odkazu zahrnete soubor, jak je znázorněno níže.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

atribut *href* značky odkazu obsahuje cestu k souboru CSS. Tímto způsobem se na dokument HTML použijí příslušné styly obsažené v přiloženém souboru CSS.

## Syntaxe CSS ##

Pravidlo CSS se skládá ze dvou komponent, selektoru a deklarace. Selektor ukazuje na prvek v dokumentu HTML. Může to být buď tag prvku, název třídy, id název, více tagů zobrazujících hierarchii atd. Deklarace obsahuje definici stylu obsahující vlastnost a hodnotu. Vlastnost identifikuje vlastnost prvku, kterou chcete změnit, a hodnota definuje jeho novou hodnotu. Každé pravidlo CSS může mít více deklarací. Následuje příklad pravidla CSS.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

Ve výše uvedeném příkladu máme **h1** jako selektor, který vybere všechny značky h1 v dokumentu HTML. Pravidlo má dvě deklarace, jednu pro váhu písma a druhou pro barvu. *font-weight* a *color* jsou vlastnosti a *700* a *forestgreen* jsou jejich hodnoty.

## Příklad použití CSS ##

Následuje ukázkový dokument HTML a šablona stylů použitá k jeho úpravě. Porovnávací obrázek je také přidán pro porovnání stylizovaných a prostých HTML dokumentů

### HTML dokument ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### šablona stylů CSS ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### Srovnání výstupů ###

Na levé straně obrázku se zobrazí dokument HTML bez použitých stylů a na pravé straně se zobrazí dokument HTML s použitými styly.

{{< figure src="../CssExample.jpg" alt="Příklad obrázku" >}}

## Reference ##

- [CSS - Wikipedie](https://en.wikipedia.org/wiki/CSS)

