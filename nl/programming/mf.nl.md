{
  "date" : "2019-10-11",
  "keywords": [ "mf file", "mf", "extension", "format", "mf file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MF - Java Manifest-bestandsindeling",
  "description":"Meer informatie over MF-bestandsindelingen en API's die MF-bestanden kunnen maken en openen.",
  "linktitle" : "MF",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een MF-bestand?

Een bestand met de extensie .mf is een Java Manifest-bestand dat informatie bevat over de afzonderlijke [JAR](/nl/programming/jar/) bestandsitems. Het MF-bestand zelf bevindt zich in het JAR-bestand en biedt alle extensie- en pakketgerelateerde definities. JAR-bestanden kunnen worden geproduceerd om te worden gebruikt als een uitvoerbaar bestand. In dat geval specificeert het mainfest-bestand de hoofdklasse van de toepassing die de instructie **'public static void main'** bevat. Manifest-bestanden worden MANIFEST.MF genoemd en kunnen worden geopend met elke teksteditor op Windows-, MacOS- en Linux-besturingssystemen.

## Specificaties van het manifest bestandsformaat

[specificaties van de bestandsindelingen](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) zijn beschikbaar door Oracle in hun gids voor JAR-bestandsindeling. Een manifestbestand bestaat uit hoofdsecties die worden gevolgd door een lijst met secties voor individuele JAR-bestandsvermeldingen. Elke sectie volgt enkele regels en beperkingen.

### Hoofdsecties

Een hoofdsectie:

* bevat informatie over beveiliging en configuratie over het JAR-bestand
* bevat informatie over de applicatie of extensie waar het JAR-bestand deel van uitmaakt
* definieert de belangrijkste kenmerken voor elk afzonderlijk manifest item

**Opmerking**: Geen enkel kenmerk in deze sectie kan de naam "Naam" krijgen.

### Afzonderlijke secties

Een afzonderlijke sectie definieert verschillende attributen voor pakketten of bestanden van een JAR-bestand. Elke sectie moet beginnen met een attribuut met de naam "Naam", waarvan de waarde een relatief pad naar het bestand moet zijn, of een absolute URL die verwijst naar gegevens buiten het archief.

### Manifestspecificaties

|Attibutes|Beschrijving|
---|---|
|manifest-bestand|hoofd-sectie nieuwe regel *individuele-sectie|
|main-section|versie-info nieuwe regel *main-attribute|
|version-info|Manifest-Version : versienummer|
|versienummer|cijfer+{.cijfer+}*|
|main-attribute|(elk legitiem hoofdattribuut) newline|
|individual-section|Naam : waarde nieuwe regel *perentry-attribuut|
|perentry-attribuut|(elk legitiem perentry-kenmerk) newline|
|newline|CR LF | LF | CR (niet gevolgd door LF)|
|cijfer|{0-9}|

## Referenties

* [Oracle - JAR-bestandsindeling](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
* [JAR-bestandsindeling](https://en.wikipedia.org/wiki/JAR_(file_format))

