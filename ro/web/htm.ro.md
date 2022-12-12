{
  "date" : "2019-10-11",
  "keywords" :[ "htm", "fișier htm", "format fișier htm", "tip fișier htm", "fișier", "tip", "ce este un fișier htm"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier HTM",
  "description" :"Ghidul dvs. de format de fișier pentru a afla ce este un fișier HTM și API-urile care le pot crea și deschide.",
  "linktitle" : "HTM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier HTM?

Fișierele cu extensia **.htm** reprezintă Hypertext Markup Language pentru crearea de pagini web pentru afișare în browsere web precum Google Chrome, Internet Explorer, Firefox și o serie de altele. Acesta definește markupurile pentru crearea de pagini statice care urmează să fie publicate pe World Wide Web (WWW) pentru accesul altora. Aceste markupuri le spun browserelor cum să afișeze conținutul unei pagini web. Astfel de pagini pot conține text simplu, imagini, hyperlinkuri către alte pagini, videoclipuri și alte informații media. Când o pagină web este publicată, puteți arunca o privire asupra codului de marcare din spatele acesteia, vizualizând sursa paginii acesteia. Browserele moderne permit inspectarea fiecărei secțiuni a unei pagini web în care este elaborată fiecare subdiviziune sau element de marcare din sursa HTM.

## Scurt istoric al HTM

De la înființare și primul lansare, specificațiile HTML au fost menținute de World Wide Web Consortium (W3C) din 1996. În 2000, a devenit, de asemenea, un standard internațional (ISO/IEC 15445:2000). În 1999, a fost publicat HTML 4.01. În 2004, Web Hypertext Application Technology Working Group (WHATWG) a început să lucreze la versiunea HTML5, care a devenit un produs comun cu W3C în 2008. A fost finalizată și standardizată pe 28 octombrie 2014.

## Format de fișier HTML

Un document HTML 4 este compus din trei părți:

1. o linie care conține informații despre versiunea HTML
1. o secțiune antet declarativă
1. un corp, care conține conținutul real al documentului. Corpul poate fi implementat de elementul BODY sau elementul FRAMESET pentru a conține corpul în cadre

Fiecare secțiune poate fi condusă sau urmată de spații albe, linii noi, file și comentarii. Un exemplu de document HTML simplu este prezentat mai jos:

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

### Informații despre versiune

Prima linie de cod,<!DOCTYPE html> , se numește declarație doctype și îi spune browserului în ce versiune de HTML este scrisă pagina. În funcție de versiunea de HTML, există o serie de declarații doctype diferite care denumesc definiția tipului de document (DTD) utilizată pentru document. Fiecare DTD diferă de celelalte în elementele pe care le suportă și diferă după cum urmează:

* HTML 4.01 Strict - include toate elementele și atributele care nu au fost [depreciate](https://www.w3.org/TR/html401/conform.html#deprecated) sau care nu apar în documentele setului de cadre
* HTML 4.01 de tranziție - include totul în DTD strict, plus elemente și atribute depreciate (majoritatea dintre acestea se referă la prezentarea vizuală)
* HTML 4.01 Frameset - include tot ce se află în DTD-ul de tranziție plus cadrele

Pentru **HTML5**, informațiile despre versiune sunt pur și simplu așa cum se menționează mai jos.

```
<!DOCTYPE html>
```

### Informații antet

Antetul unui document HTML poate include un număr de elemente HTML care nu sunt redate de browser. Astfel de elemente sunt fie metadate care descriu informații despre pagină, fie includ secțiuni care sunt utilizate pentru a prelua informații din resurse externe, cum ar fi foile de stil CSS sau fișierele JavaScript. Antetul unei pagini este reprezentat de \<head> etichetă și se termină cu \</head> etichetă.

<html>Pentru setarea titlului paginii, \<title> elementul este singurul care este necesar în etichetele \<head>. Același lucru este folosit de motoarele de căutare pentru a identifica titlul unei pagini. </html>

### Informații despre corp

Aceasta este secțiunea principală a fișierului care conține tot conținutul fișierului care este redat de browsere. Corpul HTML poate conține markupuri care se pot referi la diferite blocuri de construcție sub formă de etichete. Poate conține mai multe tipuri diferite de informații, cum ar fi text, imagini, culori, grafică etc. În plus, elementele audio și video pot fi, de asemenea, încorporate în corpul html pentru redare de către browsere. În prezența aplicației moderne de foi de stil pentru reprezentarea vizuală, atributele de prezentare ale BODY, cum ar fi culoarea de fundal, culoarea linkului, culoarea textului, etc. au fost depreciate. Astfel, aceleași efecte pot fi obținute folosind foi de stil, așa cum se arată mai jos:

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

Foile de stil în linie sunt ușor de încorporat și pentru aplicații rapide la efectele vizuale, foile de stil externe fac mai convenabil implementarea o singură dată și accesarea în mai multe locuri.

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

### Elemente HTML

După cum am menționat mai devreme, conținutul din HTML Body este reprezentat de etichete, cunoscute și sub numele de Elemente HTML. Fiecare etichetă poate avea informații suplimentare sub formă de atribute care sunt scrise ca
```
<tag attribute1#"value1" attribute2#"value2">
```
deși nu este necesar să aveți atribute cu fiecare etichetă. Dacă atributele nu sunt menționate, valorile implicite sunt utilizate în fiecare caz. Iată câteva dintre exemplele Element:

#### Antet

```
<head>
  <title>The Title</title>
</head>
```

#### Titluri

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paragrafe

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```

## Referințe

* [Structura globală a documentului HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

