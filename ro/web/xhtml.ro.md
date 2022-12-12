{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Fișier", "Extensie", "Format fișier", "Extensie fișier", "html extensibil"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Format de fișier Extensible Hypertext Markup Language",
  "description":"Aflați despre ce este formatul de fișier XHTML și API-urile care pot crea și deschide fișiere XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier XHTML?

XHTML este un format de fișier bazat pe text cu marcare în XML, folosind o reformulare a HTML 4.0. Aceste fișiere sunt potrivite pentru a fi deschise sau vizualizate într-un browser web. XHTML a fost conceput pentru a fi mai structurat, mai puțin scripting, generic; folosind toate facilitățile existente ale XML și mai mult independent de dispozitiv. XHTML oferă un set util de elemente și atribute, cu opțiuni de extensie în combinație cu foi de stil. Atributele sunt utilizate din colecția de atribute de metadate. XHTML oferă flexibilitate și accesibilitate prin subordonarea tuturor elementelor de prezentare **[HTML](/ro/web/html/)** foilor de stil. Foile de stil sunt mai versatile decât aceste elemente de prezentare. Specificațiile pentru HTML 4.01, HTML5 și XHTML sunt dezvoltate dinamic de World Wide Web Consortium (W3C).

## Scurt istoric al formatului de fișier XHTML

Istoria XHTML începe cu un proiect de document lansat în decembrie 1998 de World Wide Web Consortium. Acest document se referă la „Reformularea HTML în XML”, o specificație numită XHTML 1.0. Această nouă specificație a reformulat HTML în XML folosind elementele sau atributele existente. În mai 1999, W3 Consortium a declarat că HTML 4.0 a fost reformat ca aplicație XML. adică XHTML. În 26 ianuarie 2000, prima specificație care definește XHTML 1.0 a fost lansată de W3C. Mai departe, în 31 mai 2001, W3C a anunțat XHTML ca limbaj independent și a început să lucreze la dezvoltarea HTML 5.0. Cu toate acestea, în 2005, a fost format un grup de lucru (WHATWG) care a avut ca scop îmbunătățirea HTML-ului obișnuit independent de XHTML. WHATWG a început în cele din urmă să lucreze pe HTML5 în paralel cu XHTML 2.

## Format de fișier XHTML

XHTML este un format, care este o colecție de diferite tipuri de documente și module care imită, clasifică și extind HTML 4. Fișierele din XHTML sunt bazate pe XML și au scopul de a lucra cu agenții utilizator bazați pe XML. Fișierele XHTML sunt conforme cu XML. Instrumentele XML standard sunt utilizate pentru a vizualiza, edita și valida fișierele XHTML. Aplicațiile dependente de modelul obiect de document HTML sau modelul de obiect de document XML [DOM] pot funcționa prin documente XHTML. Optând astăzi XHTML, dezvoltatorii de conținut se pot bucura de toate beneficiile asociate XML fără a-și face griji cu privire la compatibilitatea înainte sau înapoi a conținutului lor.

Un set de elemente înrudite construiește un modul în XHTML. Un formular sau un modul de tabel poate conține diverse elemente de formular sau de tabel care pot fi afișate pe o pagină web. Modularizarea a avut ca scop izolarea elementelor HTML în seturi de numeroase elemente legate. Pentru ca dezvoltatorii de conținut să poată profita de selecția modulelor pentru diferite tipuri de dispozitive. În plus, modulele permit agenților utilizator să selecteze elemente fără a pierde consistența cu standardul XHTML. Cerințele de analiză ale XHTML sunt aceleași cu XML, în timp ce HTML își practică propriile.

### Conformitatea documentelor

XHTML2 oferă specificații conform documentelor XHTML 1.0, care utilizează elementele spațiilor de nume și atributele din XML și XHTML 1.0. Conformitatea documentelor este de două tipuri.

Un document strict conform se bazează pe XML și necesită doar servicii obligatorii definite în această specificație. Pentru fișierele XHTML trebuie îndeplinite următoarele criterii:

* Un fișier trebuie să respecte constrângerile definite în DTD-uri și în Anexa B.
* Elementul de bază al fișierului trebuie să fie html.
* Elementul de bază al fișierului trebuie să conțină declarație pentru spațiul de nume XHTML și ar trebui definit ca:

```
http://www.w3.org/1999/xhtml.
```

* Elementul de bază poate fi scris ca:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Înainte de elementul de bază, trebuie declarat un DOCTYPE, al cărui identificator public trebuie să facă referire la una dintre cele trei definiții de tip de document (DTD). Identificatorul de sistem poate fi modificat pentru a se conforma cu convențiile actuale de sistem.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

În documentele XML, nu este necesar să specificați declarații XML în toate documentele; cu toate acestea, dezvoltatorii de conținut sunt încurajați să folosească declarații XML în toate documentele lor XHTML. Aceste declarații sunt obligatorii fie atunci când codificarea caracterelor documentului este diferită de UTF-8/16 sau nu a fost specificată nicio codificare de către un protocol de guvernare. Următorul exemplu de document XHTML definește declarațiile XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Un agent utilizator conform trebuie să îndeplinească următoarele reguli:

* Analiza și evaluarea documentului XHTML se face de către un agent utilizator care asigură coerența acestuia cu Recomandarea XML 1.0.
* În cazul validării agentului utilizator, acesta trebuie să verifice validitatea documentelor pentru DTD-urile la care se face referire conform XML. Când fișierul XHTML este procesat de agentul utilizator ca XML generic, caracteristicile de tip ID vor fi recunoscute ca identificatori de fragment.

Dacă un agent utilizator se lovește de un element nerecunoscut, următoarele sunt criteriile obligatorii pe care trebuie să le îndeplinească

* procesează conținutul acelui element necunoscut
* ignorați atributul și valoarea acestuia
* Utilizați valoarea atributului furnizat ca implicit.

Când agentul utilizator întâlnește o declarație de referință a unei entități care nu a fost procesată mai devreme, atunci aceasta ar trebui să fie procesată ca caractere (începând cu semnul „&” și se termină cu punct și virgulă). În timpul procesării conținutului, caracterele sau referințele la entități de caracter care sunt previzibile de agentul utilizator, dar care nu pot fi redate, pot utiliza orice redare alternativă care oferă un înțeles similar. În acest caz, documentul trebuie să fie afișat într-o manieră care să facă utilizatorului evident faptul că procesul de randare nu a fost normal. Pentru procesarea spațiilor albe, agentul utilizator trebuie să caute definiția din caracterele CSS [CSS2].

## Compatibilitate cu XHTML înapoi

Compatibilitatea în spate a documentelor XHTML 1. este bine familiarizată cu agenții utilizator HTML 4, dacă sunt respectate regulile adecvate. XHTML 1.1 este pe deplin compatibil, cu excepția adnotărilor ruby, chiar dacă acestea sunt în general ignorate de browserele HTML 4. XHTML 2.0 este comparativ mai puțin compatibil, cu toate acestea problema a fost rezolvată într-o oarecare măsură prin utilizarea scripturilor.

## Referințe

* [O istorie a XHTML: Din anii 1990 până astăzi](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

