{
  "date" : "2019-10-11",
  "keywords" :[ "rtf-fil", "rtf-filformat", "vad är en rtf-fil", "fil", "rtf-exempel", "rtf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Rich Text Format",
  "description":"Läs mer om RTF-filformat och API:er som kan skapa och öppna RTF-filer.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är RTF fil?

Introducerat och dokumenterat av Microsoft representerar Rich Text Format (**RTF**) en metod för att koda formaterad text och grafik för användning i applikationer. Formatet underlättar plattformsoberoende dokumentutbyte med andra Microsoft-produkter, vilket tjänar syftet med interoperabilitet. Denna förmåga gör det till en standard för dataöverföring mellan ordbehandlingsprogram och därför kan innehåll överföras från ett operativsystem till ett annat utan att förlora dokumentformateringen. Filformatspecifikationerna är tillgängliga av Microsoft för offentlig [nedladdning](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) och kan refereras till från utvecklarens perspektiv.

## Kort historik över RTF-filformat ##

RTF-filformatet har genomgått flera revisioner sedan det publicerades. Dess officiella version för läs/skriva publicerades som en del av Microsoft Word 3.0 för Macintosh med version 1.0-specifikationer. Den slutliga versionen av specifikationerna, 1.9.1, publicerades av Microsoft i mars 2008. Inga fler förbättringar av specifikationerna görs efter detta. För närvarande har nästan alla operativsystem fler funktionsrika applikationer som har minimerat/utrotat användningen av RTF-filformat.

## RTF-filformatspecifikationer ##

RTF fungerar som en standard för dataöverföring mellan ordbehandlingsprogram och överföring av innehåll från ett operativsystem till ett annat. Detta uppnås med hjälp av kontrollord som introducerades av Microsoft Office Word fram till 2007. En standard RTF-fil består av ASCII för att representera rik text och med icke-ASCII-tecken som konverteras till lämpliga kodvärden. Nyare versioner av Word kan läsa RTF-filer som genererats med tidigare versioner, medan de äldre versionerna ignorerar kontrollord och grupper som de inte förstår.

### Förstå grunderna för RTF ###

RTF-filer använder 7-bitars ASCII-oformaterad text, bestående av:

* kontrollord
* kontrollsymboler och
* grupper.

Dessa fungerar som byggstenar för representation av RTF-data som begriplig text och teckenkodning.

#### Kontrollord ####

Dessa representerar speciellt formaterade kommandon som används för att markera tecken för visning och kan inte vara längre än 32 bokstäver. Ett kontrollord definieras av:

\<ASCII Letter Sequence> //<//Delimiter//> //

Varje kontrollord är skiftlägeskänsligt och börjar med ett snedstreck. ASCII-bokstavssekvensen kan innehålla ASCII-alfabet (a till z och A till Z). De<Delimite> markerar slutet på kontrollordets namn och kan vara något av följande:

* Ett utrymme. Detta tjänar endast till att avgränsa ett styrord och ignoreras vid efterföljande bearbetning.
* En numerisk siffra eller ett ASCII-minustecken, vilket indikerar att en numerisk parameter är associerad med kontrollordet. Den efterföljande digitala sekvensen avgränsas sedan av något annat tecken än en ASCII-siffra (vanligtvis ett annat kontrollord som börjar med ett snedstreck). Parametern kan vara ett positivt eller negativt decimaltal. Värdeintervallet för talet är nominellt –32768 till 32767, dvs ett 16-bitars heltal med tecken. Ett litet antal kontrollord tar värden i intervallet −2,147,483,648 till 2,147,483,647 (32-bitars heltal med tecken). Dessa kontrollord inkluderar **\binN**, **\revdttmN//**, **\rsidN** relaterade kontrollord och vissa bildegenskaper som **\bliptagN**. Här står **N** för den numeriska parametern. En RTF-parser måste tillåta upp till 10 siffror som eventuellt föregås av ett minustecken. Om avgränsaren är ett mellanslag kasseras det, det vill säga det ingår inte i efterföljande bearbetning.
* Alla tecken förutom en bokstav eller en siffra. I detta fall avslutar det avgränsande tecknet kontrollordet och är inte en del av kontrollordet. Som ett omvänt snedstreck "\", vilket betyder att ett nytt kontrollord eller en kontrollsymbol följer.

#### Kontrollsymbol ####

En kontrollsymbol representerar en speciell händelse som har specifik betydelse beroende på dess innehåll. Den består av ett omvänt snedstreck följt av ett specialtecken (icke-alfabetisk tecken) och har inga avgränsare.

#### Grupp ####

En grupp kan bestå av text, kontrollord eller kontrollsymboler omslutna av klammerparenteser (**{ }**). Den öppna klammerparentesen (**{** ) indikerar gruppens början och den avslutande klammerparentesen ( **}**) indikerar slutet på gruppen. Varje grupp specificerar texten som påverkas av gruppen och de olika attributen för den texten.

### RTF-filstruktur ###

En RTF-fil har följande standardsyntax:

Introducerat och dokumenterat av Microsoft representerar Rich Text Format (**RTF**) en metod för att koda formaterad text och grafik för användning i applikationer. Formatet underlättar plattformsoberoende dokumentutbyte med andra Microsoft-produkter, vilket tjänar syftet med interoperabilitet. Denna förmåga gör det till en standard för dataöverföring mellan ordbehandlingsprogram och därför kan innehåll överföras från ett operativsystem till ett annat utan att förlora dokumentformateringen. Filformatspecifikationerna är tillgängliga av Microsoft för offentlig [nedladdning](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) och kan refereras till från utvecklarens perspektiv.

#### RTF Header ####

En RTF Header har följande representation.

|Fält|Beskrivning
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Rubriktabeller måste visas i denna ordning om de finns. RTF-filen kan innehålla grupper för typsnitt, stilar, skärmfärg, bilder, fotnoter, kommentarer (kommentarer), sidhuvuden och sidfötter, sammanfattningsinformation, fält, bokmärken, dokument-, avsnitts-, stycke- och teckenformateringsegenskaper, matematik, bilder och föremål. Om teckensnitt, fil, stil, färg, revisionsmärke och sammanfattningsinformationsgrupper och dokumentformateringsegenskaper ingår i filen, måste de visas i RTF-huvudet, som föregår RTF-kroppen. Om innehållet i någon grupp inte används kan gruppen utelämnas. Alla grupper som använder egenskaperna definierade i en annan grupp måste visas efter gruppen som definierar dessa egenskaper. Till exempel måste färg- och teckensnittsegenskaper föregå stilgruppen.

#### RTF-version ####

Ett RTF-dokument måste börja med dessa sex tecken:

```
{\rtf1
```
där 1:an visar RTF-versionsnumret.

#### Teckenuppsättning ####

Efter {\rtf1 ska dokumentet deklarera vilken teckenuppsättning det använder. Sättet att deklarera en teckenuppsättning är med ett av dessa kommandon:

`\ansi` - Dokumentet finns i ANSI-teckenuppsättningen, även känd som Code Page 1252, den vanliga MSWindows-teckenuppsättningen.

`\mac` - Dokumentet finns i MacAscii-teckenuppsättningen, den vanliga teckenuppsättningen under gamla (före 10) versioner av Mac OS.

`\pc` - Dokumentet är i DOS-kod Sida 437, standardteckenuppsättningen för MS-DOS. Maskinskrivare med bra muskelminne kommer att notera att detta är den teckenuppsättning som fortfarande används för att tolka "Alt numeriska" koder - dvs när du håller ned Alt och skriver "130" på det numeriska tangentbordet, producerar det ett é, eftersom tecken 130 i CP437 är ett é. Det är ungefär den enda användning som CP437 ser nuförtiden.

`\pca` - Dokumentet finns i DOS-kod Sida 850, även känd som MS-DOS Multilingual Code Page.

#### Font Kommando ####

Teckenuppsättningsdefinitionen följs av kommandot `\deffN`. Detta definierar att teckensnittsnumret N är standardteckensnittet för detta dokument. Teckensnittsnumret N refereras från teckensnittstabellen. Kommandot `\deffN` är tekniskt valfritt, men det borde finnas där för att vara på den säkra sidan som en vanlig prolog som att följa teckensnitt 0 som standardteckensnitt.

`{\rtf1\ansi\deff0`

#### Teckensnittstabell ####

Alla teckensnitt som kan användas i ett dokument listas i en teckensnittstabell där varje teckensnitt representeras av ett teckensnittsnummer. Dokument måste ha en teckensnittstabell även om vissa program fungerar utan det också.

Syntaxen för en teckensnittstabell är {\fonttbl //...declarations//...}, där varje deklaration har denna grundläggande syntax:

`{\fnumber\familycommand Fontname;}`

En teckensnittstabell med fyra deklarationer är följande:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

I ett dokument med den teckensnittstabellen skulle `{\f2 stuff}` skriva ut "grejer" i Courier New. Ett teckensnitt kan inte användas i ett dokument förrän det finns med i teckensnittstabellen.

### Slut på dokument ###

Varje RTF-dokument måste sluta med en } för att stänga gruppen som öppnas av { som är det första tecknet i dokumentet. Ingenting kan följa den sista }, förutom möjligen en nyrad.

## Referenser ##

* [RTF 1.9.1-specifikationer](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)
* [Rich Text Format](https://en.wikipedia.org/wiki/Rich_Text_Format)

