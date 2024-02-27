{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICS - iCalendar-filformat",
  "description": "Lær om ICS-filformat og API'er, der kan oprette og åbne ICS-filer.",
  "linktitle": "ICS",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ic-das"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en ICS fil?

Internet Calendar and Scheduling Core Object Specification (iCalendar) er en internetstandard (RFC 2445) til udveksling og implementering af kalenderbegivenheder og planlægning. iCalendar-formatet er interoperabelt, hvilket sikrer udveksling af kalenderoplysninger mellem brugere, der har forskellige e-mail-applikationer. iCalendar formaterer inputdataene som en Multipurpose Internet Mail Extensions (MIME) og letter objektet, der udveksles via forskellige transportprotokoller. Disse transportprotokoller kan være SMTP, HTTP, punkt-til-punkt asynkron kommunikation og fysisk mediebaseret netværkstransport.

iCalendar giver brugerne mulighed for at dele begivenheder, dato/tidsafhængige opgaver og ledig/optaget information via e-mails til andre brugere, der kan svare tilbage. iCalendar-filer gemmer ved hjælp af suffikserne .ics .iCalendar eller .ifb med en MIME-type tekst/kalender. iCalendar holdes til at være selvhjulpen uden nogen transportprotokolafhængighed. Webservere (med HTTP-protokol) kan transportere iCalendar-oplysninger, og websider kan indeholde iCalendar-data i indlejret form ved hjælp af iCalendar.

## Kort historie om ICS-filformat

In 1998, the Internet Engineering Task Force (IETF) defined iCalendar as a standard (RFC 2445). The standard was documented by Frank Dawson(Lotus Notes Corporation) and Derik Stenerson ( Microsoft). In 2009, the standard was again refined by Bernard Desruisseaux (Oracle) as RFC 5545. Denne gang blev nogle nye funktioner tilføjet, og nogle forældede funktioner blev udfaset. I 2016 blev RFC 7986 udgivet og udvidet til original iCalendar RFC. RFC 7986 tilføjede nye egenskaber til VCALENDAR-hovedobjektet, og nye understøttende funktioner blev også introduceret til konferencesystemer.

## ICS-filformat ##

MIME-typen, der bruges af dataene i iCalendar, er tekst/kalender. Standardtegnsæt for iCalendar er UTF-8, men ved at angive parametre i MIME kan et andet tegnsæt bruges. En iCalendar-fil indeholder sektioner, blandt disse sektioner VCALENDAR, er den globale sektion, der indkapsler alle andre sektioner. VEVENT-sektionen definerer hændelser, VTODO viser alle to-do-punkter, VJOURNAL indeholder journalposter, og VTIMEZONE angiver information om tidszone. flere sektioner af lignende kategori er tilladt. For adskillige begivenheder kan flere VEVENT-sektioner være til stede i en iCalendar-fil.

### Indholdslinjer ###

iCalendar-objekterne er arrangeret i særskilte tekstlinjer indholdslinjer. I dette filformat afslutter CRLF-sekvensen en linje, hvorimod linjelængden er begrænset til 75 oktetter eksklusive linjeskiftet. Et langt dataelement kan spændes over mange linjer.

### Liste- og feltseparatorer ###

Egenskaber og parametre angiver en liste over værdier, der er adskilt af et KOMMA-tegn. Anførte strenge bruges til URI-baserede parameterværdier. Liste over parametre kan konstrueres af egenskabsværdien. Hver egenskabsparameter i denne liste skal adskilles af et SEMIKOLON.

I en værdiliste isolerer et SEMICOLON egenskabsparametre og et KOMMA separate egenskabsværdier. Eksempel er givet nedenfor:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Flere værdier

Nogle egenskaber kan have flere værdier. Blot at generere en ny indholdslinje med ejendomsnavnet er den grundlæggende regel for ejendomme med flere værdier. For en enkelt værdi med flere sprogvariationer må der dog ikke bruges egenskaber med flere værdier.

### Binært indhold

Inden for et iCalendar-objekt kan egenskabsværdien referere til binære indholdsdata placeret i en ekstern MIME-entitet ved hjælp af en URI. Inline binært indhold kan bruges i specielle situationer med parameteren ENCODING, hvor applikationen skal udtrykke et iCalendar-objekt som en eneste enhed. Følgende eksempel forklarer en ATTACH-egenskab med en URI-reference:

ATTACH: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Tegnsæt

Selvom standardtegnsætskemaet for en iCalendar er UTF-8, er der dog ingen egenskabsparameter angivet til at definere tegnsættet for en egenskabsværdi. i MIME-overførsler SKAL parameteren charset bruges til eksisterende tegnsæt.

## Hvordan åbner man en ICS fil?

Der er flere måder at åbne en ICS-fil på. Disse er detaljeret nedenfor.

1. Åbn ICS ved hjælp af kalenderapplikationer

Du kan åbne ICS-filer ved hjælp af kalenderprogrammer såsom Microsoft Outlook, Google Kalender eller Apple Kalender. Hvis du har disse programmer installeret på din enhed, kan du åbne ICS-filen med disse programmer ved blot at dobbeltklikke på den. Dette vil importere begivenhederne i ICS-filen til din kalender.

1. Åbn ICS-fil i teksteditor

Du kan også åbne en ICS-fil i en hvilken som helst teksteditor, såsom Microsoft Notesblok eller Apple TextEdit. Når den er åbnet, vil du se linjerne DTSTART og DTEND, der repræsenterer start- og sluttidspunkterne for begivenheden.

1. Importer ICS-fil manuelt i Kalender-appen

Du kan også manuelt importere en ICS-fil til din kalenderapp ved at bruge Imiprot- og eksportmulighederne for disse kalenderapps. Dette vil tilføje ICS-filbegivenhederne til din kalender.

## Referencer

* [Internetkalender og planlægning af kerneobjektspecifikation](https://www.ietf.org/rfc/rfc5545.txt)

* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)

* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)


