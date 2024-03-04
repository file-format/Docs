{
  "date": "2019-10-11",
  "keywords": [
"html",
"html failą",
"html failo formatas",
"html failo tipas",
"failą",
"tipo",
"kas yra html failas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTML failo formatas",
  "description": "Sužinokite apie HTML failo formatą ir API, kurios gali kurti ir atidaryti HTML failus.",
  "linktitle": "HTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-htm-ltl"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra HTML failas?

HTML (Hyper Text Markup Language) yra tinklalapių plėtinys, sukurtas rodyti naršyklėse. Žinomas kaip žiniatinklio kalba, HTML išsivystė atsižvelgiant į naujus informacijos reikalavimus, kurie turi būti rodomi kaip tinklalapių dalis. Naujausias variantas žinomas kaip HTML 5, suteikiantis daug lankstumo dirbant su kalba. HTML puslapiai gaunami iš serverio, kuriame jie yra talpinami, arba gali būti įkeliami ir iš vietinės sistemos. Kiekvienas HTML puslapis yra sudarytas iš HTML elementų, tokių kaip formos, tekstas, vaizdai, animacija, nuorodos ir kt. Šie elementai yra žymimi žymomis ir keletu kitų, kur kiekviena žyma turi pradžią ir pabaigą. Jis taip pat gali įterpti programas, parašytas skriptų kalbomis, pvz., JavaScript ir Style Sheets (CSS), kad būtų galima pateikti bendrą išdėstymą.

## Trumpa istorija ##

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. 2000 m. jis taip pat tapo tarptautiniu standartu (ISO/IEC 15445:2000). 1999 m. buvo paskelbtas HTML 4.01. 2004 m. Web Hypertext Application Technology Working Group (WHATWG) pradėjo dirbti su HTML5 versija, kuri 2008 m. tapo bendru W3C pristatymu. Ji buvo baigta ir standartizuota 2014 m. spalio 28 d.

## HTML failo formato struktūra ##

HTML 4 dokumentas susideda iš trijų dalių:

1. eilutė, kurioje yra HTML versijos informacija
1. deklaratyvioji antraštės dalis
1. tekstas, kuriame yra tikrasis dokumento turinys. Turinys gali būti įgyvendintas elementu BODY arba FRAMESET elementu, kad korpusas būtų rėmeliuose

Kiekviena sekcija gali būti pirma arba po jos gali būti tarpai, naujos eilutės, skirtukai ir komentarai. Paprasto HTML dokumento pavyzdys yra toks, kaip parodyta toliau:

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN"
   "http://www.w3.org/TR/html4/strict.dtd">
<HTML>
   <HEAD>
      <TITLE>Understanding HTML failo formatas</TITLE>
   </HEAD>
   <BODY>
      <P>Hello World!
   </BODY>
</HTML>
```

### Versijos informacija ###

Pirmoji kodo eilutė, \<!DOCTYPE html> , vadinamas doctype deklaracija ir nurodo naršyklei, kurioje HTML versijoje puslapis parašytas. Priklausomai nuo HTML versijos, yra keletas skirtingų doctype deklaracijų, kurios įvardija dokumentui naudojamą dokumento tipo apibrėžimą (DTD). Kiekvienas DTD skiriasi nuo kitų savo palaikomais elementais ir skiriasi taip:

* HTML 4.01 Strict – apima visus elementus ir atributus, kurie nebuvo [nebenaudojami](https://www.w3.org/TR/html401/conform.html#deprecated) arba nerodomi rėmelių rinkinio dokumentuose

* HTML 4.01 Transitional – apima viską, kas yra griežtame DTD, ir nebenaudojamus elementus bei atributus (dauguma jų susiję su vaizdiniu pateikimu

* HTML 4.01 Frameset – apima viską, kas yra pereinamuosiuose DTD plius rėmuose


**HTML5** versijos informacija yra tokia, kaip nurodyta toliau.

```
<!DOCTYPE html>
```

### HTML antraštės informacija ###

HTML dokumento antraštėje gali būti daug HTML elementų, kurių naršyklė nepateikia. Tokie elementai yra arba metaduomenys, apibūdinantys informaciją apie puslapį, arba apima skyrius, naudojamas informacijai gauti iš išorinių išteklių, pvz., CSS stilių lapų arba JavaScript failų. Puslapio antraštę žymi žyma head.

Norint nustatyti puslapio pavadinimą, **pavadinimo** elementas yra vienintelis, kurio reikia<head> žymės. Tą patį naudoja paieškos sistemos, norėdami nustatyti puslapio pavadinimą.

### HTML korpuso informacija ###

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

### HTML elementai ###

Kaip minėta anksčiau, turinys HTML korpuse yra vaizduojamas žymomis, taip pat žinomomis kaip HTML elementai. Kiekviena žyma gali turėti papildomos informacijos atributų pavidalu, kurie parašyti kaip<tag attribute1#value1 attribute2#value2> , nors nebūtina turėti atributų su kiekviena žyma. Jei atributai nepaminėti, kiekvienu atveju naudojamos numatytosios reikšmės. Toliau pateikiami keli elementų pavyzdžiai:

#### Antraštė ####

```
<head>
  <title>The Title</title>
</head>
```

#### Antraštės ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Pastraipos ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Nuorodos Nr.

* [Globali HTML dokumento struktūra](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


