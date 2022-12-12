{
  "date" : "2019-10-11",
  "keywords" :[ "fișier emf", "format fișier emf", "ce este un fișier emf", "fișier", "exemplu emf", "extensie fișier emf", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMF – Format de metafile îmbunătățit",
  "description":"Aflați despre formatul de fișier EMF și despre API-urile care pot crea și deschide fișiere EMF.",
  "linktitle" : "EMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier EMF?

**Format de metafișier îmbunătățit (EMF)** stochează imagini grafice independent de dispozitiv. Metafișierele EMF cuprind înregistrări cu lungime variabilă în ordine cronologică care pot reda imaginea stocată după analizarea pe orice dispozitiv de ieșire. Aceste înregistrări cu lungime variabilă pot fi definiții ale obiectelor incluse, comenzi pentru desen și proprietăți grafice esențiale pentru a reda imaginea cu acuratețe. Când un dispozitiv deschide un metafișier EMF folosind propriul mediu grafic, proporțiile, dimensiunile, culorile și alte proprietăți grafice ale imaginii originale rămân aceleași, indiferent de platforma dispozitivului de deschidere.

## Scurt istoric ##

În 1990, Microsoft a proiectat un format de fișier imagine Windows Metafile ([WMF](/ro/image/wmf/)) pentru Microsoft Windows. Metafișierele Windows sunt în format de 16 biți care pot conține unele componente bitmap. WMF poate consta din grafică vectorială și este destinat să rămână portabil între diferite aplicații. În 1993, Win32/GDI a anunțat Enhanced Metafile (EMF), o versiune mai nouă, cu flexibilitate și scalabilitate îmbunătățite. EMF este folosit și ca comenzi pentru limbajul grafic pentru a rula driverele de imprimantă. Microsoft recomandă acum formatul de metafișier îmbunătățit (EMF) față de formatul Windows (WMF). Când a fost introdus Windows XP, a fost lansată versiunea Enhanced Metafile Format Plus (EMF+). Această versiune mai nouă își găsește drumul prin serializarea apelurilor API GDI+, de asemenea, WMF/EMF înregistrează apelurile către GDI. Există o versiune comprimată gzip a EMF cunoscută sub numele de EMZ.

## Format metafișier EMF ##

Următoarele sunt elementele esențiale ale formatului de metafișier îmbunătățit:

* Un EMR_HEADER (versiunea, dimensiunea, rezoluția imaginii la creare)
* Un tabel pentru obiectele GDI
* O paletă rezervată (opțional)
* Înregistrări metafile aranjate în structură matrice (setări de proprietate, obiecte definite, comenzi de desen)
* Înregistrare EMR_EOF (ultima înregistrare în metafișierul EMF)

## Versiuni EMF ##
* **Original**: versiunea originală specifică înregistrarea necesară pentru a păstra imaginea originală și pentru a-i menține independentă de dispozitiv. În plus, acceptă înregistrarea care conține obiecte grafice și comenzi pentru desen.
* **Versiunea 1**: Cea de-a doua versiune a EMF a îmbunătățit flexibilitatea și independența dispozitivului prin adăugarea înregistrării pentru formatul pixelilor și prevederea utilizării comenzii OpenGL.
* **Versiunea 2**: Cea de-a treia versiune a îmbunătățit precizia prin adăugarea sistemului Metric pentru a măsura distanța la suprafața dispozitivului, lăsând înregistrarea mai scalabilă.

## Înregistrări îmbunătățite metafile ##

Înregistrările metafile sunt aranjate sub formă de matrice. Aceste înregistrări au structură ENHMETARECORD și lungime variabilă. ENHMETARECORD specifică datele care definesc funcțiile GDI pentru a crea o imagine folosind formatul de metafișier îmbunătățit. Structura **ENHMETAHEADER** este întotdeauna prima înregistrare în acest format. Acest antet EMF conține următoarele informații.

Fiecare înregistrare a metafișierului îmbunătățit are doi membri ai EMR (oferă structura de bază) la început. Primul membru recunoaște funcția GDI (parametrii sunt utilizați în înregistrare) care determină tipul de înregistrare și este cunoscută sub numele de iType. Celălalt membru nSize definește dimensiunea fiecărei înregistrări. Parametrii rămași (dacă există) și date suplimentare aranjate imediat sub nSize. Imediat după antet poate prezenta o descriere text opțională. Numele imaginii și al autorului sunt înregistrate în descrierea textului respectiv. Paleta a cărei prezență este o opțiune specifică culorile utilizate în crearea de metafișier îmbunătățită. Celelalte înregistrări sunt folosite pentru a specifica funcția GDI, care este esențială în crearea imaginii.

În fiecare metafișier ar trebui să fie prezentă cel puțin o înregistrare EMF. Informațiile de trecere de la o înregistrare la alta depinde de înregistrările EMF, astfel încât aceste înregistrări trebuie aranjate adiacent. La orice înregistrare dată din metafișier, cu excepția EOF_record, lungimea acelei înregistrări specifice definește trecerea la următoarea înregistrare.

## Creare îmbunătățită de metafișier ##

Funcția **CreateEnhMetaFile** este utilizată pentru a crea un metafișier îmbunătățit. Argumentele acestei funcții sunt folosite pentru dimensiunile și stocarea imaginii pe disc/memorie. În plus, această funcție necesită dimensiunea dispozitivului în care a apărut prima imagine (dispozitiv de referință) și contextul dispozitivului de referință (DC). Deci, argumentele pentru a gestiona acest DC trebuie să le furnizeze atunci când se apelează funcția **CreateEnhMetaFile**. Sintaxa funcției este următoarea:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** mâner la un dispozitiv de referință.

**lptoFilename:** Un indicator către numele fișierului.

**lprc:** Indicatorul către structura ovală specifică dimensiunile imaginii în mm.

**lpDesc:** un indicator către un șir pentru titlul imaginii și numele aplicației care a creat imaginea.

## Operații îmbunătățite cu metafile ##

Următoarele sunt lucrări care pot fi realizate folosind mânerul la un metafișier îmbunătățit.

* Afișați și editați imaginea stocată.
* Produce copii de metafișier îmbunătățite.
* Preluați copia unui antet EMF, descrierea opțională și versiunea binară a unui metafișier îmbunătățit
* Recapitulați culorile din paletă.

## Obiecte grafice ##

În operațiunile de desen și pictură, obiectele grafice pot fi create prin înregistrările de creare a obiectelor și pot fi salvate pentru utilizare ulterioară. O înregistrare `EMR_SELECTOBJECT` poate prelua aceste obiecte grafice folosind contextul dispozitivului de redare. Pixurile, paletele, pensulele, spațiile de culoare, fonturile și obiectele stoc sunt câteva tipuri de obiecte reutilizabile.

## Comanda octet ##

Formatul Little-endian este folosit pentru a stoca date în înregistrările metafile.

## Versiune ##

Formatul fișierului EMF a fost revizuit de două ori. Versiunile modificate sunt originale, extensia 1 și extensia 2. Versiunile extinse au prevederi pentru înregistrări OpenGL și un descriptor opțional pentru formatul de pixel intern. Se adaugă o facilitate de măsurare în mililitri pentru dimensiunile afișate.

## Referințe ##

* [Metafișiere cu format îmbunătățit | Microsoft Docs](https://docs.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)
* [Format și specificații îmbunătățite pentru metafișier](https://msdn.microsoft.com/en-us/library/cc230514.aspx)

