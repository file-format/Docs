{
  "date": "2022-05-06",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FIT faila formāts - Garmin darbības fails",
  "description": "Uzziniet par FIT faila formātu un API, kas var izveidot un atvērt FIT failus.",
  "linktitle": "FIT",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-fi-lvt"
}
},
  "lastmod": "2022-05-06"
}

## Kas ir FIT fails?

FIT fails ir GIS fails, ko izveido Garmin sporta valkājamas ierīces. To izmanto, lai reģistrētu personas darbības, kad viņš/viņa pārvietojas, valkājot šīs ierīces. Aktivitāšu dati ietver GPS ierīces ierakstīto atrašanās vietu un laiku. FIT faili tiek izmantoti arī reģistrēto aktivitāšu datu pārsūtīšanai, izmantojot tīmekļa API. Šī iemesla dēļ FIT faili ir visbiežāk izmantotais failu formāts fitnesa datu kopīgošanai ar citām fitnesa platformām. Citi izplatīti failu formāti ir [GPX](/gis/gpx/), TCX un [KML](/gis/kml/).

## FIT faila formāts — vairāk informācijas

FIT faili tiek saglabāti diskā kā bināri faili ar Garmin ierīču ierakstīto informāciju par aktivitāti. FIT failā saglabātā informācija ietver:

 * Datums Laiks
 * Sporta veidi
 * Apļa un sadalītie dati
 * GPS trase
 * Sensora dati
 * Pasākumi aktīvai sesijai

Darbības datus var ierakstīt failā reāllaikā vai eksportēt, kad aktivitāšu ierakstīšana ir pabeigta.

### FIT aktivitātes ziņojumi

FIT darbības failā var būt ietverti daži nepieciešamie ziņojumu veidi. Tālāk ir norādīti darbības failam nepieciešamie ziņojumi.

|Ziņojums|Mērķis|
---|---|
|Faila ID| Faila ID ziņojums ir nepieciešams visiem FIT failu tipiem, un ir paredzēts, ka tas ir pirmais ziņojums failā. Darbības failiem rekvizīta tips ir jāiestata uz 4.|
|Aktivitāte| FIT aktivitātes failā ir nepieciešams viens aktivitātes ziņojums. Darbības ziņojumā ir iekļauti rekvizīti Vietējais laikspiedols un sesiju skaits. Vietējais laikspiedols tiek izmantots, lai noteiktu laika joslas nobīdi, ko var lietot visiem faila laikspiedoliem. Lielākā daļa ierīču ieraksta FIT failus reāllaikā, un sesiju skaits nebūs zināms līdz ieraksta beigām. Šī iemesla dēļ darbības ziņojums bieži vien ir faila pēdējais ziņojums.|
|Sesija| Darbību failos būs viens vai vairāki sesijas ziņojumi. Sesijas ziņojums ir kopsavilkuma ziņojuma veids. Sākuma laiks, Kopējais pagājušais laiks, Kopējais taimera laiks un Laika zīmogs ir obligāti lauki visiem kopsavilkuma ziņojumiem.|
|Aplis| Apļa ziņojumi atspoguļo apļus vai intervālus sesijas laikā. Apļa ziņojums ir kopsavilkuma ziņojuma veids. Sākuma laiks, Kopējais pagājušais laiks, Kopējais taimera laiks un Laika zīmogs ir obligāti lauki visiem kopsavilkuma ziņojumiem.|
|Ieraksts| Ieraksta ziņojumi ietver GPS koordinātas, ātrumu, attālumu, sirdsdarbības ātrumu, jaudu utt.|

## FIT fails noderīgi resursi

 * [FIT aktivitāšu failu atkodēšana](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
 * [FIT aktivitāšu failu kodēšana](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 
## Atsauces Nr.

* [FIT darbības fails](https://developer.garmin.com/fit/file-types/activity/)


