{
  "date": "2019-10-11",
  "keywords": [
"htm",
"htm failą",
"htm failo formatas",
"htm failo tipas",
"failą",
"tipo",
"kas yra htm failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTM failo formatas",
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra HTM failas ir API, kurios gali juos sukurti ir atidaryti.",
  "linktitle": "HTM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-ltm"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra HTM failas?

Failai su plėtiniu **.htm** yra hiperteksto žymėjimo kalba, skirta kurti tinklalapius, kurie būtų rodomi žiniatinklio naršyklėse, pvz., Google Chrome, Internet Explorer, Firefox ir daugelyje kitų. Jame apibrėžiami žymėjimai kuriant statinius puslapius, kurie bus paskelbti žiniatinklyje (WWW), kad galėtų juos pasiekti. Šie žymėjimai nurodo naršyklėms, kaip rodyti tinklalapio turinį. Tokiuose puslapiuose gali būti paprasto teksto, vaizdų, nuorodų į kitus puslapius, vaizdo įrašų ir kitos žiniasklaidos informacijos. Kai tinklalapis yra paskelbtas, galite pažvelgti į už jo esantį žymėjimo kodą, peržiūrėdami jo puslapio šaltinį. Šiuolaikinės naršyklės leidžia apžiūrėti kiekvieną tinklalapio skiltį, kurioje yra išplėtotas kiekvienas HTM šaltinio poskyris arba žymėjimo elementas.

## Trumpa HTM istorija

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. 2000 m. jis taip pat tapo tarptautiniu standartu (ISO/IEC 15445:2000). 1999 m. buvo paskelbtas HTML 4.01. 2004 m. Web Hypertext Application Technology Working Group (WHATWG) pradėjo dirbti su HTML5 versija, kuri 2008 m. tapo bendru W3C pristatymu. Ji buvo baigta ir standartizuota 2014 m. spalio 28 d.

## HTML failo formatas

HTML 4 dokumentas susideda iš trijų dalių:

1. eilutė, kurioje yra HTML versijos informacija
1. deklaratyvioji antraštės dalis
1. turinys, kuriame yra tikrasis dokumento turinys. Turinys gali būti įgyvendintas elementu BODY arba FRAMESET elementu, kad korpusas būtų rėmeliuose

Kiekviena sekcija gali būti pirma arba po jos gali būti tarpai, naujos eilutės, skirtukai ir komentarai. Paprasto HTML dokumento pavyzdys yra toks, kaip parodyta toliau:

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

### Versijos informacija

Pirmoji kodo eilutė,<!DOCTYPE html> , vadinamas doctype deklaracija ir nurodo naršyklei, kurioje HTML versijoje puslapis parašytas. Priklausomai nuo HTML versijos, yra keletas skirtingų doctype deklaracijų, kurios įvardija dokumentui naudojamą dokumento tipo apibrėžimą (DTD). Kiekvienas DTD skiriasi nuo kitų savo palaikomais elementais ir skiriasi taip:

* HTML 4.01 Strict – apima visus elementus ir atributus, kurie nebuvo [nebenaudojami](https://www.w3.org/TR/html401/conform.html#deprecated) arba nerodomi rėmelių rinkinio dokumentuose

* HTML 4.01 Transitional – apima viską, kas yra griežtame DTD, ir nebenaudojamus elementus bei atributus (dauguma jų susiję su vaizdiniu pateikimu

* HTML 4.01 Frameset – apima viską, kas yra pereinamuosiuose DTD plius rėmuose


**HTML5** versijos informacija yra tokia, kaip nurodyta toliau.

```
<!DOCTYPE html>
```

### Antraštės informacija

HTML dokumento antraštėje gali būti daug HTML elementų, kurių naršyklė nepateikia. Tokie elementai yra arba metaduomenys, apibūdinantys informaciją apie puslapį, arba apima skyrius, naudojamas informacijai gauti iš išorinių išteklių, pvz., CSS stilių lapų arba JavaScript failų. Puslapio antraštę žymi \<head> žyma ir baigiasi \</head> žyma.

Norėdami nustatyti puslapio pavadinimą, \<title> elementas yra vienintelis, kurio reikia \<head> žymose. Tą patį naudoja paieškos sistemos, norėdami nustatyti puslapio pavadinimą.

### Kūno informacija

Tai yra pagrindinė failo skiltis, kurioje yra visas failo turinys, kurį pateikia naršyklės. HTML tekste gali būti žymenų, galinčių nurodyti įvairius žymų formos elementus. Jame gali būti kelių skirtingų tipų informacijos, pvz., teksto, vaizdų, spalvų, grafikos ir t. t. Be to, garso ir vaizdo elementai taip pat gali būti įterpti į HTML turinį, kad naršyklės galėtų juos pateikti. Esant šiuolaikinei vizualinio vaizdavimo stiliaus lapų programai, BODY pateikimo atributai, tokie kaip fono spalva, nuorodos spalva, teksto spalva ir kt., buvo nebenaudojami. Taigi tokius pačius efektus galima pasiekti naudojant stilių lenteles, kaip parodyta toliau:

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

Įterptuosius stiliaus lapus lengva įterpti, o norint greitai pritaikyti vaizdo efektus, išoriniai stilių lapai leidžia patogiau įdiegti vieną kartą ir pasiekti daugybę vietų.

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

### HTML elementai

Kaip minėta anksčiau, turinys HTML korpuse yra vaizduojamas žymomis, taip pat žinomomis kaip HTML elementai. Kiekviena žyma gali turėti papildomos informacijos atributų pavidalu, kurie parašyti kaip
```
<tag attribute1#"value1" attribute2#"value2">
```
nors nebūtina turėti atributų su kiekviena žyma. Jei atributai nepaminėti, kiekvienu atveju naudojamos numatytosios reikšmės. Toliau pateikiami keli elementų pavyzdžiai:

#### Antraštė

```
<head>
  <title>The Title</title>
</head>
```

#### Antraštės

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Pastraipos

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Nuorodos

* [Globali HTML dokumento struktūra](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


