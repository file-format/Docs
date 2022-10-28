{
  "date" : "2021-07-29",
  "keywords" :[ "pes file", "pes file format", "was ist eine pes file", "file", "pes example", "pes file extension", "extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PES-Dateiformat - Brother PE-Stickformat",
  "description":"Erfahren Sie mehr über das PES-Dateiformat und APIs, die PES-Dateien erstellen und öffnen können.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Was ist eine PES-Stickdatei?

Die PES-Stickdatei ist eine Designdatei, die Anweisungen für die Stick-/Nähmaschinen enthält. Es wurde von Brother Industries für ihre Stickmaschinen entwickelt, aber später als allgemeines Dateiformat formalisiert. PES-Dateien werden von Nähmaschinen verwendet, um Anweisungen zum Nähen von Mustern auf Stoff zu lesen. Diese Dateien dienen zwei Zwecken; erstens Bereitstellung von Designinformationen für die von Brother Industries entwickelte PE-Design-Anwendung und zweitens Bereitstellung von Designnamen, Farben und Stickmaschinencodes wie "Stopp", "Sprung" und "Trimmen".

## PES-Dateiformat – Weitere Informationen

Eine PES-Datei wird im Binärdateiformat auf der Disc gespeichert. Es enthält mehrere Abschnitte, in denen Nähinformationen mit vordefinierten Methoden gespeichert sind. Das PES-Dateiformat ist wie folgt.

* Versionsdaten - Gibt Versionsinformationen an und kann ein beliebiger Wert sein `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* PEC-Suchwert – Eine 4-Byte-Little-Endian-Ganzzahl, die unmittelbar auf die Versionsdaten folgt und den Suchwert für den PEC-Abschnitt darstellt, der Entwurfsdetails enthält
* PSE-Abschnitt – Enthält Designinformationen, die für das Brother PE-Design relevant sind, und möglicherweise andere Nähanwendungen
* PCE-Abschnitt – Kann sich irgendwo in der PSE-Datei befinden, wird aber vom PEC-Suchwert referenziert.

## Art der Nähmaschinen mit PES-Datei

PES-Dateien werden hauptsächlich von der PE-Design-Software erstellt, die mit den Brother-Nähmaschinen verwendet wird. Einige andere Maschinen, die PES-Dateien unterstützen können, sind Babylock- und Bernina-Heimstickmaschinen.

## Wie konvertiert man PSE-Dateien?

Die PE-Design-Softwareanwendung kann [PSE-Datei konvertieren](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+Datei) in andere Formate wie .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd oder .xxx. Dies kann mit der Anwendung PE-Design erfolgen, indem Sie die Datei öffnen und das Konvertierungsformat auswählen.

## Verweise

* [PE Design – Bedienungsanleitung](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

