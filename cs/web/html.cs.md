{
  "date" : "2019-10-11",
  "keywords" :[ "html", "soubor html", "formát souboru html", "typ souboru html", "soubor", "typ", "co je soubor html" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru HTML",
  "description":"Další informace o formátu souboru HTML a rozhraních API, která mohou vytvářet a otevírat soubory HTML.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor HTML?

HTML (Hyper Text Markup Language) je rozšíření pro webové stránky vytvořené pro zobrazení v prohlížečích. HTML, známé jako jazyk webu, se vyvinulo s požadavky na nové informace, které mají být zobrazeny jako součást webových stránek. Nejnovější varianta je známá jako HTML 5, která poskytuje velkou flexibilitu pro práci s jazykem. HTML stránky jsou buď přijímány ze serveru, kde jsou umístěny, nebo mohou být načteny z lokálního systému. Každá stránka HTML se skládá z prvků HTML, jako jsou formuláře, text, obrázky, animace, odkazy atd. Tyto prvky jsou reprezentovány značkami a několika dalšími, kde každá značka má začátek a konec. Může také vkládat aplikace napsané ve skriptovacích jazycích, jako je JavaScript a styly (CSS), pro celkovou reprezentaci rozvržení.

## Stručná historie ##

Od svého založení a první role byly specifikace HTML udržovány konsorciem World Wide Web Consortium (W3C) od roku 1996. V roce 2000 se také staly mezinárodním standardem (ISO/IEC 15445:2000). V roce 1999 bylo publikováno HTML 4.01. V roce 2004 začala pracovní skupina Web Hypertext Application Technology Working Group (WHATWG) pracovat na verzi HTML5, která se v roce 2008 stala společným výstupem s W3C. Byla dokončena a standardizována 28. října 2014.

## Struktura formátu souboru HTML ##

HTML 4 dokument se skládá ze tří částí:

1. řádek obsahující informace o verzi HTML
1. deklarativní záhlaví
1. tělo, které obsahuje skutečný obsah dokumentu. Tělo může být implementováno prvkem BODY nebo prvkem FRAMESET tak, aby obsahovalo tělo v rámcích

Každá sekce může být vedena nebo následována mezerami, novými řádky, kartami a komentáři. Příklad jednoduchého HTML dokumentu je uveden níže:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML File Format</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Informace o verzi ###

První řádek kódu, \<!DOCTYPE html> , se nazývá deklarace doctype a sděluje prohlížeči, ve které verzi HTML je stránka zapsána. V závislosti na verzi HTML existuje řada různých deklarací doctype, které pojmenovávají definici typu dokumentu (DTD) používanou pro daný dokument. Každý DTD se od ostatních liší v prvcích, které podporuje, a liší se následovně:

* HTML 4.01 Strict – zahrnuje všechny prvky a atributy, které nebyly [zastaralé](https://www.w3.org/TR/html401/conform.html#deprecated) nebo se neobjevují v dokumentech sady rámců
* HTML 4.01 Transitional – zahrnuje vše v přísném DTD plus zastaralé prvky a atributy (z nichž většina se týká vizuální prezentace
* HTML 4.01 Frameset – zahrnuje také vše v přechodných DTD plus rámcích

Pro **HTML5** jsou informace o verzi jednoduše takové, jak je uvedeno níže.

```
<!DOCTYPE html>
```

### Informace v záhlaví HTML ###

Záhlaví dokumentu HTML může obsahovat řadu prvků HTML, které prohlížeč nevykresluje. Takovými prvky jsou buď metadata, která popisují informace o stránce, nebo zahrnují části, které se používají k načítání informací z externích zdrojů, jako jsou šablony stylů CSS nebo soubory JavaScriptu. Záhlaví stránky představuje tag head.

Pro nastavení názvu stránky je prvek **title** jediný, který je vyžadován v rámci<head> značky. Totéž používají vyhledávače k identifikaci názvu stránky.

### Informace o těle HTML ###

Toto je hlavní část v souboru, která obsahuje veškerý obsah souboru, který vykreslují prohlížeče. Html tělo může obsahovat značky, které mohou odkazovat na různé stavební bloky ve tvaru značek. Může obsahovat několik různých typů informací, jako je text, obrázky, barvy, grafika atd. Kromě toho lze do těla html vložit zvukové a obrazové prvky pro vykreslení pomocí prohlížečů. V přítomnosti moderní aplikace šablon stylů pro vizuální reprezentaci byly atributy prezentace BODY, jako je barva pozadí, barva odkazu, barva textu atd., zastaralé. Pomocí šablon stylů lze tedy dosáhnout stejných efektů, jak je uvedeno níže:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Inline Style Sheets referencing</TITLE>
 <STYLE type#"text/css">
  BODY { background: white; color: black}
  A:link { color: red }
  A:visited { color: maroon }
  A:active { color: fuchsia }
 </STYLE>
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>
```

Vložené šablony stylů se snadno vkládají a pro rychlé aplikace vizuálních efektů usnadňují externí šablony stylů jednorázové nasazení a přístup na mnoha místech.

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
<HEAD>
 <TITLE>Linking to External style sheets</TITLE>
 <LINK rel#"stylesheet" type#"text/css" href#"smartstyle.css">
</HEAD>
<BODY>
  ... document body...
</BODY>
</HTML>

```

### Prvky HTML ###

Jak již bylo zmíněno dříve, obsah v těle HTML je reprezentován značkami, také známými jako Html Elements. Každá značka může mít další informace ve formě atributů, které se zapisují jako<tag attribute1#"value1" attribute2#"value2"> , i když není nutné mít atributy u každé značky. Pokud atributy nejsou uvedeny, použijí se v každém případě výchozí hodnoty. Níže jsou uvedeny některé příklady prvků:

#### Záhlaví ####

```
<head>
  <title>The Title</title>
</head>
```

#### Nadpisy ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Odstavce ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Reference ##

* [Globální struktura dokumentu HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

