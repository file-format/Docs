{
  "date": "2019-10-11",
  "keywords": [
"htm",
"htm failu",
"htm faila formātā",
"htm faila tips",
"failu",
"veids",
"kas ir htm fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HTM faila formāts",
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir HTM fails un API, kas tos var izveidot un atvērt.",
  "linktitle": "HTM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ht-lvm"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir HTM fails?

Faili ar paplašinājumu **.htm** ir hiperteksta iezīmēšanas valoda tīmekļa lapu izveidei, lai tās parādītu tīmekļa pārlūkprogrammās, piemēram, Google Chrome, Internet Explorer, Firefox un vairākās citās. Tas definē marķējumus statisku lapu izveidei, kas jāpublicē globālajā tīmeklī (WWW), lai piekļūtu citiem. Šie marķējumi norāda pārlūkprogrammām, kā parādīt tīmekļa lapas saturu. Šādās lapās var būt vienkāršs teksts, attēli, hipersaites uz citām lapām, videoklipi un cita multivides informācija. Kad tīmekļa lapa ir publicēta, varat apskatīt aiz tās esošo iezīmēšanas kodu, apskatot tās lapas avotu. Mūsdienu pārlūkprogrammas ļauj pārbaudīt katru tīmekļa lapas sadaļu, kurā ir izstrādāts katrs HTM avota apakšnodalījums vai iezīmēšanas elements.

## Īsa HTM vēsture

Since its inception and first role out, the HTML specifications have been maintained by World Wide Web Consortium (W3C) since 1996. 2000. gadā tas kļuva arī par starptautisku standartu (ISO/IEC 15445:2000). 1999. gadā tika publicēts HTML 4.01. 2004. gadā Web hiperteksta lietojumprogrammu tehnoloģiju darba grupa (WHATWG) sāka darbu pie HTML5 versijas, kas kļuva par kopīgu rezultātu ar W3C 2008. gadā. Tā tika pabeigta un standartizēta 2014. gada 28. oktobrī.

## HTML faila formāts

HTML 4 dokuments sastāv no trim daļām:

1. rinda, kurā ir informācija par HTML versiju
1. deklaratīvā galvenes sadaļa
1. pamatteksts, kas satur dokumenta faktisko saturu. Pamattekstu var ieviest elements BODY vai elements FRAMESET, lai ietvertu pamattekstu kadros

Katrai sadaļai var būt ievads vai aiz tās var būt atstarpes, jaunās rindiņas, cilnes un komentāri. Vienkārša HTML dokumenta piemērs ir šāds:

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

### Informācija par versiju

Pirmā koda rindiņa,<!DOCTYPE html> , tiek saukta par doctype deklarāciju un norāda pārlūkprogrammai, kurā HTML versijā lapa ir rakstīta. Atkarībā no HTML versijas ir vairākas dažādas doctype deklarācijas, kas nosauc dokumentam izmantoto dokumenta tipa definīciju (DTD). Katrs DTD atšķiras no citiem ar atbalstītajiem elementiem un atšķiras šādi:

* HTML 4.01 Strict — ietver visus elementus un atribūti, kas nav [novecojuši](https://www.w3.org/TR/html401/conform.html#deprecated) vai neparādās rāmju kopas dokumentos.

* HTML 4.01 Transitional — ietver visu stingrā DTD, kā arī novecojušos elementus un atribūtus (no kuriem lielākā daļa attiecas uz vizuālo prezentāciju

* HTML 4.01 Frameset — ietver arī visu pārejas DTD plus rāmjos


**HTML5** versijas informācija ir tāda, kā minēts tālāk.

```
<!DOCTYPE html>
```

### Galvenes informācija

HTML dokumenta galvenē var būt ietverti vairāki HTML elementi, kurus pārlūkprogramma neatveido. Šādi elementi ir vai nu metadati, kas apraksta informāciju par lapu, vai ietver sadaļas, kas tiek izmantotas, lai iegūtu informāciju no ārējiem resursiem, piemēram, CSS stilu lapām vai JavaScript failiem. Lapas galveni apzīmē \<head> tags un beidzas ar \</head> tagu.

Lai iestatītu lapas nosaukumu, \<title> elements ir vienīgais, kas ir nepieciešams tagos \<head>. To pašu izmanto meklētājprogrammas, lai identificētu lapas nosaukumu.

### Pamatinformācija

Šī ir galvenā faila sadaļa, kurā ir viss faila saturs, ko atveido pārlūkprogrammas. Html pamattekstā var būt atzīmes, kas var attiekties uz dažādiem elementiem tagu formā. Tas var saturēt dažādu veidu informāciju, piemēram, tekstu, attēlus, krāsas, grafiku utt. Turklāt audio un video elementus var arī iegult html pamattekstā, lai pārlūkprogrammas tos atveidotu. Mūsdienu stila lapu lietojumprogrammas vizuālajam attēlojumam klātbūtnē BODY prezentācijas atribūti, piemēram, fona krāsa, saites krāsa, teksta krāsa utt., ir novecojušas. Tādējādi tos pašus efektus var panākt, izmantojot stila lapas, kā parādīts tālāk:

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

Iekļautās stila lapas ir viegli iegult, un, lai ātri pielietotu vizuālos efektus, ārējās stila lapas padara ērtāku vienreizēju izvietošanu un piekļuvi daudzās vietās.

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

### HTML elementi

Kā minēts iepriekš, saturu HTML pamattekstā attēlo tagi, kas pazīstami arī kā HTML elementi. Katram tagam var būt papildu informācija atribūtu veidā, kas tiek rakstīti kā
```
<tag attribute1#"value1" attribute2#"value2">
```
lai gan nav obligāti jābūt atribūtiem ar katru tagu. Ja atribūti nav minēti, katrā gadījumā tiek izmantotas noklusējuma vērtības. Tālāk ir sniegti daži elementu piemēri.

#### Galvene

```
<head>
  <title>The Title</title>
</head>
```

#### Virsraksti

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Rindkopas

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Atsauces

* [HTML dokumenta globālā struktūra](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)


