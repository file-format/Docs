{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Aflați despre formatul de fișier PCL și despre API-urile care pot crea și deschide fișiere PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PCL? ##

PCL înseamnă Printer Command Language, care este un limbaj de descriere a paginii introdus de Hewlett Packard (HP). HP a creat PCL pentru a oferi o modalitate eficientă de control al caracteristicilor imprimantei pe mai multe dispozitive de imprimare diferite. Formatul a fost dezvoltat inițial pentru imprimantele HP cu matrice de puncte și cu jet de cerneală, dar a făcut parte din diferite imprimante termice, matriciale și de pagină odată cu trecerea timpului. Formatul a suferit mai multe revizuiri diferite, rezultând versiuni diferite în care fiecare versiune a fost îmbunătățită pentru a răspunde cerințelor de timp în ceea ce privește caracteristicile de control al imprimantei. Astăzi, PCL este cel mai răspândit limbaj de imprimantă pe ultima piață a imprimantelor.

## Versiuni PCL ##

Versiunile PCL diferă în funcție de funcționalitate (de exemplu, suport pentru tipul de font: fonturi bitmap, fonturi scalabile (Intellifonts, fonturi TrueType), metode de compresie grafică raster, suport grafic HP-GL/2).

**PCL 1:** în jurul anului 1980 - Funcționalitatea de imprimare și spațiu este setul de bază de funcții furnizate pentru ieșire simplă, convenabilă, pentru un singur utilizator.

**PCL 2:** în jurul anului 1980 - EDP (Electronic Data Processing)/Funcționalitatea de tranzacție este un superset al PCL 1. Funcțiile au fost adăugate pentru imprimare de sistem cu mai mulți utilizatori.

**PCL 3**: 1984 - Funcționalitatea Office Word Processing este un superset al PCL 2. Au fost adăugate funcții pentru producția de documente de înaltă calitate, de birou și a crescut dpi până la 300 dpi. A permis utilizarea unui număr limitat de fonturi bitmap și grafică și a acceptat HP-GL. PCL 3 a fost imitat pe scară largă de alți producători de imprimante și a fost numit de aceste companii „LaserJet Plus Emulation”.
(Imprimante: familia HP DeskJet, imprimantă din seria HP LaserJet, imprimantă din seria HP LaserJet Plus)

**PCL3+:** Folosit de familia de imprimante DeskJet și DesignJet.

**PCL3c:** Folosit de familia de imprimante DeskJet și DesignJet.

**PCL3e**: Folosit de familia de imprimante DeskJet și DesignJet. Acum este folosit și în PhotoSmart.

**PCL3GUI**: Utilizează RTL și este utilizat de familia de imprimante DeskJet și DesignJet.

**PCLSLEEK**: Utilizează RTL și este folosit de familia de imprimante DeskJet și DesignJet.

**PCL 4**: 1985 - Funcționalitatea de formatare a paginii este un superset al PCL 3. Macro-uri acceptate, fonturi bitmap mai mari și grafică. (Imprimante: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Funcționalitatea Office Publishing este un superset al PCL 4. Noile capabilități de publicare includ scalarea fonturilor și grafica HP-GL/2 (vectorală). (Imprimante: HP LaserJet III)

**PCL 5e:** 1994 - Aceasta este o revizuire majoră, care include noi caracteristici precum Sistemul de compresie adaptivă, codificarea caracterelor pe 2 octeți, suport pentru fonturi vectoriale și comenzi de configurare bidirecțională. Include operații logice (corespunde cu ROP-urile GDI) pentru a îmbunătăți suportul Windows înainte de a tăia traseele. (Imprimante: HP LaserJet 4)

**PCL 5j:** Caracteristici noi, cum ar fi suport pentru caractere de 2 octeți pentru fonturi scalabile rezidente japoneze, scriere verticală, dimensiuni de hârtie japoneze și șiruri de caractere. (Imprimante: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Suportul culorilor și operațiunile logice au fost adăugate la PCL5. PCL5c precede PCL5e. Unele modele acceptă și trasee de tăiere. (Imprimante: HP Color LaserJet, HP PaintJet 300 XL (prima imprimantă cu PCL5c), HP DeskJet 1200C/1600C (aceste numere de model au fost refolosite, iar modelele mai noi nu sunt PCL 5c)

**PCL 5ce:** Suportă fonturi scalabile Agfa Microtype. (Imprimante: HP 2500c Pro Printer)

**PCL 6 / XL:** 1996 - PCL 6 sau PCL XL este un nou format introdus în 1995, care nu este compatibil cu nicio versiune anterioară de PCL. (Imprimante: HP LaserJet 5, 5M și 5N)

## Prezentare generală PCL 6 ##

HP a introdus PCL 6 în 1996, care a fost următoarea evoluție a limbajului PCL și a tehnologiilor conexe. Are următoarele componente:

**PCL 6 Enhanced:** oferă o versiune optimizată pentru imprimare din interfețe grafice cu utilizatorul (GUI) precum MS Windows și OS/2

**PCL 6 Standard:** oferă compatibilitate completă cu imprimantele HP LaserJet anterioare

**PCL Font Synthesis:** oferă fonturi scalabile, gestionarea fonturilor și stocarea formularelor și a fonturilor.

Versiunea extinsă PCL XL este mai aproape de GDI pe care o folosesc multe aplicații. Se asigură că au loc mai puține traduceri, ceea ce duce la capacități WYSIWYG crescute și o performanță mai bună cu aplicațiile care acceptă evadările implementate de driverul îmbunătățit. Ieșirea din driverul îmbunătățit (PCL XL) poate să nu fie aceeași cu ieșirea din driverul standard. Dacă rezultatul nu este cel așteptat, alegeți driverul Standard (PCL5e).

Comenzile PCL 6 Enhanced sunt concepute pentru a se potrivi optim cu cerințele de imprimare grafică pentru aplicațiile bazate pe GUI. În cele mai multe cazuri, pentru fiecare comandă de imprimare grafică pe care o interfață grafică dorește să o execute, există o comandă PCL 6 Enhanced corespunzătoare. Acest lucru reduce numărul de comenzi necesare pentru a descrie o pagină grafică. Fiecare comandă din PCL 6 Enhanced este concepută pentru a necesita un transfer minim de date de la computerul gazdă la imprimantă. Acest lucru reduce cantitatea de date necesare pentru a descrie o pagină.

Sistemul de imprimare Windows pentru majoritatea imprimantelor HP LaserJet oferă două drivere separate: standard și îmbunătățit. Driverul Standard oferă compatibilitate inversă prin utilizarea comenzilor PCL 6 Standard (PCL5e) pentru a imprima text simplu sau pagini mixte de text și grafică. Driverul Enhanced utilizează comenzile PCL 6 Enhanced care au fost optimizate pentru imprimarea paginilor grafice complexe.

## Revizuirile clasei PCL 6 ##

#### Clasa 1.1 ####

**Instrumente de desen:** Suportă linii de desenare, arce/elipse/coarde, dreptunghiuri (rotunjite), poligoane, trasee Bezier, trasee tăiate, imagini raster, linii de scanare, operații raster.
**Manevrarea culorilor:** Suport palete de 1/4/8 biți, spațiu de culoare RGB/gri. Suportă modele de semiton personalizate (maximum 256 de modele).
**Compresie:** Suportă RLE.
**Unități de măsură:** Inch, milimetru, zecime de milimetru.
**Manevrarea hârtiei:** acceptă seturi personalizate sau predefinite de tipuri de hârtie, inclusiv Letter, Legal, A4 etc. Hârtia poate fi duplexă orizontal sau vertical. Hârtia poate fi orientată în portret, peisaj sau rotație de 180 de grade față de primele două.
**Font:** acceptă fonturi bitmap sau TrueType, puncte de cod pe 8 sau 16 biți. Alegerea setului de caractere utilizează un cod de set de simboluri diferit de PCL 5. Când se utilizează font bitmap, multe comenzi de scalare nu sunt disponibile. Când se utilizează font TrueType, descriptorii de lungime variabilă, blocurile de continuare nu sunt acceptate. Fontul contur poate fi rotit, scalat sau tăiat.

#### Clasa 2.0 ####

**Compresie:** S-a adăugat o compresie JPEG proprietară numită JetReady.
**Manipularea hârtiei:** Suporturile pot fi redirecționate către diferite recipiente de ieșire (până la 256). S-au adăugat dimensiuni media presetate A6 și japoneză B6. A fost adăugată a treia casetă presetată, 248 de surse media externe pentru tavă.
**Font:** Textul poate fi scris pe verticală.

#### Clasa 2.1 ####

**Manevrarea culorilor:** A fost adăugată funcția de potrivire a culorilor.
**Compresie:** S-a adăugat Delta Row.
**Manevrarea hârtiei:** Orientarea, dimensiunea suportului sunt opționale atunci când declarați o pagină nouă. S-au adăugat tipuri de hârtie B5, JIS 8K, JIS 16K, JIS Exec.

#### Clasa 3.0 ####

**Manevrarea culorilor:** Permite utilizarea diferitelor setări de semitonuri pentru grafică vectorială sau raster, text. Sprijină semi-tonarea adaptivă.
**Protocol:** acceptă trecerea PCL, permițând ca funcțiile PCL 5 să fie utilizate de fluxurile PCL 6. Cu toate acestea, unele stări PCL 6 nu sunt păstrate atunci când se utilizează această caracteristică.
**Font:** acceptă fonturi PCL.
**Vizualizator/Convertor:** PCLReader (freeware) poate vizualiza, converti sau imprima orice nivel de PCL 6 (inclusiv JetReady) pe orice imprimantă.

## Referințe ##

* [PCL - Prin Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)

