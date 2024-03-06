{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TCX faila formāts - apmācības centra XML fails",
  "description":"Uzziniet par TCX failu formātu un API, kas var izveidot un atvērt TCX failus.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx-lv",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Kas ir TCX fails?

TCX (Training Center XML) fails ir datu apmaiņas formāts, ko izmanto datu apmaiņai starp fitnesa ierīcēm. Tas tika ieviests 2008. gadā ar Garmin apmācību centra produktu. Treniņu dati, piemēram, sirdsdarbības ātrums, skriešanas ritms, velosipēda ritms, kalorijas un apļa laiks, tiek saglabāti [XML](/web/xml/) formātā TCX failā. Turklāt TCX failā ir iekļauti arī kopsavilkuma dati par treniņu trasi. TCX faili ir līdzīgi [FIT](/gis/fit/) failiem, kas izveidoti ar Garmin sporta valkājamām ierīcēm.

## TCX faila formāts — vairāk informācijas

TCX faili tiek saglabāti diskā kā XML faili, katrs ieraksts tiek saglabāts kā darbība. Aktivitāte ietver visus treniņa datus, piemēram, laiku, apļa laiku, ID, sirdsdarbības ātrumu, intensitāti, ritmu un trases informāciju, kas satur pozīciju pārus, kā arī laika zīmogu šai platuma garajai pozīcijai, kas ir līdzīga [GPX](/gis/gpx/) faili.

### TCX faila formāta versijas

Ir divas šī formāta versijas ar savām XML shēmām, ko mitina Garmin. Tālāk ir minēti daži no tiem:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX datu protokols

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Atsauces Nr.

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)

* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)


