{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier PS",
  "description":"Aflați despre formatul de fișier PS și despre API-urile care pot crea și deschide fișiere PS.",
  "linktitle" : "PS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier .PS? ##

PostScript (PS) este un limbaj de descriere a paginilor de uz general utilizat în afacerile de publicare pe computer și electronice. Obiectivul principal al PostScript (PS) este de a facilita designul grafic bidimensional. Majoritatea limbilor necesită o etapă de compilare distinctă înainte de execuția codului, în timp ce formatul Post Script (PS) acceptă o interpretare directă la timp de execuție. Versiunea sa timpurie definește formele grafice, diferitele apariții ale textului și imaginile modelate pe paginile tipărite sau pe paginile afișate, urmând regulile modelului de imagine Adobe. Un program de PS este capabil să comunice o descriere a unui document între o compoziție și un sistem de imprimare, menținând dispozitivul independent și la nivel înalt. Mai mult, acest program este, de asemenea, capabil să guverneze aspectul textului și graficelor pe un afișaj.

Descrierea paginii PostScript este disponibilă pentru a fi redată, afișată pe imprimantă și pe alt dispozitiv de ieșire cu ajutorul interpretului PostScript al dispozitivului. Pe măsură ce comenzile de tipărire a caracterelor, formelor grafice și imaginilor sunt executate de către interpret, pentru acel dispozitiv specific, descrierea PostScript de nivel înalt se convertește în formatul de date raster de nivel scăzut. În general, diferite aplicații, cum ar fi ilustratorii, sistemele de compunere a documentelor și proiectarea asistată de computer (CAD) sunt automatizate pentru a genera descrieri de pagini PostScript. În general, programatorii trebuie să scrie programe PostScript în momentul creării de noi aplicații. Cu toate acestea, un programator poate profita de capacitățile limbajului PostScript care nu sunt accesibile în nicio aplicație prin scrierea unui program PS pentru acea situație specială.

## Scurt istoric ##

Conceptul de limbaj PostScript a fost introdus pentru prima dată de John Warnock. În 1966 lucra la un proiect al portului din New York. El încerca să dezvolte un interpret pentru o grafică tridimensională mare pentru baza de date a proiectului respectiv. Pentru procesarea acestor grafice, John Warnock a conceput limbajul Design System. Între timp, Xerox PARC căuta un mijloc standard de definire a imaginilor de pagină pentru prima lor imprimantă laser. Deși Bob Sproull și William Newman în 1975-76 au dezvoltat formatul Press (format de date) pentru a conduce imprimantele laser, totuși era nevoie de un limbaj pentru mai multă flexibilitate. În 1978, Warnock s-a alăturat lui Martin Newell în Xerox PARC și a rescris limbajul interpretativ, JaM, care a fost ulterior crescut și extins în limbajul Interpress. Warnock a fondat Adobe Systems în decembrie 1982 împreună cu Chuck Geschke, Doug Brotz, Ed Taft și Bill Paxton. Au început să lucreze la un limbaj mai simplu numit PostScript similar cu Interpress, care a fost lansat comercial în 1984. Steve Jobs de la Apple i-a vizitat și i-a sfătuit să adapteze PostScript pentru a conduce imprimantele laser.

În martie 1985, prima imprimantă cu un interpret PostScript încorporat a fost Apple LaserWriter, care a revoluționat desktop publishing (DTP). Soliditatea tehnică și disponibilitatea pe scară largă au făcut din PostScript, un limbaj de alegere pentru publicarea desktop și electronică. În 1990, un interpret pentru limbajul PostScript a fost o parte esențială a imprimantelor laser.

## Caracteristici principale ##

Capacitățile limbajului PostScript de a se ocupa de grafica interactivă și descrierea paginii posedă următoarele caracteristici:

**Forme:** de natură arbitrară, pot cuprinde linii drepte, curbe, pătrate și curbe cubice care pot fi atât auto-traversante, cât și deconectate (în secțiuni și găuri).

**Operatori de pictură:** permit conturul formei de orice grosime, culoare, umplere sau permit ca forma să fie desenată ca decupare pentru a permite tăierea oricărui alt grafic.

**Culori:** au o diversitate precum tonuri de gri, RGB, CMYK și CIE. Tipuri speciale de culori sunt modelate ca caracteristici diferite: culori spot, mapare a culorilor, chiar umbrire și modele repetate.

**Text:** complet integrat cu grafica. Mai mult, modelul de imagistică Adobe permite afișarea caracterelor de text ca forme grafice care pot fi operate de orice operator grafic normal.

**Imagini eșantionate**: extrase din surse originale (fotografii scanate) sau pot fi produse sintetic. Limbajul PostScript oferă diverse mijloace de regenerare a imaginilor la orice rezoluție și în funcție de diferite modele de culoare pe un dispozitiv de ieșire.

Un limbaj de programare de uz general poate profita de capacitățile grafice limbajul PostScript prin încorporarea Ps în cadrul său. Tipurile de date primitive, cum ar fi numere, caractere, matrice și șiruri de caractere; primitive de control, cum ar fi bucle, proceduri și condiționale; iar unele caracteristici neconvenționale, cum ar fi dicționarele, sunt specificate în limbaj. Aceste caracteristici facilitează programatorilor să scrie comenzi pentru a invoca operații de nivel superior. Aceste operațiuni de nivel înalt îndeplinesc nevoile aplicațiilor complexe. O astfel de practică este mai compactă și mai eficientă decât utilizarea unui set fix de operații de bază.

Programele scrise în PostScript pot fi produse, comunicate și interpretate sub formă de text sursă ASCII. Întreaga limbă poate fi definită sub formă de caractere imprimabile și spațiu alb. Această reprezentare îi ajută pe programatori să creeze, să manipuleze și să înțeleagă cu ușurință limbajul. În plus, stocarea și transmiterea fișierelor între diverse computere și sisteme de operare au fost menținute convenabile prin independența mașinii.

Formele codificate binare ale limbajului sunt posibile, atunci când programul este garantat pentru o cale de comunicație complet transparentă către interpretul PostScript. Pentru schimbul de documente sau stocarea arhivă, Adobe recomandă o coeziune strictă la reprezentarea ASCII a programelor PS.

## Versiunile ##

PS(.ps) este extensia de fișier pentru un document PostScript. Arhivele Naționale din Regatul Unit clasifică cinci versiuni cronologice ale fișierului PostScript, definite în versiunea DSC: versiunile 1.0, 2.0, 2.1, 3.0, 3.1. Fiecare versiune definește comentarii importante de structurare. Fișierul PostScript încapsulat (EPS) este un subtip special de fișier PostScript care utilizează limbajul pentru a specifica un grafic dreptunghiular. Manualul de referință al limbajului PostScript descrie un EPS ca: „Un fișier PostScript încapsulat (EPS) este un program PostScript care descrie cel mult o singură pagină într-o formă care poate fi importată de alte aplicații pentru a fi încorporat într-un document care le conține”. Un fișier de document PostScript poate încapsula un fișier EPS în el. O utilizare suplimentară a PostScript este menționată ca Display PostScript (DPS). DPS generează grafică pe ecran printr-un motor grafic care utilizează modelul și limbajul de imagine PostScript.

## Referințe ##

* [Familia de format PostScript](https://www.loc.gov/preservation/digital/formats/fdd/fdd000029.shtml)

