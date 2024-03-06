{
  "date": "2022-08-05",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPCACHE fails — HTML5 kešatmiņas manifesta faila formāts",
  "description": "Uzziniet, kas ir APPCACHE fails un API, kas var izveidot un atvērt APPCACHE failus.",
  "linktitle": "APPCACHE",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-appcach-lve"
}
},
  "lastmod": "2022-08-05"
}

## Kas ir APPCACHE fails?

APPCACHE fails ir teksta fails, kas satur to resursu sarakstu, kas pārlūkprogrammām jāglabā kešatmiņā, lai bezsaistē piekļūtu tīmekļa lietojumprogrammām. Tas ir noderīgi, ja nav interneta savienojuma. Šādā situācijā pārlūkprogramma izmanto bezsaistes kešatmiņas resursus, lai nodrošinātu piekļuvi tīmekļa saturam. APPCACHE failā ir ietverti tīmekļa resursi, piemēram, attēli (piemēram, **[PNG](/image/png/)**, **[WEBP](/image/webp/)** utt.), stila lapas **([CSS])(/web/css/) )** un skriptu failus (piemēram, Javascript **[JS](/web/js/)** failus).

Lietojumprogrammas, kas var **atvērt APPCACHE failus**, ietver tādas tīmekļa pārlūkprogrammas kā Google Chrome, Safari un Firefox.

## APPCACHE faila formāts — vairāk informācijas

APPCACHE faili ir vienkārši teksta faili, kas nodrošina bezsaistes piekļuvi tīmekļa lapām, lai tās darbotos bez interneta savienojuma. APPCACHE klātbūtne norāda, ka lapa ir pieejama bezsaistē.

### Kā atsaukties uz APPCACHE failu?

Jūsu HTML lapā uz APPCACHE failu ir atsauce šādi.

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE manifesta faila struktūra

Vienkāršs APPCACHE manifesta fails izskatās šādi.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Šis ir vienkāršākais piemērs, un var būt arī sarežģītākas struktūras.

## APPCACHE Manifesta priekšrocības

Kešatmiņas saskarnes izmantošana sniedz tīmekļa lietojumprogrammām šādas priekšrocības.

 1. Bezsaistes pārlūkošana — kešatmiņas saskarne ļauj galalietotājiem pārlūkot visu jūsu vietni, kad viņi ir bezsaistē.
 1. Ātrums — kešatmiņa nodrošina ātru piekļuvi bezsaistes saturam tieši no diska
 1. Pieejamība visu laiku — ja jūsu vietne nedarbosies, lietotāji joprojām varēs piekļūt tīmekļa saturam un varēs izmantot bezsaistes pieredzi.

## Atsauces

 * [AppCache manifesta ceļvedis iesācējiem](https://web.dev/appcache-beginner/)

