{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" : [ "fundamentals" ],
  "description": "Portable Document Format (PDF) er en standardrepræsentation af dokumenter uafhængig af software, hardware og OS. PDF-standarder inkluderer PDF/A, PDF/E, PDF/UA, PDF/VT og PDF/X.",
  "title" : "PDF-filformat - Hvad er en PDF-fil?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
"vægt : 01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) er en type dokument skabt af Adobe tilbage i 1990'erne. Formålet med dette filformat var at indføre en standard for repræsentation af dokumenter og andet referencemateriale i et format, der er uafhængigt af applikationssoftware, hardware samt operativsystem. PDF-filformatet har fuld kapacitet til at indeholde information som tekst, billeder, hyperlinks, formularfelter, rich media, digitale signaturer, vedhæftede filer, metadata, geospatiale funktioner og 3D-objekter i det, der kan blive en del af kildedokumentet.

I de fleste tilfælde konverteres eksisterende dokumenter til PDF i stedet for at oprette en ny PDF fra bunden. Men det betyder ikke, at der ikke er nogen software til oprettelse eller manipulation af PDF-filer.

**(Skal du dele noget om PDF-filformat? Du kan sende dine resultater i afsnittet [PDF File Format News](https://news.fileformat.com/t/PDF).)**

## PDF-filformat - kort historie

En hurtig gennemgang af tidslinjen om [PDF file format](https://products.fileformat.com/pdf/) med hensyn til tidslinjen er som følger:

**1993** - Adobe Systems stillede PDF-specifikationerne til rådighed gratis

**2008** - PDF blev udgivet som en åben standard den 1. juli 2008 og blev udgivet af International Organization for Standardization som **ISO 32000-1:2008**.

**2008** - Adobe udgav en offentlig patentlicens til ISO 32000-1-formatet royaltyfrie rettigheder for alle patenter ejet af Adobe, som er nødvendige for at lave, bruge, sælge og distribuere PDF-kompatible implementeringer.

The first version of PDF designated as PDF 1.0 which later went through revisions up to PDF 1.7. PDF 1.7, som blev til ISO 32000-1, inkluderer nogle ikke-standardiserede proprietære teknologier såvel som Adobe XML Forms Architecture (XFA) og JavaScript-udvidelse til Acrobat. Det var den 28. juli 2017, da PDF 2.0, kendt som ISO 32000-2:2017, blev offentliggjort, som ikke inkluderer nogen ikke-standardiserede teknologier.

## Specifikationer for PDF-filformat

En PDF-fil er et sæt bytes, der kan grupperes i tokens i henhold til syntaksregler defineret af PDF-specifikationer. Én eller flere tokens kombineres for at danne syntaktiske enheder på højere niveau, primært objekter, som er de grundlæggende dataværdier, som et PDF-dokument er konstrueret ud fra.

### Filstruktur af PDF-filer

PDF-filens indhold er arrangeret i følgende rækkefølge inde i filen.

|Overskrift
|Krop
|Krydsreferencetabel
| Trailer

#### PDF-filoverskrift ####

Uanset PDF-versionen starter en PDF-fil med en header, der indeholder en unik identifikator for PDF og versionen af formatet såsom %PDF-1.x, hvor x går fra 1-7.

#### Filtekst ####

Brødteksten i en PDF-fil består af en sekvens af indirekte objekter, der repræsenterer indholdet af et dokument. Objekterne, som beskrevet ovenfor, repræsenterer komponenter af dokumentet, såsom skrifttyper, sider og prøvebilleder. Fra og med PDF 1.5 kan brødteksten også indeholde objektstrømme, som hver indeholder en sekvens af indirekte objekter.

#### Krydsreferencetabel ####

Krydsreferencetabellen indeholder information, der tillader tilfældig adgang til indirekte objekter i filen, således at hele filen ikke skal læses for at finde et bestemt objekt. Tabellen skal indeholde en indtastning på én linje for hvert indirekte objekt, der specificerer byteforskydningen for det pågældende objekt i filens brødtekst. (Begyndende med PDF 1.5 kan nogle eller alle krydsreferenceoplysningerne alternativt være indeholdt i krydsreferencestrømme.

#### File Trailer ####

Traileren til en PDF-fil gør det muligt for en konform læser hurtigt at finde krydsreferencetabellen og visse specielle objekter. Konforme læsere bør læse en PDF-fil fra dens ende. Den sidste linje i filen skal kun indeholde slutningen af filen, %%EOF. De to foregående linjer skal indeholde, én pr. linje og i rækkefølge, nøgleordet startxref og byteforskydningen i den afkodede strøm fra begyndelsen af filen til begyndelsen af xref-nøgleordet i det sidste krydsreferenceafsnit.

### PDF-objekter ###

En PDF-fil indeholder flere forskellige typer objekter, der er af følgende typer

* Booleske værdier - repræsenterer betinget sand eller falsk

* Tal - heltal og reelle værdier

* Strings - indeholder tegn inden for parentes

* Navne - start med et frem/tegn f.eks. /ASomewhatLongerName resulterer i ASomewhatLongerName

* Arrays - PDF understøtter endimensionelle arrays. Arrays med højere dimensioner kan konstrueres ved at bruge arrays som indlejrede elementer

* Ordbøger - samling af objekter som nøgleværdi-par. Den kan have nul indtastninger.

* Streams - repræsenterer sekvens af bytes, som også kan være af ubegrænset længde

* Null Object - repræsenterer en nulværdi


Der kan være andre andre objekter som kommentarer, der introduceres med %-tegnet og kan indeholde 8-bit tegn.

### Indirekte objekter ###

Ethvert objekt i en PDF-fil kan mærkes som et indirekte objekt. Indirekte objekter får en unik objektidentifikator, som andre objekter kan referere til dem. Krydsreferencer til disse opretholdes i en indekstabel og markeres med xref nøgleordet, som følger hovedteksten og giver byte offset for hvert indirekte objekt fra starten af filen.

### Lineære og ikke-lineære PDF-layouts ###

PDF-layout er kategoriseret som Llnær og ikke-lineær afhængigt af målapplikationerne og andre faktorer.

Ikke-lineær - Ikke-lineære PDF-filer bruger mindre diskplads sammenlignet med lineære PDF-filer. PDF-sider af dokumentet ligger spredt ud over PDF-filen, og det er grunden til, at ikke-lineære filer er langsommere sammenlignet med lineære filer.

Lineær PDF - Lineære PDF-filer er rettet mod online PDF-fremvisere, konstrueret på en sådan måde, at de skrives til disken på en lineær måde. Dette kræver ikke browser-plugins for at hele dokumentet skal indlæses først før visning.

### Objektoversigt ###

Som nævnt er PDF body en samling af objekter nævnt ovenfor. PDF er stort set baseret på PostScript uden kontrolfunktionerne i programmeringssprog som if og loop-kommandoer. Kommandoer udstedt af Postscript-kode for at generere grafisk indhold indsamles og tokeniseres ud over eventuelle filer, grafik eller skrifttyper, der henvises til af dokumentet. Alt dette indhold akkumuleres til en enkelt fil, hvilket resulterer i sammensat PostScript-output.

#### Tekst ####

Text in PDF is represented by text elements which are actually displayed with glyphs from fonts.   A  glyph  is  a  graphical  shape  and  is  subject  to  all  graphical  manipulations,  such  as  coordinate transformation. Because of the importance of text in most page descriptions, PDF provides higher-level facilities to describe, select, and render glyphs conveniently and efficiently.

#### Grafik ####

De grafikoperatorer, der bruges i PDF-indholdsstrømme, beskriver udseendet af sider, der skal gengives på en rasteroutputenhed. Faciliteterne er beregnet til både printer- og displayapplikationer. De grafiske operatører udgør seks hovedgrupper:

* Grafiktilstandsoperatører manipulerer datastrukturen kaldet grafiktilstanden, den globale ramme, inden for hvilken de andre grafikoperatører udfører. Grafiktilstanden inkluderer den aktuelle transformationsmatrix (CTM), som kortlægger brugerrumskoordinater, der bruges i en PDF-indholdsstrøm, til outputenhedskoordinater. Det inkluderer også den aktuelle farve, den aktuelle fritlægningssti og mange andre parametre, der er implicitte operander for malerioperatørerne.

* Stikonstruktionsoperatører angiver stier, som definerer former, linjebaner og regioner af forskellig slags. De inkluderer operatorer til at starte en ny sti, tilføje linjesegmenter og kurver til den og lukke den.

* Stimaleroperatører udfylder en sti med en farve, maler en streg langs den eller bruger den som en klippegrænse.

* Andre malerioperatører maler visse selvbeskrivende grafikobjekter. Disse omfatter samplede billeder, geometrisk definerede skygger og hele indholdsstrømme, der igen indeholder sekvenser af grafikoperatorer.

* Text operators select and show character glyphs from fonts (descriptions of typefaces for representing text characters). Because PDF treats glyphs as general graphical shapes, many of the text operators could be grouped with the graphics state or painting operators. However, the data structures and mechanisms for dealing with glyph and font descriptions are sufficiently specialized.
* Marked-content-operatører forbinder logisk information på højere niveau med objekter i indholdsstrømmen. Disse oplysninger påvirker ikke indholdets gengivne udseende; det er nyttigt for programmer, der bruger PDF til dokumentudveksling.


## Referencer ##

* [PDF-filformat: Grundlæggende struktur](https://resources.infosecinstitute.com/topics/hacking/pdf-file-format-basic-structure/)

* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)

* [PDF-reference - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)


