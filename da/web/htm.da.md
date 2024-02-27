{
  "date": "2019-10-11",
  "keywords": [
"htm",
"htm fil",
"htm filformat",
"htm filtype",
"fil",
"type",
"hvad er en htm-fil"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTM filformat",
  "description": "Din filformatguide for at lære, hvad der er en HTM-fil og API'er, der kan oprette og åbne dem.",
  "linktitle": "HTM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-dam"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en HTM fil?

Filer med filtypenavnet **.htm** repræsenterer Hypertext Markup Language til at skabe websider til visning i webbrowsere såsom Google Chrome, Internet Explorer, Firefox og en række andre. Den definerer opmærkningerne for at oprette statiske sider, der skal publiceres på World Wide Web (WWW) for adgang for andre. Disse markeringer fortæller browserne, hvordan de viser en websides indhold. Sådanne sider kan indeholde almindelig tekst, billeder, hyperlinks til andre sider, videoer og andre medieoplysninger. Når en webside er udgivet, kan du se opmærkningskoden bag den ved at se dens sidekilde. Moderne browsere gør det muligt at inspicere hver sektion af en webside, hvor hver underopdeling eller markup-element i HTM-kilden er uddybet.

## Kort historie om HTM

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. I 2000 blev det også en international standard (ISO/IEC 15445:2000). I 1999 blev HTML 4.01 udgivet. I 2004 begyndte Web Hypertext Application Technology Working Group (WHATWG) at arbejde på HTML5-versionen, som blev en fælles leverance med W3C i 2008. Den blev færdiggjort og standardiseret den 28. oktober 2014.

## HTML filformat

Et HTML 4-dokument består af tre dele:

1. en linje, der indeholder HTML-versionsoplysninger
1. en deklarativ overskriftssektion
1. en krop, som indeholder dokumentets faktiske indhold. Kroppen kan implementeres af BODY-elementet eller FRAMESET-elementet til at indeholde kroppen i rammer

Hver sektion kan føres eller efterfølges af hvide mellemrum, nye linjer, faner og kommentarer. Et eksempel på et simpelt HTML-dokument er som vist nedenfor:

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

### Versionsoplysninger

Den første kodelinje,<!DOCTYPE html> , kaldes en doctype-erklæring og fortæller browseren, hvilken version af HTML siden er skrevet i. Afhængigt af versionen af HTML er der en række forskellige doctype-erklæringer, der navngiver dokumenttypedefinitionen (DTD), der er i brug for dokumentet. Hver DTD adskiller sig fra andre i de elementer, den understøtter og adskiller sig som følger:

* HTML 4.01 Strict – inkluderer alle elementer og attributter, der ikke er blevet [forældet](https://www.w3.org/TR/html401/conform.html#deprecated) eller ikke vises i rammesætdokumenter

* HTML 4.01 Transitional - inkluderer alt i den strenge DTD plus forældede elementer og attributter (hvoraf de fleste vedrører visuel præsentation

* HTML 4.01 Frameset - inkluderer også alt i overgangs DTD plus frames


For **HTML5** er versionsoplysningerne blot som nævnt nedenfor.

```
<!DOCTYPE html>
```

### Overskriftsoplysninger

Header på et HTML-dokument kan indeholde en række HTML-elementer, som ikke gengives af browseren. Sådanne elementer er enten metadata, der beskriver information om siden eller inkluderer sektioner, der bruges til at hente information fra eksterne ressourcer som CSS-stylesheets eller JavaScript-filer. Overskriften på en side er repræsenteret af \<head> tag og slutter med \</head> tag.

Til indstilling af sidetitel skal \<title> element er det eneste, der kræves inden for \<head> tags. Det samme bruges af søgemaskiner til at identificere titlen på en side.

### Kropsoplysninger

Dette er hovedafsnittet i filen, der indeholder alt indholdet af filen, der gengives af browsere. Html body kan indeholde markeringer, der kan henvise til forskellige byggeklodser i form af tags. Det kan indeholde flere forskellige typer information som tekst, billeder, farver, grafik osv. Derudover kan lyd- og videoelementer også indlejres i html-tekst til gengivelse af browsere. I tilstedeværelsen af moderne stilarksapplikationer til visuel repræsentation er præsentationsattributterne for BODY, såsom baggrundsfarve, linkfarve, tekstfarve osv. blevet forældet. Således kan de samme effekter opnås ved at bruge stylesheets som vist nedenfor:

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

Inline-typografiark er nemme at integrere, og for hurtige anvendelser til de visuelle effekter gør eksterne typografiark det mere bekvemt at implementere én gang og få adgang mange steder.

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

### HTML-elementer

Som tidligere nævnt er indholdet i HTML Body repræsenteret af tags, også kendt som HTML-elementer. Hvert tag kan have yderligere information i form af attributter, som er skrevet som
```
<tag attribute1#"value1" attribute2#"value2">
```
selvom det ikke er nødvendigt at have attributter med hvert tag. Hvis attributter ikke er nævnt, anvendes standardværdier i hvert enkelt tilfælde. Følgende er nogle af elementerne eksempler:

#### Header

```
<head>
  <title>The Title</title>
</head>
```

#### Overskrifter

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Afsnit

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Referencer

* [The Global Structure of HTML-dokument](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


