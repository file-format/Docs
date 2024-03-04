{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICS – „iCalendar“ failo formatas",
  "description": "Sužinokite apie ICS failo formatą ir API, kurios gali kurti ir atidaryti ICS failus.",
  "linktitle": "ICS",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ic-lts"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra ICS failas?

Interneto kalendoriaus ir planavimo pagrindinio objekto specifikacija (iCalendar) yra interneto standartas (RFC 2445), skirtas keistis ir įdiegti kalendoriaus įvykius bei planuoti. iCalendar formatas yra sąveikus, todėl užtikrinamas keitimasis kalendoriaus informacija tarp vartotojų, turinčių skirtingas el. pašto programas. iCalendar formatuoja įvesties duomenis kaip daugiafunkcinius interneto pašto plėtinius (MIME) ir palengvina apsikeitimą objektu naudojant skirtingus transportavimo protokolus. Šie perdavimo protokolai gali būti SMTP, HTTP, asinchroninis ryšys iš taško į tašką ir fizinės medijos tinklo transportavimas.

iCalendar leidžia vartotojams dalytis įvykiais, nuo datos / laiko priklausančiomis užduotimis ir informacija apie laisvą / užimtą el. laiškais kitiems vartotojams, kurie gali atsakyti. iCalendar failai saugomi naudojant priesagas .ics .iCalendar arba .ifb, o MIME tipas yra text/calendar. iCalendar išlaikomas savarankiškas be jokios transportavimo protokolo priklausomybės. Žiniatinklio serveriai (su HTTP protokolu) gali perduoti iCalendar informaciją, o tinklalapiuose gali būti iCalendar duomenų įterptoje formoje, naudojant iCalendar.

## Trumpa ICS failo formato istorija

In 1998, the Internet Engineering Task Force (IETF) defined iCalendar as a standard (RFC 2445). The standard was documented by Frank Dawson(Lotus Notes Corporation) and Derik Stenerson ( Microsoft). In 2009, the standard was again refined by Bernard Desruisseaux (Oracle) as RFC 5545. Šį kartą buvo pridėta keletas naujų funkcijų, o kai kurios pasenusios funkcijos buvo nebenaudojamos. 2016 m. RFC 7986 buvo išleistas ir papildytas originaliu iCalendar RFC. RFC 7986 pridėjo naujų savybių pagrindiniam VCALENDAR objektui, taip pat buvo pristatytos naujos palaikomosios funkcijos konferencijų sistemoms.

## ICS failo formatas ##

iCalendar duomenų naudojamas MIME tipas yra tekstas / kalendorius. Numatytasis iCalendar simbolių rinkinys yra UTF-8, tačiau nurodant parametrus MIME, galima naudoti kitą simbolių rinkinį. ICalendar faile yra skyrių, tarp jų VCALENDAR yra pasaulinė sekcija, apimanti visas kitas dalis. Skyriuje VEVENT apibrėžiami įvykiai, VTODO – visų darbų sąrašas, VJOURNAL – žurnalo įrašai, o VTIMEZONE – laiko juostos informacija. leidžiamos kelios panašios kategorijos skyriai. Daugeliui įvykių iCalendar faile gali būti keli VEVENT skyriai.

### Turinio eilutės ###

iCalendar objektai yra išdėstyti į skirtingas teksto eilutes turinio eilutes. Šiame failo formate CRLF seka baigia eilutę, o eilutės ilgis ribojamas iki 75 oktetų, neįskaitant eilutės lūžio. Ilgą duomenų elementą galima išplėsti iki daugelio eilučių.

### Sąrašo ir laukų skyrikliai ###

Savybės ir parametrai nurodo reikšmių sąrašą, atskirtą KOMMA simboliu. Cbutuotos eilutės naudojamos URI pagrįstoms parametrų reikšmėms. Parametrų sąrašas gali būti sudarytas pagal turto vertę. Kiekvienas šio sąrašo ypatybės parametras turi būti atskirtas SEMIKOLAŠIU.

Vertybių sąraše SEMIKOLAPIS išskiria ypatybių parametrus, o KABLIS atskiria ypatybių vertes. Pavyzdys pateiktas žemiau:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Kelios reikšmės

Kai kurios savybės gali turėti kelias reikšmes. Paprasčiausiai sugeneruoti naują turinio eilutę su nuosavybės pavadinimu yra pagrindinė daugiareikšmių ypatybių taisyklė. Tačiau vienai vertei su keliais kalbų variantais negalima naudoti kelių reikšmių savybių.

### Dvejetainis turinys

iCalendar objekte ypatybės reikšmė gali nurodyti dvejetainio turinio duomenis, patalpintus išoriniame MIME objekte, naudojant URI. Įdėtas dvejetainis turinys gali būti naudojamas specialiose situacijose naudojant parametrą ENCODING, kai programa turi išreikšti iCalendar objektą kaip vienintelį objektą. Toliau pateiktame pavyzdyje paaiškinama ypatybė ATTACH su URI nuoroda:

ATTACH: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Simbolių rinkinys

Nors numatytoji iCalendar simbolių rinkinio schema yra UTF-8, nenurodytas joks ypatybės parametras, kuris apibrėžtų ypatybės vertės simbolių rinkinį. MIME perdavimuose parametras charset PRIVALO būti naudojamas esamam simbolių rinkiniui.

## Kaip atidaryti ICS failą?

Yra keletas būdų, kaip atidaryti ICS failą. Tai išsamiai aprašyta toliau.

1. Atidarykite ICS naudodami kalendoriaus programas

ICS failus galite atidaryti naudodami kalendoriaus programas, tokias kaip Microsoft Outlook, Google Calendar arba Apple Calendar. Jei jūsų įrenginyje įdiegtos šios programos, galite atidaryti ICS failą su šiomis programomis tiesiog dukart spustelėdami jį. Taip ICS failo įvykiai bus importuoti į jūsų kalendorių.

1. Atidarykite ICS failą teksto rengyklėje

Taip pat galite atidaryti ICS failą bet kuriame teksto rengyklėje, pvz., Microsoft Notepad arba Apple TextEdit. Atidarę pamatysite eilutes DTSTART ir DTEND, kurios atspindi įvykio pradžios ir pabaigos laiką.

1. Rankiniu būdu importuokite ICS failą kalendoriaus programoje

Taip pat galite rankiniu būdu importuoti ICS failą į savo kalendoriaus programą naudodami šių kalendoriaus programų Imiprot ir eksportavimo parinktis. Taip ICS failo įvykiai bus įtraukti į jūsų kalendorių.

## Nuorodos

* [Interneto kalendoriaus ir planavimo pagrindinio objekto specifikacija](https://www.ietf.org/rfc/rfc5545.txt)

* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)

* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)


