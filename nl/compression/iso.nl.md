{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Schijfkopiebestandsindeling",
  "description":"Wat is een ISO-bestand en API's die ISO-bestanden kunnen maken en openen?",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Wat is een ISO-bestand?

Een bestand met de extensie .iso is een niet-gecomprimeerd archiefschijfkopiebestand dat de inhoud van volledige gegevens op een optische schijf, zoals een cd of dvd, vertegenwoordigt. Gebaseerd op de [ISO-9660](https://www.iso.org/standard/17505.html) standaard, bevat het ISO-beeldbestandsformaat de schijfgegevens samen met de bestandssysteeminformatie die erin is opgeslagen. De mogelijkheid van ISO-bestanden om een exacte replica van de inhoud te bevatten, maakt het het perfecte bestandstype voor het maken van kopieën van cd's/dvd's en wordt meestal gebruikt om opstartbare gegevens op te slaan voor installatie. Meestal worden ISO-bestanden op USB/CD/DVD gebrand als opstartbare inhoud voor het opstarten van de machine voor installatie. ISO-bestanden hebben MIME-type application/x-iso9660-image.

## ISO-bestandsindeling

ISO-bestandsindeling is niet zoals andere bestandsindelingen voor containers, hoewel het de opgegeven inhoud van gegevens archiveert. Het archief wordt gemaakt als een binair bestand met de exacte structuur van de inhoud en bestandssysteeminformatie. Het ISO-bestandsformaat wordt als volgt beschreven door de [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660).

### Structuur op het hoogste niveau van ISO-bestand

De algemene structuur van het bestand bestaat uit:

* `Systeemgebied` - 32.768 bytes en wordt niet gebruikt door ISO_9660
* `Gegevensgebied` - bestaat uit een volumedescriptorset en padtabellen, mappen en bestanden

### Volumebeschrijving instellen

Het gegevensgebied begint met de volumedescriptorset, een set van een of meer volumedescriptors die eindigt met een volumedescriptorsetterminator. Deze fungeren gezamenlijk als een header voor het gegevensgebied en beschrijven de inhoud ervan (vergelijkbaar met het BIOS-parameterblok dat wordt gebruikt door FAT-, HPFS- en NTFS-geformatteerde schijven).

Een volumedescriptorset is zoals hieronder weergegeven.

|Volumebeschrijvingsset|
---|
|Volumebeschrijving #1|
|...|
|Volumebeschrijving #N|
|Volume descriptor set terminator|

#### Volumebeschrijving

Elke volumedescriptor is 2048 bytes groot en heeft de volgende structuur:

|Onderdeel |Type |Identificatie |Versie |Data|
---|---|---|---|---|
|Grootte |1 byte |5 bytes (altijd 'CD001') |1 byte (altijd 0x01) |2.041 bytes|

## Referenties

* [Optical Disk Image - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Bestandshandtekeningen](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

