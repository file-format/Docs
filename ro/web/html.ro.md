{
  "date" : "2019-10-11",
  "keywords" :[ "html","fișier html", "format fișier html", "tip fișier html", "fișier", "tip", "ce este un fișier html" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier HTML",
  "description":"Aflați despre formatul de fișier HTML și despre API-urile care pot crea și deschide fișiere HTML.",
  "linktitle" : "HTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier HTML?

HTML (Hyper Text Markup Language) este extensia pentru paginile web create pentru afișare în browsere. Cunoscut ca limbajul web, HTML a evoluat cu cerințele de noi cerințe de informații care trebuie afișate ca parte a paginilor web. Cea mai recentă variantă este cunoscută ca HTML 5, care oferă multă flexibilitate pentru lucrul cu limbajul. Paginile HTML sunt fie primite de la server, unde acestea sunt găzduite, fie pot fi încărcate și din sistemul local. Fiecare pagină HTML este alcătuită din elemente HTML, cum ar fi formulare, text, imagini, animații, link-uri etc. Aceste elemente sunt reprezentate de etichete și alte câteva în care fiecare etichetă are început și sfârșit. De asemenea, poate încorpora aplicații scrise în limbaje de scripting, cum ar fi JavaScript și Foi de stil (CSS) pentru reprezentarea generală a aspectului.

## Scurt istoric ##

De la înființarea și primul lansare, specificațiile HTML au fost menținute de World Wide Web Consortium (W3C) din 1996. În 2000, a devenit, de asemenea, un standard internațional (ISO/IEC 15445:2000). În 1999, a fost publicat HTML 4.01. În 2004, Web Hypertext Application Technology Working Group (WHATWG) a început să lucreze la versiunea HTML5, care a devenit un produs comun cu W3C în 2008. A fost finalizată și standardizată pe 28 octombrie 2014.

## Structura formatului fișierului HTML ##

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

### Informații despre versiune ###

Prima linie de cod, \<!DOCTYPE html> , se numește declarație doctype și îi spune browserului în ce versiune de HTML este scrisă pagina. În funcție de versiunea de HTML, există o serie de declarații doctype diferite care denumesc definiția tipului de document (DTD) utilizată pentru document. Fiecare DTD diferă de celelalte în elementele pe care le suportă și diferă după cum urmează:

* HTML 4.01 Strict - include toate elementele și atributele care nu au fost [depreciate](https://www.w3.org/TR/html401/conform.html#deprecated) sau care nu apar în documentele setului de cadre
* HTML 4.01 de tranziție - include totul în DTD strict, plus elemente și atribute depreciate (majoritatea dintre acestea se referă la prezentarea vizuală)
* Setul de cadre HTML 4.01 - include tot ce se află în DTD-ul de tranziție plus cadrele

Pentru **HTML5**, informațiile despre versiune sunt pur și simplu așa cum se menționează mai jos.

```
<!DOCTYPE html>
```

### Informații antet HTML ###

Antetul unui document HTML poate include un număr de elemente HTML care nu sunt redate de browser. Astfel de elemente sunt fie metadate care descriu informații despre pagină, fie includ secțiuni care sunt utilizate pentru a prelua informații din resurse externe, cum ar fi foile de stil CSS sau fișierele JavaScript. Antetul unei pagini este reprezentat de eticheta head.

Pentru setarea titlului paginii, elementul **titlu** este singurul care este necesar în cadrul<head> Etichete. Același lucru este folosit de motoarele de căutare pentru a identifica titlul unei pagini.

### Informații despre corpul HTML ###

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

### Elemente HTML ###

După cum am menționat mai devreme, conținutul din HTML Body este reprezentat de etichete, cunoscute și sub numele de Elemente HTML. Fiecare etichetă poate avea informații suplimentare sub formă de atribute care sunt scrise ca<tag attribute1#"value1" attribute2#"value2"> , deși nu este necesar să aveți atribute cu fiecare etichetă. Dacă atributele nu sunt menționate, valorile implicite sunt utilizate în fiecare caz. Iată câteva dintre exemplele Element:

#### Antet ####

```
<head>
  <title>The Title</title>
</head>
```

#### Titluri ####

```
<h1>Heading level 1</h1>
<h2>Heading level 2</h2>
<h3>Heading level 3</h3>
<h4>Heading level 4</h4>
<h5>Heading level 5</h5>
<h6>Heading level 6</h6>
```

#### Paragrafe ####

```
<p>Paragraph 1</p> <p>Paragraph 2</p>
```


## Referințe ##

* [Structura globală a documentului HTML](https://www.w3.org/TR/html401/struct/global.html#h-7.5.4)

