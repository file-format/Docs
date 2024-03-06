{
  "date": "2019-10-11",
  "keywords": [
"mht",
"mht failu",
"mht faila formātā",
"mht faila tips",
"failu",
"veids",
"kas ir mht fails"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MHT — MIME HTML faila formāts",
  "description": "Uzziniet par MHT faila formātu un API, lai izveidotu un atvērtu MHT failus.",
  "linktitle": "MHT",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-mh-lvt"
}
},
  "lastmod": "2021-02-29"
}

## Kas ir MHT fails?

Fails ar paplašinājumu .mht ir MIME iespējots arhivēšanas faila formāts, kas satur dažāda veida datus vienā failā. Tā var saglabāt datus, piemēram, tekstu, attēlus, lapas stilu [CSS](/web/css/) failu veidā, JavaScript un citus resursus kā iegultos resursus. MHT faili, kuriem ir MIME tipa ziņojums/rfc822, iekapsulē visu HTML faila saturu kā vienu arhīva failu, ko glabāt arhivēšanas ierīcēs. Programmatūras lietojumprogrammas, piemēram, Microsoft Word, ļauj konvertēt WORD dokumentus MHT formātā, eksportējot kā MHT failu. MHT failus var atvērt, izmantojot populāras pārlūkprogrammas, piemēram, Microsoft Internet Explore un Google Chrome.

## MHT faila formāts

Tāpat kā [MHTML](/web/mhtml/), MHT ir arī apkopotu HTML dokumentu MIME iekapsulēšana. Dokumenta saturs MHT dokumentā, piemēram, iekļautie attēli, stila lapas, sīklietotnes utt., ir MIME kodēts, ja tie ir saistīti ar saknes resursu, izmantojot URI. E-pasta klienti, piemēram, Microsoft Outlook, saglabā e-pastus (parasti [EML](/email/eml/)) MHT faila formātā. Pilnīgas MHT faila formāta specifikācijas ir pieejamas vietnē [RFC 822](https://tools.ietf.org/html/rfc822), un tās var izmantot programmatūras lietojumprogrammu izstrādei, kas var apstrādāt MHT failus.

## Atšķirība starp MHT un MHTML

Saglabājot tiešsaistes lapu, lietotājam tiek lūgts izvēlēties faila formātu, kurā tiešsaistes lapa ir jāsaglabā vietējā sistēmā. Visbiežāk lietotājs sajaucas starp iezīmēšanas valodu un MHTML failu formātiem. Viņi ievēro, ka ir apgrūtinoši redzēt, ka starp šiem faila formāts ir veselīgāks.

Kad lietotājs nolemj izvairīties no tiešsaistes lapas izšķērdēšanas kā iezīmēšanas valodas, tiek izveidota mape, kurā ir vairāki faili dažādam lapas saturam, ti, pilnīgi atšķirīga failu apgabala vienība, kas izveidota tekstam, grafikai, sīklietotnēm utt. Savukārt, saglabājot tiešsaistes lapa, jo MHTML izveido vienu failu visai tiešsaistes lapai. Visi lapas elementi kopā ar grafiku, saitēm un alternatīvo failu apgabala vienību iegulti vienā failā.

Protams, ir vienkārši apstrādāt MHT vai MHTML failus, jo failu var aizsargāt un koplietot vienkārši pa e-pastu. Tomēr iezīmēšanas valodas failu apgabala vienība zem informācijas zaudēšanas iespējas, jo pat viena faila pazaudēšana vai dzēšana var radīt visu iezīmēšanas valodas mapi lietotājam nederīgu.

## Atsauces

* [MHTML — Wikipedia](https://en.wikipedia.org/wiki/MHTML)

* [MHT RFC](https://tools.ietf.org/html/rfc822)


