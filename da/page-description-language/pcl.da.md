{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCL",
  "description": "Lær om PCL-filformat og API'er, der kan oprette og åbne PCL-filer.",
  "linktitle": "PCL",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-pc-dal"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en PCL fil? ##

PCL står for Printer Command Language, som er et sidebeskrivelsessprog introduceret af Hewlett Packard (HP). HP skabte PCL for at give en effektiv måde at kontrollere printerfunktioner på tværs af mange forskellige udskrivningsenheder. Formatet er oprindeligt udviklet til HP's matrix- og inkjet-printere, men har med tiden været en del af forskellige termo-, matrix- og sideprintere. Formatet gennemgik flere forskellige revisioner, hvilket resulterede i forskellige versioner, hvor hver version blev forbedret for at opfylde tidens krav med hensyn til printerens kontrolfunktioner. I dag er PCL det mest udbredte printersprog på markedet for lasterprintere.

## PCL-versioner ##

PCL-versioner adskiller sig i funktionalitet (f.eks. understøttelse af skrifttype: bitmapskrifttyper, skalerbare skrifttyper (Intellifonts, TrueType-skrifttyper), rastergrafikkomprimeringsmetoder, HP-GL/2-grafikunderstøttelse).

**PCL 1:** omkring 1980 - Print- og Space-funktionalitet er basissættet af funktioner, der er tilvejebragt for enkel, bekvem, enkeltbruger-workstation-output.

**PCL 2:** around 1980 - EDP (Electronic Data Processing)/Transaction functionality is a superset of PCL 1. Funktioner blev tilføjet til generelle formål, multi-user system print.

**PCL 3**: 1984 - Office Word Processing functionality is a superset of PCL 2. Funktioner blev tilføjet til højkvalitets, kontordokumentproduktion og øget dpi op til 300 dpi. Det tillod brugen af et begrænset antal bitmapskrifttyper og grafik og understøttede HP-GL. PCL 3 blev i vid udstrækning efterlignet af andre printerproducenter og blev af disse virksomheder omtalt som LaserJet Plus-emulering.
(Printere: HP DeskJet familie, HP LaserJet serie printer, HP LaserJet Plus serie printer)

**PCL3+:** Bruges af DeskJet og DesignJet familie af printere.

**PCL3c:** Bruges af DeskJet og DesignJet familie af printere.

**PCL3e**: Bruges af DeskJet og DesignJet familie af printere. Bruges nu også i PhotoSmart.

**PCL3GUI**: Bruger RTL og bruges af DeskJet og DesignJet familie af printere.

**PCLSLEEK**: Bruger RTL og bruges af DeskJet og DesignJet familie af printere.

**PCL 4**: 1985 - Page formatting functionality is a superset of PCL 3. Understøttede makroer, større bitmapskrifttyper og grafik. (Printere: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing functionality is a superset of PCL 4. Nye udgivelsesmuligheder omfatter skrifttypeskalering og HP-GL/2 (vektor) grafik. (Printere: HP LaserJet III)

**PCL 5e:** 1994 - Dette er en større revision, som inkluderer nye funktioner som Adaptive Compression System, 2byte tegnkodning, understøttelse af vektorskrifttyper og tovejskonfigurationskommandoer. Indeholder logiske operationer (svarer til GDI ROP'er) for at forbedre Windows-understøttelse før fritlægning. (Printere: HP LaserJet 4)

**PCL 5j:** Nye funktioner som 2-byte-tegnunderstøttelse af skalerbare skrifttyper, der er hjemmehørende i Japan, lodret skrift, japanske papirstørrelser og skrifttypestrenge. (Printere: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Colour support and Logical Operations was added to PCL5. PCL5c predates PCL5e. Some models also support clipping paths. (Printers: HP Colour LaserJet, HP PaintJet 300 XL (first printer with PCL5c), HP DeskJet 1200C/1600C (these model numbers have been re-used and the newer models are not PCL 5c)

**PCL 5ce:** Understøtter Agfa Microtype skalerbare skrifttyper. (Printere: HP 2500c Pro-printer)

**PCL 6 / XL:** 1996 - PCL 6 eller PCL XL er et nyt format introduceret i 1995, som ikke er kompatibelt med nogen tidligere versioner af PCL. (Printere: HP LaserJet 5, 5M og 5N)

## PCL 6-oversigt ##

HP introducerede PCL 6 i 1996, som var den næste udvikling af PCL-sproget og relaterede teknologier. Den har følgende komponenter:

**PCL 6 Enhanced:** leverer optimeret version til udskrivning fra grafiske brugergrænseflader (GUI'er) som MS Windows og OS/2

**PCL 6 Standard:** giver komplet bagudkompatibilitet med tidligere HP LaserJet-printere

**PCL Font Synthesis:** leverer skalerbare skrifttyper, skrifttypestyring og opbevaring af formularer og skrifttyper.

Den udvidede version PCL XL er tættere på GDI, som mange applikationer bruger. Det sikrer, at færre oversættelser finder sted, hvilket resulterer i øgede WYSIWYG-kapaciteter og bedre ydeevne med applikationer, der understøtter escapes implementeret af den forbedrede driver. Outputtet fra den forbedrede (PCL XL) driver er muligvis ikke det samme som outputtet fra standarddriveren. Hvis outputtet ikke er som forventet, skal du i stedet vælge standarddriveren (PCL5e).

PCL 6 Enhanced-kommandoer er designet til optimalt at matche grafikudskrivningskravene til GUI-baserede applikationer. I de fleste tilfælde er der for hver grafikudskrivningskommando, som en GUI ønsker at udføre, en matchende PCL 6 Enhanced-kommando. Dette reducerer antallet af kommandoer, der kræves for at beskrive en grafikside. Hver kommando i PCL 6 Enhanced er designet til at kræve minimal dataoverførsel fra værts-pc'en til printeren. Dette reducerer mængden af data, der kræves for at beskrive en side.

Windows-udskrivningssystemet til de fleste HP LaserJet-printere har to separate drivere: Standard og Enhanced. Standarddriveren giver bagudkompatibilitet ved at bruge PCL 6 Standard (PCL5e) kommandoer til at udskrive enkel tekst eller blandede tekst- og grafiksider. Den forbedrede driver bruger PCL 6 Enhanced-kommandoer, der er optimeret til udskrivning af komplekse grafiksider.

## PCL 6 klasserevisioner ##

#### Klasse 1.1 ####

**Tegneværktøjer:** Understøtter tegnelinjer, buer/ellipser/akkorder, (afrundede) rektangler, polygoner, Bezier-stier, klippede stier, rasterbilleder, skanningslinjer, rasteroperationer.
**Farvehåndtering:** Understøtter 1/4/8-bit paletter, RGB/grå farverum. Understøtter brugerdefinerede halvtonemønstre (maks. 256 mønstre).
**Kompression:** Understøtter RLE.
**Måleenheder:** Tommer, millimeter, tiendedel af millimeter.
**Papirhåndtering:** Understøtter brugerdefinerede eller foruddefinerede sæt af papirtyper, inklusive almindelig Letter, Legal, A4 osv. Kan vælge papir fra manuel fremføring, bakker, kassetter. Papir kan duplexes vandret eller lodret. Papir kan orienteres i stående, liggende eller 180 graders rotation af de to førstnævnte.
**Font:** Supports bitmap or TrueType fonts, 8 or 16-bit code points. Choosing character set uses different symbol set code from PCL 5. Når der bruges bitmapskrifttype, er mange skaleringskommandoer ikke tilgængelige. Når TrueType-skrifttype bruges, understøttes beskrivelser med variabel længde, fortsættelsesblokke ikke. Outline-skrifttype kan roteres, skaleres eller klippes.

#### Klasse 2.0 ####

**Kompression:** Tilføjet en proprietær JPEG-komprimering kaldet JetReady.
**Papirhåndtering:** Medier kan omdirigeres til forskellige udskriftsbakker (op til 256). Tilføjet A6 og japansk B6 forudindstillede mediestørrelser. Tilføjet tredje forudindstilling af kassette, 248 eksterne bakke mediekilder.
**Skrifttype:** Tekst kan skrives lodret.

#### Klasse 2.1 ####

**Farvehåndtering:** Tilføjet farvetilpasningsfunktion.
**Kompression:** Tilføjet Delta Row.
**Papirhåndtering:** Orientering, mediestørrelse er valgfri, når du angiver en ny side. Tilføjet B5, JIS 8K, JIS 16K, JIS Exec papirtyper.

#### Klasse 3.0 ####

**Farvehåndtering:** Tillad brug af forskellige halvtoneindstillinger til vektor- eller rastergrafik, tekst. Understøtter adaptiv halvtoning.
**Protocol:** Supports PCL passthrough, allowing PCL 5 features to be used by PCL 6 streams. However, some PCL 6 states are not preserved when using this feature.
**Skrifttype:** Understøtter PCL-skrifttyper.
**Viewer/Converter:** PCLReader (freeware) kan se, konvertere eller udskrive et hvilket som helst niveau af PCL 6 (inklusive JetReady) til enhver printer.

## Referencer ##

* [PCL - af Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)


