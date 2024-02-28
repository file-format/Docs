{
  "date": "2019-10-11",
  "keywords": [
"rtf fil",
"rtf filformat",
"hvad er en rtf-fil",
"fil",
"rtf eksempel",
"rtf filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RTF - Rich Text Format",
  "description": "Lær om RTF-filformat og API'er, der kan oprette og åbne RTF-filer.",
  "linktitle": "RTF",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-rt-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en RTF fil?

Introduceret og dokumenteret af Microsoft, Rich Text Format (**RTF**) repræsenterer en metode til kodning af formateret tekst og grafik til brug i applikationer. Formatet letter dokumentudveksling på tværs af platforme med andre Microsoft-produkter, hvilket tjener interoperabilitetsformålet. Denne egenskab gør det til en standard for dataoverførsel mellem tekstbehandlingssoftware, og derfor kan indhold overføres fra et operativsystem til et andet uden at miste dokumentformatering. Filformatspecifikationerne er tilgængelige af Microsoft for offentlige download og kan henvises til fra udviklerens perspektiv.

## Kort historie om RTF-filformat ##

RTF file format has underwent several revisions since its publication. Its official version for read/write was published as part of Microsoft Word 3.0 for Macintosh with version 1.0 specifications. The final version of specifications, 1.9.1 was published by Microsoft in Mar 2008. Der foretages ikke flere forbedringer af specifikationerne efter dette. På nuværende tidspunkt har næsten alle operativsystemer mere funktionsrige applikationer, der har minimeret/udryddet brugen af RTF-filformat.

## RTF-filformatspecifikationer ##

RTF serves as a standard of data transfer between word processing software and transfer of content from one operating system to another. This is achieved using control words that were introduced by Microsoft Office Word up through 2007. En standard RTF-fil består af ASCII til at repræsentere rig tekst og med ikke-ASCII-tegn, der konverteres til passende kodeværdier. Nyere versioner af Word kan læse RTF-filer genereret med tidligere versioner, mens de ældre versioner ignorerer kontrolord og grupper, de ikke forstår.

### Forstå grundlaget for RTF ###

RTF-filer bruger 7-bit ASCII almindelig tekst, bestående af:

* kontrolord

* kontrolsymboler og

* grupper.


Disse fungerer som byggestenene til repræsentation af RTF-data som forståelig tekst- og tegnkodning.

#### Kontrolord ####

Disse repræsenterer specielt formaterede kommandoer, der bruges til at markere tegn til visning og kan ikke være længere end 32 bogstaver. Et kontrolord er defineret ved:

\<ASCII Letter Sequence> //<//Delimiter//> //

Hvert kontrolord skelner mellem store og små bogstaver og starter med en omvendt skråstreg. ASCII-bogstavsekvensen kan indeholde ASCII-alfabeter (a til z og A til Z). Det<Delimite> markerer slutningen af kontrolordets navn og kan være en af følgende:

* Et mellemrum. Dette tjener kun til at afgrænse et styreord og ignoreres ved efterfølgende behandling.

* Et numerisk ciffer eller et ASCII minustegn, som angiver, at en numerisk parameter er knyttet til styreordet. Den efterfølgende digitale sekvens afgrænses derefter af et hvilket som helst andet tegn end et ASCII-ciffer (normalt et andet kontrolord, der begynder med en omvendt skråstreg). Parameteren kan være et positivt eller negativt decimaltal. Området for værdierne for tallet er nominelt –32768 til 32767, dvs. et 16-bit heltal med fortegn. Et lille antal kontrolord har værdier i området −2.147.483.648 til 2.147.483.647 (32-bit heltal med fortegn). Disse kontrolord inkluderer **\binN**, **\revdttmN//**, **\rsidN** relaterede kontrolord og nogle billedegenskaber som **\bliptagN**. Her står **N** for den numeriske parameter. En RTF-parser skal tillade op til 10 cifre, eventuelt foran et minustegn. Hvis afgrænsningstegnet er et mellemrum, kasseres det, det vil sige, at det ikke er inkluderet i den efterfølgende behandling.

* Ethvert tegn bortset fra et bogstav eller et ciffer. I dette tilfælde afslutter det afgrænsende tegn kontrolordet og er ikke en del af kontrolordet. Såsom en omvendt skråstreg "\", hvilket betyder, at et nyt kontrolord eller et kontrolsymbol følger.


#### Kontrolsymbol ####

Et kontrolsymbol repræsenterer en speciel hændelse, der har specifik betydning afhængigt af dens indhold. Den består af en omvendt skråstreg efterfulgt af et specialtegn (ikke-alfabetisk tegn) og har ingen skilletegn.

#### Gruppe ####

En gruppe kan bestå af tekst, kontrolord eller kontrolsymboler omgivet af klammer (**{ }**). Den indledende klammeparentes (**{**) angiver gruppens start, og den afsluttende klammeparentes (**}**) angiver gruppens afslutning. Hver gruppe specificerer den tekst, der er påvirket af gruppen, og de forskellige attributter for denne tekst.

### RTF-filstruktur ###

En RTF-fil har følgende standardsyntaks:

Introduceret og dokumenteret af Microsoft, Rich Text Format (**RTF**) repræsenterer en metode til kodning af formateret tekst og grafik til brug i applikationer. Formatet letter dokumentudveksling på tværs af platforme med andre Microsoft-produkter, hvilket tjener interoperabilitetsformålet. Denne egenskab gør det til en standard for dataoverførsel mellem tekstbehandlingssoftware, og derfor kan indhold overføres fra et operativsystem til et andet uden at miste dokumentformatering. Filformatspecifikationerne er tilgængelige af Microsoft for offentlige download og kan henvises til fra udviklerens perspektiv.

#### RTF-header ####

En RTF-header har følgende repræsentation.

|Felt|Beskrivelse
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Overskriftstabeller skal vises i denne rækkefølge, hvis de findes. RTF-filen kan omfatte grupper for skrifttyper, typografier, skærmfarve, billeder, fodnoter, kommentarer (annoteringer), sidehoveder og sidefødder, oversigtsoplysninger, felter, bogmærker, dokument-, sektions-, afsnits- og tegnformateringsegenskaber, matematik, billeder og genstande. Hvis skrifttype-, fil-, stil-, farve-, revisionsmærke- og resuméinformationsgrupper og dokumentformateringsegenskaber er inkluderet i filen, skal de vises i RTF-headeren, der går forud for RTF-brødteksten. Hvis indholdet af en gruppe ikke bruges, kan gruppen udelades. Enhver gruppe, der bruger de egenskaber, der er defineret i en anden gruppe, skal stå efter den gruppe, der definerer disse egenskaber. For eksempel skal farve- og skrifttypeegenskaber gå forud for typografigruppen.

#### RTF-version ####

Et RTF-dokument skal starte med disse seks tegn:

```
{\rtf1
```
hvor 1 viser RTF versionsnummeret.

#### Tegnsæt ####

Efter {\rtf1 skal dokumentet erklære, hvilket tegnsæt det bruger. Måden at erklære et tegnsæt på er med en af disse kommandoer:

`\ansi` - Dokumentet er i ANSI-tegnsættet, også kendt som Code Page 1252, det sædvanlige MSWindows-tegnsæt.

`\mac` - Dokumentet er i MacAscii-tegnsættet, det sædvanlige tegnsæt under gamle (før-10) versioner af Mac OS.

`\pc` - Dokumentet er i DOS-kode Side 437, standardtegnsættet for MS-DOS. Maskinskrivere med god muskelhukommelse vil bemærke, at dette er det tegnsæt, der stadig bruges til at fortolke Alt numeriske koder - dvs. når du holder Alt nede og skriver 130 på det numeriske tastatur, producerer det et é, fordi tegn 130 i CP437 er et é. Det er omtrent den eneste brug, som CP437 ser i disse dage.

`\pca` - Dokumentet er i DOS Code Side 850, også kendt som MS-DOS Multilingual Code Page.

#### Skrifttypekommando ####

Definitionen af tegnsæt efterfølges af kommandoen `\deffN`. Dette definerer, at skrifttypenummeret N er standardskrifttypen for dette dokument. Skrifttypenummeret N henvises til fra skrifttypetabellen. Kommandoen `\deffN` er teknisk valgfri, men den burde være der for at være på den sikre side som en almindelig prolog som at følge skrifttype 0 som standardskrifttype.

`{\rtf1\ansi\deff0`

#### Skrifttypetabel ####

Alle de skrifttyper, der kan bruges i et dokument, er angivet i en skrifttypetabel, hvor hver skrifttype er repræsenteret med et skrifttypenummer. Dokument skal have en skrifttypetabel, selvom nogle programmer også fungerer uden det.

Syntaksen for en skrifttypetabel er {\fonttbl //...declarations//...}, hvor hver erklæring har denne grundlæggende syntaks:

`{\fnumber\familiekommando skrifttypenavn;}`

En skrifttypetabel med fire erklæringer er som følger:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

I et dokument med den skrifttypetabel ville `{\f2 stuff}` udskrive ting i Courier New. En skrifttype kan ikke bruges i et dokument, før den er angivet i skrifttypetabellen.

### Slut på dokument ###

Hvert RTF-dokument skal slutte med et } for at lukke gruppen, der åbnes af {, der er det første tegn i dokumentet. Intet kan følge den endelige }, undtagen muligvis en ny linje.

## Referencer ##
* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)
