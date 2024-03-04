---
date: 2019-10-11
keywords: json, .json, json file format, how to open json files, javascript object notation, json data format, .json file format
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON failo formatas – kas yra JSON failase?
linktitle: JSON
description: Luždirbti apie JSON failo formatą ir API, kurios gali sukurti ir atidaryti JSON failąs.
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Kas yra JSON failas?

JSON (JavaScript Object Notation) yra atviras standartinis failo formatas, skirtas dalytis duomenimis, kuriame duomenims saugoti ir perduoti naudojamas žmogaus skaitomas tekstas. JSON failai saugomi su .json plėtiniu. JSON reikia mažiau formatuoti ir yra gera [XML](/web/xml/) alternatyva. JSON yra išvestas iš JavaScript, bet yra nuo kalbos nepriklausomas duomenų formatas. JSON generavimą ir analizavimą palaiko daugelis šiuolaikinių programavimo kalbų. *application/json* yra JSON naudojamas medijos tipas.

## JSON failo formatas – trumpa istorija

There was a need for real-time server to client communication that lead to the creation of JSON. The JSON format was first specified by Douglas Crockford in March 2001. JSON buvo pagrįsta standartiniu ECMA-262 3-iuoju leidimu – 1999 m. gruodžio mėn., kuris yra JavaScript poaibis.

The first edition of JSON standard ECMA-404 was published in October 2013 by Ecma International. RFC 7159 became the main reference for JSON's Internet uses in 2014. 2017 m. lapkritį ISO/IEC 21778:2017 buvo paskelbtas kaip tarptautinis standartas. RFC 8259 2017 m. gruodžio 13 d. paskelbė The Internet Engineering Task Force, kuri yra dabartinė interneto standarto STD 90 versija.

## JSON failo struktūra

JSON duomenys rašomi **rakto/vertės** poromis. Raktas ir reikšmė yra atskirti dvitaškiu (:) viduryje, raktas yra kairėje, o reikšmė - dešinėje. Skirtingos rakto/reikšmių poros atskiriamos kableliais (,). Raktas yra eilutė, apsupta dvigubomis kabutėmis, pavyzdžiui, vardas. Vertės gali būti šių tipų.

- Skaičius.
- Eilutė: Unikodo simbolių seka, apsupta dvigubomis kabutėmis.
- Boolean: tiesa ar klaidinga.
- Masyvas: pavyzdžiui, laužtiniais skliaustais pateiktų verčių sąrašas

``` json
[ Obuolys, Bananas, Apelsinas]
```

- Objektas: raktų / reikšmių porų rinkinys, apsuptas riestiniais skliaustais, pvz.

``` json
{vardas: Džekas, amžius: 30, mėgstamiausias sportas : futbolas}
```

JSON objektai taip pat gali būti įdėti, kad atspindėtų duomenų struktūrą. Toliau pateikiamas JSON objekto pavyzdys.

### JSON formato pavyzdys

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

## Koks yra didžiausias JSON failo dydis?

Didžiausias JSON failo dydis praktiškai neribojamas. Jis gali būti tiek, kiek vietos reikia laikyti turiniui.

Kalbant apie JSON failo formato naudojimą duomenims perduoti internetu, reikia būti atsargiems dėl turimų kompiuterio išteklių. Jei perkeliami dideli JSON duomenys, perkėlimas turės įtakos, jei kliento naršyklėje bus ribota atmintis.


Specifikacijos neapibrėžia griežtų apribojimų, tačiau turite būti atsargūs, kad neišnaudotumėte išteklių savo naudotojų kompiuteriuose, nes tai greitai pablogins naudotojų patirtį ir jie greičiausiai atsisakys jūsų programos.

## JSON prieš XML

**XML** yra dar vienas įprastas ir plačiai naudojamas failų formatas, skirtas keistis duomenimis internetu. Kai kalbama apie keitimąsi duomenimis tarp programų, kūrėjai turi galimybę naudoti XML ir JSON failų formatus. Tačiau JSON yra priimtas kaip patogiausias būdas keistis duomenimis tarp programų internetu dėl toliau nurodytų priežasčių.

 1. JSON suteikia aiškų ir lengviau skaitomą duomenų vaizdą, palyginti su XML failų formatais
 1. JSON sumažina duomenų perdavimo internetu išlaidas, nes jame yra mažiau simbolių tam pačiam duomenų rinkiniui apibrėžti, palyginti su XML.
 1. Šiuolaikinės programavimo kalbos suteikia įmontuotus analizatorius, skirtus JSON atsakui išanalizuoti žiniatinklyje.

## DUK

 * **Kam naudojamas JSON failas?** JSON failo formatas gali būti naudojamas kaip tarpinis failo formatas duomenims, sugeneruotiems duomenims, pvz., iš pateiktos formos svetainėje, saugoti. Jis taip pat naudojamas kaip duomenų formato failas bet kuriai programavimo kalbai ir užtikrina skirtingų tipų duomenų sąveiką.
 * **Ar JSON ir XML failai yra vienodi?** Tikrai ne. JSON skiriasi nuo XML tuo, kad JSON yra trumpesnis, jį galima greitai nuskaityti ir teisingai, gali naudoti masyvus ir nenaudoja pabaigos žymos.
 * **Can I convert JSON to CSV?** Yes, there are certain online converter apps such as **GroupDocs Conversion apps** that can [convert JSON to CSV](https://products.groupdocs.app/conversion/json-to-csv).
 * **Kaip konvertuoti JSON į PDF?** Galite naudoti internetines programas, pvz., Asopse.app for Cells, norėdami [konvertuoti JSON failą į PDF](https://products.aspose.app/cells/conversion/json-to- pdf).
 * **Kaip atidaryti JSON failą programoje Word?** Galite naudoti internetines programas, pvz., Aspose.app for Words, norėdami [konvertuoti JSON failą į Word] (konvertuoti JSON formatą į WORD sistemoje Android per Java).

## Ar tu žinai?

You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about JSON or Web file formats, you can post your findings in [Web File Format News](https://news.fileformat.com/t/Web) section for people to learn more form these.

## Nuorodos

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [An Introduction to JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

