{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "fundamente" ],
  "description":"Portable Document Format (PDF) este o reprezentare standard a documentelor independentă de software, hardware și sistem de operare. Standardele PDF includ PDF/A, PDF/E, PDF/UA, PDF/VT și PDF/X.",
  "title" :"Format fișier PDF – Ce este un fișier PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) este un tip de document creat de Adobe în anii 1990. Scopul acestui format de fișier a fost de a introduce un standard pentru reprezentarea documentelor și a altor materiale de referință într-un format care este independent de software-ul aplicației, hardware-ul și sistemul de operare. Formatul de fișier PDF are capacitatea deplină de a conține informații precum text, imagini, hyperlinkuri, câmpuri de formular, rich media, semnături digitale, atașamente, metadate, caracteristici geospațiale și obiecte 3D care pot deveni parte a documentului sursă.

În majoritatea cazurilor, documentele existente sunt convertite în PDF, mai degrabă decât să creeze un nou PDF de la zero. Dar asta nu înseamnă că nu există software pentru crearea sau manipularea fișierelor PDF.

**(Trebuie să împărtășiți ceva despre formatul fișierului PDF? Vă puteți posta constatările în secțiunea [Știri în format fișier PDF](https://news.fileformat.com/t/PDF).)**

## Format de fișier PDF - Scurt istoric

O prezentare rapidă a cronologiei despre formarea fișierului PDF în ceea ce privește cronologia este următoarea:

**1993** - Adobe Systems a făcut ca specificațiile PDF să fie disponibile gratuit

**2008** - PDF a fost lansat ca standard deschis la 1 iulie 2008 și a fost publicat de Organizația Internațională pentru Standardizare ca **ISO 32000-1:2008**.

**2008** - Adobe a publicat o licență publică de brevet pentru formatul ISO 32000-1 drepturi fără drepturi de autor pentru toate brevetele deținute de Adobe care sunt necesare pentru a realiza, utiliza, vinde și distribui implementări compatibile cu PDF.

Prima versiune de PDF a fost desemnată PDF 1.0, care a trecut ulterior prin revizuiri până la PDF 1.7. PDF 1.7, care a devenit ISO 32000-1, include unele tehnologii proprietare nestandardizate, precum și Adobe XML Forms Architecture (XFA) și extensia JavaScript pentru Acrobat. Pe 28 iulie 2017 a fost publicat PDF 2.0, cunoscut sub numele de ISO 32000-2:2017, care nu include tehnologii nestandardizate.

## Specificații de format de fișier PDF

Un fișier PDF este un set de octeți care pot fi grupați în token-uri conform regulilor de sintaxă definite de specificațiile PDF. O dată sau mai multe jetoane sunt combinate pentru a forma entități sintactice de nivel superior, în principal obiecte, care sunt valorile de bază ale datelor din care este construit un document PDF.

### Structura fișierelor PDF

Conținutul fișierului PDF este aranjat în următoarea secvență în interiorul fișierului.

| Antet
|Corpul
|Tabel de referințe încrucișate
|Remorcă

#### Antet fișier PDF ####

Indiferent de versiunea PDF, un fișier PDF începe cu un antet care conține un identificator unic pentru PDF și versiunea formatului, cum ar fi %PDF-1.x, unde x variază de la 1 la 7.

#### Corpul fișierului ####

Corpul unui fișier PDF constă dintr-o secvență de obiecte indirecte reprezentând conținutul unui document. Obiectele, așa cum sunt descrise mai sus, reprezintă componente ale documentului, cum ar fi fonturi, pagini și imagini eșantionate. Începând cu PDF 1.5, corpul poate conține și fluxuri de obiecte, fiecare dintre ele conține o secvență de obiecte indirecte.

#### Tabel de referințe încrucișate ####

Tabelul de referințe încrucișate conține informații care permit accesul aleatoriu la obiectele indirecte din fișier, astfel încât întregul fișier nu trebuie citit pentru a localiza un anumit obiect. Tabelul trebuie să conțină o intrare pe o linie pentru fiecare obiect indirect, specificând decalajul de octeți a acelui obiect în corpul fișierului. (Începând cu PDF 1.5, unele sau toate informațiile de referință încrucișată pot fi conținute alternativ în fluxuri de referințe încrucișate.

#### File Trailer ####

Trailerul unui fișier PDF permite unui cititor conform să găsească rapid tabelul de referințe încrucișate și anumite obiecte speciale. Cititorii conformi ar trebui să citească un fișier PDF de la capăt. Ultima linie a fișierului va conține doar marcatorul de sfârșit de fișier, %%EOF. Cele două linii precedente trebuie să conțină, una pe linie și în ordine, cuvântul cheie startxref și byte offset în fluxul decodat de la începutul fișierului până la începutul cuvântului cheie xref din ultima secțiune de referință încrucișată.

### Obiecte PDF ###

Un fișier PDF include mai multe tipuri diferite de obiecte care sunt de următoarele tipuri

* Valori booleene - reprezentând condițional adevărat sau fals
* Numere - valori întregi și reale
* Șiruri - conține caractere între paranteze
* Nume - începe cu un caracter înainte / de exemplu /ASomewhatLongerName are ca rezultat ASomewhatLongerName
* Arrays - PDF acceptă matrice unidimensionale. Matricele de dimensiuni mai mari pot fi construite folosind matrice ca elemente imbricate
* Dicționare - colecție de obiecte ca perechi cheie-valoare. Poate avea zero intrări.
* Fluxuri - reprezintă o secvență de octeți care pot avea și o lungime nelimitată
* Null Object - reprezintă o valoare nulă

Pot exista și alte obiecte, cum ar fi comentarii, care sunt introduse cu semnul % și pot conține caractere de 8 biți.

### Obiecte indirecte ###

Orice obiect dintr-un fișier PDF poate fi etichetat ca obiect indirect. Obiectelor indirecte li se oferă un identificator unic de obiect prin care alte obiecte se pot referi la el. Referențele încrucișate la acestea sunt menținute într-un tabel index și marcate cu cuvântul cheie xref care urmează corpul principal și oferă offset-ul de octeți a fiecărui obiect indirect de la începutul fișierului.

### Aspecte PDF liniare și neliniare ###

Aspectele PDF sunt clasificate ca Llneare și neliniare, în funcție de aplicațiile țintă și de alți factori.

Neliniar - Fișierele PDF neliniare utilizează mai puțin spațiu pe disc în comparație cu fișierele PDF liniare. Paginile PDF ale documentului se află în formă împrăștiată în fișierul PDF și de aceea fișierele neliniare sunt mai lente în comparație cu fișierele liniare.

PDF liniar - Vizând vizualizatorii PDF online, fișierele PDF liniar sunt construite în așa fel încât să fie scrise pe disc într-un mod liniar. Acest lucru nu necesită pluginuri de browser pentru ca întregul document să se încarce mai întâi înainte de afișare.

### Prezentare generală a obiectelor ###

După cum am menționat, PDF body este o colecție de obiecte menționate mai sus. PDF se bazează în mare parte pe PostScript, fără caracteristicile de control ale limbajelor de programare, cum ar fi comenzile if și loop. Comenzile emise de codul Postscript pentru a genera conținut grafic sunt colectate și tokenizate în plus față de orice fișiere, grafice sau fonturi menționate de document. Toate aceste conținuturi sunt acumulate într-un singur fișier, rezultând o ieșire PostScript compusă.

#### Text ####

Textul în PDF este reprezentat de elemente de text care sunt de fapt afișate cu glife din fonturi. Un glif este o formă grafică și este supusă tuturor manipulărilor grafice, cum ar fi transformarea coordonatelor. Datorită importanței textului în majoritatea descrierilor paginilor, PDF oferă facilități de nivel superior pentru a descrie, selecta și reda glife în mod convenabil și eficient.

#### Grafică ####

Operatorii grafici utilizați în fluxurile de conținut PDF descriu aspectul paginilor care urmează să fie reproduse pe un dispozitiv de ieșire raster. Facilitățile sunt destinate atât aplicațiilor de imprimantă, cât și de afișare. Operatorii grafici formează șase grupuri principale:

* Operatorii de stare grafică manipulează structura de date numită stare grafică, cadrul global în care se execută ceilalți operatori grafici. Starea grafică include matricea de transformare curentă (CTM), care mapează coordonatele spațiului utilizator utilizate într-un flux de conținut PDF în coordonatele dispozitivului de ieșire. De asemenea, include culoarea curentă, calea de tăiere curentă și mulți alți parametri care sunt operanzi impliciti ai operatorilor de pictură.
* Operatorii de construcție a căilor specifică căi, care definesc forme, traiectorii de linii și regiuni de diferite tipuri. Acestea includ operatori pentru începerea unui nou traseu, adăugarea de segmente de linie și curbe la acesta și închiderea acesteia.
* Operatorii de pictare a traseului umplu un traseu cu o culoare, pictează un contur de-a lungul ei sau îl folosesc ca limită de tăiere.
* Alți operatori de pictură pictează anumite obiecte grafice care se descriu pe sine. Acestea includ imagini eșantionate, umbriri definite geometric și fluxuri întregi de conținut care, la rândul lor, conțin secvențe de operatori grafici.
* Operatorii de text selectează și afișează glife de caractere din fonturi (descrieri ale fonturilor pentru reprezentarea caracterelor text). Deoarece PDF tratează glifele ca forme grafice generale, mulți dintre operatorii de text ar putea fi grupați cu operatorii de stare grafică sau de pictură. Cu toate acestea, structurile și mecanismele de date pentru tratarea descrierilor de glif și fonturi sunt suficient de specializate.
* Operatorii de conținut marcat asociază informații logice de nivel superior cu obiectele din fluxul de conținut. Aceste informații nu afectează aspectul redat al conținutului; este util pentru aplicațiile care folosesc PDF pentru schimbul de documente.

## Referințe ##

* [Format fișier PDF: Structură de bază](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [Referință PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

