{
  "date" : "2019-10-11",
  "keywords" :[ "html","html-fil", "html-filformat", "html-filtyp", "fil", "typ", "vad är en html-fil" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTML-filformat",
  "description":"Läs mer om HTML-filformat och API:er som kan skapa och öppna HTML-filer.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en HTML-fil?

HTML (Hyper Text Markup Language) är tillägget för webbsidor som skapats för visning i webbläsare. HTML, som är känt som webbens språk, har utvecklats med krav på nya informationskrav som ska visas som en del av webbsidor. Den senaste varianten är känd som HTML 5 som ger mycket flexibilitet för att arbeta med språket. HTML-sidor tas antingen emot från servern, där dessa är värd, eller kan också laddas från det lokala systemet. Varje HTML-sida består av HTML-element som formulär, text, bilder, animationer, länkar etc. Dessa element representeras av taggar och flera andra där varje tagg har start och slut. Den kan också bädda in applikationer skrivna i skriptspråk som JavaScript och Style Sheets (CSS) för övergripande layoutrepresentation.

## Kortfattad bakgrund ##

Sedan starten och första roll ut har HTML-specifikationerna underhållits av World Wide Web Consortium (W3C) sedan 1996. År 2000 blev det också en internationell standard (ISO/IEC 15445:2000). 1999 publicerades HTML 4.01. 2004 började Web Hypertext Application Technology Working Group (WHATWG) arbeta på HTML5-versionen som blev en gemensam leverans med W3C 2008. Den färdigställdes och standardiserades den 28 oktober 2014.

## HTML-filformatstruktur ##

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

### Versionsinformation ###

Den första kodraden, \<!DOCTYPE html> , kallas en doctype-deklaration och talar om för webbläsaren vilken version av HTML sidan är skriven i. Beroende på HTML-versionen finns det ett antal olika doctype-deklarationer som namnger dokumenttypsdefinitionen (DTD) som används för dokumentet. Varje DTD skiljer sig från andra i de element den stöder och skiljer sig enligt följande:

* HTML 4.01 Strict – inkluderar alla element och attribut som inte har [fatats ut](https://www.w3.org/TR/html401/conform.html#deprecated) eller som inte visas i ramuppsättningsdokument
* HTML 4.01 Transitional - inkluderar allt i den strikta DTD plus föråldrade element och attribut (varav de flesta gäller visuell presentation
* HTML 4.01 Frameset - inkluderar allt i övergångs DTD plus ramar också

För **HTML5** är versionsinformationen helt enkelt som nämns nedan.

```
<!DOCTYPE html>
```

### HTML Header Information ###

Rubriken i ett HTML-dokument kan innehålla ett antal HTML-element som inte renderas av webbläsaren. Sådana element är antingen metadata som beskriver information om sidan eller inkluderar avsnitt som används för att hämta information från externa resurser som CSS-formatmallar eller JavaScript-filer. Sidhuvudet representeras av head-taggen.

För att ställa in sidrubrik är elementet **title** det enda som krävs inom<head> taggar. Detsamma används av sökmotorer för att identifiera titeln på en sida.

### HTML Body Information ###

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

Inline-stilmallar är lätta att bädda in och för snabba tillämpningar av visuella effekter gör externa stilmallar det bekvämare att distribuera en gång och komma åt på många ställen.

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

### HTML-element ###

Som nämnts tidigare representeras innehållet i HTML Body av taggar, även kända som HTML-element. Varje tagg kan ha ytterligare information i form av attribut som skrivs som<tag attribute1#"value1" attribute2#"value2"> , även om det inte är nödvändigt att ha attribut med varje tagg. Om attribut inte nämns används standardvärden i varje fall. Följande är några av elementexemplen:

#### Rubrik ####

```
<head>
  <title>The Title</title>
</head>
```

#### Rubriker ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Stycken ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Referenser ##

* [The Global Structure of HTML-dokument](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

