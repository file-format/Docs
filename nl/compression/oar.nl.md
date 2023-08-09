{
  "date" : "2021-04-08",
  "keywords" :[ "oar file", "oar file format", "wat is een oar file", "file", "oar example", "oar file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator Archief-bestandsindeling",
  "description":"Meer informatie over OAR-bestandsindeling en API's die OAR-bestanden kunnen maken en openen.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Wat is een OAR-bestand?

Een bestand met de extensie .oar is een archiefbestand dat wordt gebruikt door de OpenSimulator-toepassing, een open-source 3D-toepassingsserver voor het creëren van een virtuele omgeving die via het netwerk toegankelijk is voor meerdere gebruikers. Het OAR-bestandsformaat biedt de benodigde activagegevens die nodig zijn om het terrein, de objecttexturen en inventarissen volledig op een ander systeem te laden. OpenSimulator heeft ook een optionele hypergrid waarmee gebruikers andere OpenSimulator-installaties op internet kunnen bezoeken. OAR-bestanden hebben een internet-MIME-type applicatie / roeispaan en bevatten een of meer gearchiveerde bestanden.


## OAR-bestandsindeling

OAR zijn binaire bestanden die zijn opgeslagen in gecomprimeerde archiefbestandsindeling. De nieuwste versie van de OAR-bestandsindeling is [versie 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) die grote veranderingen heeft ondergaan ten opzichte van de vorige [versie 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). De nieuwste versie ondersteunt het opslaan van meerdere regio's in een enkele OAR en is niet achterwaarts compatibel met versies van OpenSimulator vóór 0.7.5. Een OAR-bestand is een gzipped tar-bestand (tar.gz) in het originele Unix tar-formaat (niet USTAR).

## Voorbeeld OAR-regio's
AOR-bestanden kunnen meerdere regio's bevatten. De structuur van het archief is als volgt (dit voorbeeld bevat 4 regio's):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archief.xml

Het archiefcontrolebestand bevat een belangrijk versienummer voor het definiëren van compatibiliteit met toekomstige formaatwijzigingen. De aanwezigheid van activa in een OAR-indeling wordt aangegeven door het booleaanse element<assets_included> . Informatie over de opgenomen regio's is opgenomen in een manifest dat aanwezig is in het controlebestand. Een voorbeeld van Archive.xml is als volgt.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Referenties

* [OAR-indeling v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

