{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar-filformat",
  "description":"Läs mer om ICS-filformat och API:er som kan skapa och öppna ICS-filer.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en ICS fil?

Internet Calendar and Scheduling Core Object Specification (iCalendar) är en internetstandard (RFC 2445) för utbyte och distribution av kalenderhändelser och schemaläggning. iCalendar-formatet är interoperabelt, vilket säkerställer utbyte av kalenderinformation mellan användare som har olika e-postprogram. iCalendar formaterar indata som en Multipurpose Internet Mail Extensions (MIME) och underlättar objektet som utbyts via olika transportprotokoll. Dessa transportprotokoll kan vara SMTP, HTTP, punkt-till-punkt asynkron kommunikation och fysisk mediabaserad nätverkstransport.

iCalendar låter användare dela händelser, datum/tid beroende uppgifter och ledig/upptagen information via e-post till andra användare som kan svara tillbaka. iCalendar-filer lagras med suffixen ".ics" ".iCalendar" eller ".ifb" med MIME-typen "text/kalender". iCalendar hålls för att vara självförsörjande utan något transportprotokollberoende. Webbservrar (med HTTP-protokoll) kan transportera iCalendar-information och webbsidor kan innehålla iCalendar-data i inbäddad form med iCalendar.

## Kort historik över ICS-filformat

1998 definierade Internet Engineering Task Force (IETF) iCalendar som en standard (RFC 2445). Standarden dokumenterades av Frank Dawson (Lotus Notes Corporation) och Derik Stenerson (Microsoft). 2009 förfinades standarden återigen av Bernard Desruisseaux (Oracle) som RFC 5545. Den här gången lades några nya funktioner till och några föråldrade funktioner fasades ut. Under 2016 släpptes RFC 7986 och utökades till original iCalendar RFC. RFC 7986 lade till nya egenskaper till VCALENDAR-huvudobjektet och nya stödjande funktioner introducerades också för konferenssystem.

## ICS-filformat ##

MIME-typen som används av data i iCalendar är "text/kalender". Standardteckenuppsättning för iCalendar är UTF-8, men genom att tillhandahålla parametrar i MIME kan en annan teckenuppsättning användas. En iCalendar-fil innehåller sektioner, bland dessa sektioner är "VCALENDAR", den globala sektionen som kapslar in alla andra sektioner. VEVENT-sektionen definierar händelser, VTODO listar alla att göra-objekt, VJOURNAL innehåller journalanteckningar och VTIMEZONE anger information om tidszon. flera sektioner av liknande kategori är tillåtna. För många evenemang kan flera VEVENT-sektioner finnas i en iCalendar-fil.

### Innehållsrader ###

iCalendar-objekten är ordnade i distinkta textrader "innehållsrader". I detta filformat avslutar CRLF-sekvensen en rad medan radlängden är begränsad till 75 oktetter exklusive radbrytningen. En lång datapost kan spännas över till många rader.

### List- och fältseparatorer ###

Egenskaper och parametrar anger lista över värden som är separerade med ett KOMMA-tecken. Citerade strängar används för URI-baserade parametervärden. Lista över parametrar kan konstrueras av egenskapsvärdet. Varje egenskapsparameter i den här listan måste separeras med ett semikolon.

I en värdelista isolerar ett SEMICOLON egenskapsparametrar och ett COMMA separata egenskapsvärden. Exempel ges nedan:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Flera värden

Vissa egenskaper kan ha flera värden. Att helt enkelt generera en ny innehållsrad med egenskapens namn är grundregeln för fastigheter med flera värden. För ett enskilt värde med flera språkvariationer får dock inte flervärdiga egenskaper användas.

### Binärt innehåll

Inom ett iCalendar-objekt kan egenskapsvärdet referera till en binär innehållsdata placerad i en extern MIME-entitet med hjälp av en URI. Inline binärt innehåll kan användas i speciella situationer med parametern "ENCODING", där applikationen behöver uttrycka ett iCalendar-objekt som en enda enhet. Följande exempel förklarar en "ATTACH"-egenskap med en URI-referens:

BILAGA: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Teckenuppsättning

Även om standardteckenuppsättningsschemat för en iCalendar är UTF-8, har ingen egenskapsparameter specificerats för att definiera teckenuppsättningen för ett egenskapsvärde. i MIME-överföringar MÅSTE "charset"-parametern användas för befintlig charset.

## Referenser

* [Specifikation för kärnobjekt för internetkalender och schemaläggning](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

