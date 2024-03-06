---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON faila formāts — kas ir JSON failse?
linktitle: JSON
description: Lnopelniet par JSON faila formātu un API, kas var izveidot un atvērt JSON failus.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Kas ir JSON fails?

JSON (JavaScript Object Notation) ir atvērta standarta faila formāts datu koplietošanai, kas izmanto cilvēkiem lasāmu tekstu datu glabāšanai un pārsūtīšanai. JSON faili tiek glabāti ar paplašinājumu .json. JSON nepieciešams mazāk formatēšanas, un tā ir laba alternatīva [XML](/web/xml/). JSON ir atvasināts no JavaScript, bet ir no valodas neatkarīgs datu formāts. JSON ģenerēšanu un parsēšanu atbalsta daudzas mūsdienu programmēšanas valodas. *application/json* ir JSON izmantotais multivides veids.

## JSON faila formāts — īsa vēsture

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON pamatā bija standarta ECMA-262 3. izdevums — 1999. gada decembris, kas ir JavaScript apakškopa.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. 2017. gada novembrī ISO/IEC 21778:2017 tika publicēts kā starptautisks standarts. RFC 8259 2017. gada 13. decembrī publicēja The Internet Engineering Task Force, kas ir interneta standarta STD 90 pašreizējā versija.

## JSON faila struktūra

JSON dati tiek rakstīti **atslēgas/vērtības** pāros. Atslēga un vērtība ir atdalīta ar kolu (:) vidū, atslēga atrodas kreisajā pusē un vērtība labajā pusē. Dažādi atslēgu/vērtību pāri ir atdalīti ar komatu (,). Atslēga ir virkne, ko ieskauj pēdiņas, piemēram, nosaukums. Vērtības var būt šāda veida.

- Numurs.
- Virkne: Unikoda rakstzīmju secība, ko ieskauj pēdiņas.
- Būla: patiess vai nepatiess.
- Masīvs: vērtību saraksts, ko ieskauj, piemēram, kvadrātiekavās

``` json
[ Ābols, Banāns, Apelsīns]
```

- Objekts: atslēgu/vērtību pāru kolekcija, ko ieskauj cirtaini iekavas, piemēram,

``` json
{vārds: Džeks, vecums: 30, mīļākais sporta veids : Futbols}
```

JSON objektus var arī ligzdot, lai attēlotu datu struktūru. Tālāk ir sniegts JSON objekta piemērs.

### JSON formāta piemērs

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Kāds ir maksimālais JSON faila lielums?

JSON faila maksimālajam izmēram praktiski nav ierobežojumu. Tas var būt tik garš, cik daudz vietas prasa glabājamais saturs.

Kad runa ir par JSON faila formāta izmantošanu datu pārsūtīšanai internetā, ir jābūt uzmanīgiem attiecībā uz datora pieejamajiem resursiem. Ja tiek pārsūtīti lieli JSON dati, pārsūtīšana tiks ietekmēta, ja klienta pārlūkprogrammai ir ierobežota atmiņa.


Specifikācijās nav stingru ierobežojumu, taču jums ir jābūt uzmanīgiem, lai neiztērētu lietotāju datoros esošos resursus, jo tas ātri pasliktinās lietotāju pieredzi un viņi, visticamāk, pametīs jūsu lietotni.

## JSON vs XML

**XML** ir vēl viens izplatīts un plaši izmantots failu formāts datu apmaiņai internetā. Runājot par datu apmaiņu starp lietojumprogrammām, izstrādātājiem ir iespēja izmantot gan XML, gan JSON failu formātus. Tomēr JSON tiek pieņemts kā ērtākais veids datu apmaiņai starp lietojumprogrammām internetā šādu iemeslu dēļ.

 1. JSON nodrošina skaidru un vieglāk lasāmu datu skatījumu salīdzinājumā ar XML failu formātiem
 1. JSON samazina datu pārsūtīšanas izmaksas internetā, jo tajā ir mazāk rakstzīmju skaita, lai noteiktu to pašu datu kopu, salīdzinot ar XML.
 1. Mūsdienu programmēšanas valodas nodrošina iebūvētus parsētājus, lai parsētu JSON atbildi tīmeklī.

## FAQ

 * **Kam tiek izmantots JSON fails?** JSON faila formātu var izmantot kā starpposma faila formātu, lai saglabātu datus, kas ģenerēti, piemēram, no vietnē iesniegtās veidlapas. To izmanto arī kā datu formāta failu jebkurai programmēšanas valodai un nodrošina sadarbspēju starp dažādiem datu veidiem.
 * **Vai JSON un XML fails ir viens un tas pats?** Nav īsti. JSON atšķiras no XML ar to, ka JSON ir īsāks, ātri nolasāms un labojams, var izmantot masīvus un neizmanto beigu tagu.
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **Kā konvertēt JSON uz PDF?** Varat izmantot tiešsaistes lietotnes, piemēram, Asopse.app for Cells, lai [konvertētu JSON failu uz PDF] (https://products.aspose.app/cells/conversion/json-to- pdf).
 * **Kā atvērt JSON failu programmā Word?** Varat izmantot tiešsaistes lietotnes, piemēram, Aspose.app for Words, lai [konvertētu JSON failu uz Word] (pārveidotu JSON formātu par WORD operētājsistēmā Android, izmantojot Java).

## Vai tu zināji?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## Atsauces

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

