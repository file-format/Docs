{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ATOM fails — Atom sindikācijas formāts",
  "description": "Uzziniet, kas ir ATOM fails un API, kas var izveidot un atvērt ATOM failus.",
  "linktitle": "ATOM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ato-lvm"
}
},
  "lastmod": "2022-08-05"
}

## Kas ir ATOM fails?

ATOM fails ir sindikācijas formāts Atom plūsmas un ievades dokumentu struktūrai. Līdzīgi kā .RSS failiem, ATOM faila formāts ir uz XML balstīts sindikācijas formāts, kas ir satura publicēšanas standarts. ATOM fails tiek izmantots tīmekļa plūsmām, kas ļauj programmatūras programmām pārbaudīt vietnē publicētos atjauninājumus. Tajā ir ieraksti, kas var būt dažāda veida, piemēram, virsraksti, pilna teksta raksti, fragmenti vai saites uz vietnes saturu.

Lietojumprogrammas, kas var **atvērt ATOM failus**, ietver **Apple Safari**.

## ATOM faila formāts — vairāk informācijas

ATOM faili tiek glabāti un publicēti populārajā XML failu formātā, kas ir universāls informācijas apmaiņas formāts. Tas tika izstrādāts kā alternatīva RSS, ņemot vērā RSS failu formāta ierobežojumus un trūkumus.

### Atomu dokumentu veidi

 1. Atom ievades dokumenti — tas ir XML dokuments, kas sastāv no viena informācijas elementa, ko sauc par ierakstu, Atom plūsmai. Tam ir atomu ievades elements, kas satur vairākus bērnu elementus. Atom ieraksta saturs var būt vienkāršs teksts, HTML, XHTML vai cits IANA (Internet Assigned Numbers Authority) multivides veids.
 1. Atom plūsmas dokumenti — tas ir XML dokuments, kas nodrošina metadatus par Atom plūsmu un vienu vai vairākus plūsmas ierakstus. Kad klients pieprasa informācijas pieprasījumu no plūsmas, serveris ģenerē plūsmas dokumentu, kas ietver vairākus Atom ierakstus, lai izpildītu pieprasījumu.
 1. Atom kolekcija — tas ir īpaša veida Atom plūsmas dokuments, kurā ir rediģēšanai pieejamie Atom ierakstu URL.

## Atsauces

* [Atom sindikācijas formāts — RFC](https://www.rfc-editor.org/rfc/rfc4287.html)

* [Overview of Atom Feeds - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom — tīmekļa standarts](https://en.wikipedia.org/wiki/Atom_(web_standard))


