{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICS — iCalendar faila formāts",
  "description": "Uzziniet par ICS failu formātu un API, kas var izveidot un atvērt ICS failus.",
  "linktitle": "ICS",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ic-lvs"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir ICS fails?

Interneta kalendāra un plānošanas pamatobjekta specifikācija (iCalendar) ir interneta standarts (RFC 2445) kalendāra notikumu un plānošanas apmaiņai un izvietošanai. iCalendar formāts ir sadarbspējīgs, tādējādi nodrošinot kalendāra informācijas apmaiņu starp lietotājiem, kuriem ir dažādas e-pasta lietojumprogrammas. iCalendar formatē ievades datus kā daudzfunkcionālus interneta pasta paplašinājumus (MIME) un atvieglo objektu apmaiņu, izmantojot dažādus transporta protokolus. Šie transporta protokoli var būt SMTP, HTTP, asinhronā saziņa no punkta uz punktu un fizisku mediju tīkla transportēšana.

iCalendar ļauj lietotājiem koplietot notikumus, no datuma/laika atkarīgus uzdevumus un informāciju par brīvu/aizņemtību, izmantojot e-pastu, citiem lietotājiem, kuri var atbildēt. iCalendar faili tiek uzglabāti, izmantojot sufiksus .ics .iCalendar vai .ifb ar MIME veidu text/calendar. iCalendar tiek uzturēts tā, lai tas būtu neatkarīgs bez transporta protokola atkarības. Tīmekļa serveri (ar HTTP protokolu) var pārsūtīt iCalendar informāciju, un tīmekļa lapas var saturēt iCalendar datus iegultā veidā, izmantojot iCalendar.

## Īsa ICS faila formāta vēsture

In 1998, the Internet Engineering Task Force (IETF) defined iCalendar as a standard (RFC 2445). The standard was documented by Frank Dawson(Lotus Notes Corporation) and Derik Stenerson ( Microsoft). In 2009, the standard was again refined by Bernard Desruisseaux (Oracle) as RFC 5545. Šoreiz tika pievienotas dažas jaunas funkcijas un dažas novecojušas funkcijas tika novecojušas. 2016. gadā tika izlaists RFC 7986 un papildināts ar sākotnējo iCalendar RFC. RFC 7986 pievienoja jaunus raksturlielumus galvenajam VCALENDAR objektam, un tika ieviesti arī jauni atbalsta līdzekļi konferenču sistēmām.

## ICS faila formāts ##

MIME veids, ko izmanto iCalendar datos, ir text/calendar”. iCalendar noklusējuma rakstzīmju kopa ir UTF-8, taču, nodrošinot parametrus MIME, var izmantot citu rakstzīmju kopu. iCalendar failā ir sadaļas, starp šīm sadaļām VCALENDAR ir globālā sadaļa, kas ietver visas pārējās sadaļas. VEVENT sadaļa nosaka notikumus, VTODO uzskaita visus uzdevumus, VJOURNAL satur žurnāla ierakstus un VTIMEZONE norāda laika joslas informāciju. ir atļautas vairākas līdzīgas kategorijas sadaļas. Daudziem pasākumiem iCalendar failā var būt vairākas VEVENT sadaļas.

### Satura līnijas ###

iCalendar objekti ir sakārtoti atšķirīgās teksta rindās satura rindās. Šajā faila formātā CRLF secība beidz rindu, savukārt līnijas garums ir ierobežots līdz 75 oktetiem, neskaitot rindiņas pārtraukumu. Garu datu vienumu var aptvert daudzās rindās.

### Sarakstu un lauku atdalītāji ###

Rekvizīti un parametri norāda vērtību sarakstu, kas ir atdalītas ar komatu. Pēdinātās virknes tiek izmantotas parametru vērtībām, kuru pamatā ir URI. Parametru sarakstu var izveidot pēc īpašuma vērtības. Katrs rekvizīta parametrs šajā sarakstā ir jāatdala ar SEMIKOLU.

Vērtību sarakstā SEMIKOLONS izdala rekvizītu parametrus un KOMATS atdala rekvizītu vērtības. Piemērs ir dots zemāk:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Vairākas vērtības

Dažiem rekvizītiem var būt vairākas vērtības. Vairāku vērtību rekvizītu pamatnoteikums ir vienkārša jaunas satura rindiņas ģenerēšana ar rekvizīta nosaukumu. Tomēr vienai vērtībai ar vairākām valodu variācijām nedrīkst izmantot rekvizītus ar vairākām vērtībām.

### Binārais saturs

iCalendar objektā rekvizīta vērtība var atsaukties uz binārā satura datiem, kas ievietoti ārējā MIME entītijā, izmantojot URI. Iekļauto bināro saturu var izmantot īpašās situācijās ar parametru ENCODING, kur lietojumprogrammai ir jāizsaka iCalendar objekts kā vienīgā entītija. Šis piemērs izskaidro rekvizītu ATTACH ar URI atsauci:

ATTACH: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Rakstzīmju kopa

Lai gan iCalendar noklusējuma rakstzīmju kopas shēma ir UTF-8, tomēr nav norādīts rekvizīta parametrs, lai definētu rekvizīta vērtības rakstzīmju kopu. MIME pārsūtījumos esošajai rakstzīmju kopai OBLIGĀTI jāizmanto parametrs charset.

## Kā atvērt ICS failu?

Ir vairāki veidi, kā atvērt ICS failu. Tie ir sīkāk aprakstīti zemāk.

1. Atveriet ICS, izmantojot kalendāra lietojumprogrammas

Varat atvērt ICS failus, izmantojot kalendāra lietojumprogrammas, piemēram, Microsoft Outlook, Google Calendar vai Apple Calendar. Ja jūsu ierīcē ir instalētas šīs lietojumprogrammas, varat atvērt ICS failu ar šīm lietojumprogrammām, vienkārši veicot dubultklikšķi uz tā. Tādējādi ICS faila notikumi tiks importēti jūsu kalendārā.

1. Atveriet ICS failu teksta redaktorā

Varat arī atvērt ICS failu jebkurā teksta redaktorā, piemēram, Microsoft Notepad vai Apple TextEdit. Pēc atvēršanas jūs redzēsit DTSTART un DTEND rindas, kas atspoguļo notikuma sākuma un beigu laiku.

1. Manuāli importējiet ICS failu lietotnē Kalendārs

Varat arī manuāli importēt ICS failu savā kalendāra lietotnē, izmantojot šo kalendāra programmu Imiprot un eksportēšanas opcijas. Tādējādi jūsu kalendāram tiks pievienoti ICS faila notikumi.

## Atsauces

* [Interneta kalendāra un plānošanas pamatobjekta specifikācija](https://www.ietf.org/rfc/rfc5545.txt)

* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)

* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)


