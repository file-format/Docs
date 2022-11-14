{
  "date" : "2021-07-29",
  "keywords" :[ "pes file", "pes file format", "wat is een pes file", "file", "pes example", "pes file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PES-bestandsindeling - Brother PE-borduurindeling",
  "description":"Meer informatie over PES-bestandsindeling en API's die PES-bestanden kunnen maken en openen.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Wat is een PES-borduurbestand?

Het PES-borduurbestand is een ontwerpbestand met instructies voor de borduur-/naaimachines. Het werd ontwikkeld door Brother Industries voor hun borduurmachines, maar werd later geformaliseerd als algemeen bestandsformaat. PES-bestanden worden door naaimachines gebruikt om instructies te lezen voor het naaien van patronen op stof. Deze bestanden hebben twee doelen; eerst het verstrekken van ontwerpinformatie voor de PE-Design-toepassing ontwikkeld door Brother Industries en ten tweede het verstrekken van ontwerpnaam, kleuren en borduurmachinecodes zoals "stop", "jump" en "trim".

## PES-bestandsindeling - Meer informatie

Een PES-bestand wordt in binaire bestandsindeling op schijf opgeslagen. Het bevat meerdere secties met naai-informatie die is opgeslagen met behulp van een vooraf gedefinieerde methode. Het PES-bestandsformaat is als volgt.

* Versiegegevens - Geeft versie-informatie en kan elke waarde zijn `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* PEC-zoekwaarde - Een 4 byte little-endian integer die onmiddellijk de versiegegevens volgt en de zoekwaarde vertegenwoordigt voor de PEC-sectie die ontwerpdetails bevat.
* PSE-sectie - Bevat ontwerpinformatie die relevant is voor Brother PE-Design en mogelijk andere naaitoepassingen
* PCE-sectie - Kan overal in het PSE-bestand zijn, maar waarnaar wordt verwezen door de PEC-zoekwaarde.

## Type naaimachines met PES-bestand

PES-bestanden worden voornamelijk gemaakt door de PE-Design-software die wordt gebruikt met de Brother-naaimachines. Sommige andere machines die PES-bestanden kunnen ondersteunen, zijn onder meer Babylock- en Bernina-borduurmachines voor thuis.

## Hoe PSE-bestanden converteren?

De PE-Design-softwaretoepassing kan [PSE-bestand converteren](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+bestand) naar andere formaten zoals .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd of .xxx. Het kan worden gedaan met behulp van de PE-Design-applicatie door het bestand te openen en het conversieformaat te selecteren.

## Referenties

* [PE-ontwerp - Instructiehandleiding](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

