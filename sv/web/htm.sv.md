{
  "date" : "2019-10-11",
  "keywords" :[ "htm","htm-fil", "htm-filformat", "htm-filtyp", "fil", "typ", "vad är en htm-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTM-filformat",
  "description" :"Din filformatguide för att lära dig vad en HTM-fil och API:er är som kan skapa och öppna dem.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en HTM fil?

Filer med tillägget **.htm** representerar Hypertext Markup Language för att skapa webbsidor för visning i webbläsare som Google Chrome, Internet Explorer, Firefox och ett antal andra. Den definierar markeringarna för att skapa statiska sidor som ska publiceras på World Wide Web (WWW) för åtkomst av andra. Dessa markeringar talar om för webbläsarna hur de ska visa en webbsidas innehåll. Sådana sidor kan innehålla vanlig text, bilder, hyperlänkar till andra sidor, videor och annan medieinformation. När en webbsida publiceras kan du ta en titt på uppmärkningskoden bakom den genom att se sidans källa. Moderna webbläsare tillåter att inspektera varje sektion av en webbsida där varje underavdelning eller uppmärkningselement i HTM-källan är utarbetad.

## Kort historia om HTM

Sedan starten och första roll ut har HTML-specifikationerna underhållits av World Wide Web Consortium (W3C) sedan 1996. År 2000 blev det också en internationell standard (ISO/IEC 15445:2000). 1999 publicerades HTML 4.01. 2004 började Web Hypertext Application Technology Working Group (WHATWG) arbeta på HTML5-versionen som blev en gemensam leverans med W3C 2008. Den färdigställdes och standardiserades den 28 oktober 2014.

## HTML-filformat

Ett HTML 4-dokument består av tre delar:

1. en rad som innehåller HTML-versionsinformation
1. en deklarativ rubrik
1. en kropp, som innehåller dokumentets faktiska innehåll. Kroppen kan implementeras av BODY-elementet eller FRAMESET-elementet för att innehålla kroppen i ramar

Varje avsnitt kan ledas eller följas av blanksteg, radnyheter, flikar och kommentarer. Ett exempel på ett enkelt HTML-dokument är som visas nedan:

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

### Versionsinformation

Den första kodraden,<!DOCTYPE html> , kallas en doctype-deklaration och talar om för webbläsaren vilken version av HTML sidan är skriven i. Beroende på HTML-versionen finns det ett antal olika doctype-deklarationer som namnger dokumenttypsdefinitionen (DTD) som används för dokumentet. Varje DTD skiljer sig från andra i de element den stöder och skiljer sig enligt följande:

* HTML 4.01 Strict – inkluderar alla element och attribut som inte har [fatats ut](https://www.w3.org/TR/html401/conform.html#deprecated) eller som inte visas i ramuppsättningsdokument
* HTML 4.01 Transitional - inkluderar allt i den strikta DTD plus föråldrade element och attribut (varav de flesta gäller visuell presentation
* HTML 4.01 Frameset - inkluderar allt i övergångs DTD plus ramar också

För **HTML5** är versionsinformationen helt enkelt som nämns nedan.

```
<!DOCTYPE html>
```

### Rubrikinformation

Rubriken i ett HTML-dokument kan innehålla ett antal HTML-element som inte renderas av webbläsaren. Sådana element är antingen metadata som beskriver information om sidan eller inkluderar avsnitt som används för att hämta information från externa resurser som CSS-formatmallar eller JavaScript-filer. Sidhuvudet representeras av \<head> tagga och slutar med \</head> märka.

<html>För att ställa in sidtitel, \<title> element är det enda som krävs inom \<head>-taggarna. Detsamma används av sökmotorer för att identifiera titeln på en sida. </html>

### Kroppsinformation

Detta är huvudsektionen i filen som innehåller allt innehåll i filen som renderas av webbläsare. Html-kroppen kan innehålla markeringar som kan referera till olika byggstenar i form av taggar. Den kan innehålla flera olika typer av information som text, bilder, färger, grafik, etc. Dessutom kan ljud- och videoelement också bäddas in i html-kroppen för rendering av webbläsare. I närvaro av moderna stilarksapplikationer för visuell representation, har presentationsattributen för BODY såsom bakgrundsfärg, länkfärg, textfärg, etc. fasats ut. Således kan samma effekter uppnås med hjälp av stilmallar som visas nedan:

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

Inline stilmallar är lätta att bädda in och för snabba tillämpningar av visuella effekter gör externa stilmallar det mer bekvämt att distribuera en gång och komma åt på många ställen.

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

### HTML-element

Som nämnts tidigare representeras innehållet i HTML Body av taggar, även kända som HTML-element. Varje tagg kan ha ytterligare information i form av attribut som skrivs som
```
<tag attribute1#"value1" attribute2#"value2">
```
även om det inte är nödvändigt att ha attribut med varje tagg. Om attribut inte nämns används standardvärden i varje fall. Följande är några av elementexemplen:

#### Rubrik

```
<head>
  <title>The Title</title>
</head>
```

#### Rubriker

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Stycken

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Referenser

* [The Global Structure of HTML-dokument](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

