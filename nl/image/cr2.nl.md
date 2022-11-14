{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR2-bestandsindeling - Canon Raw 2-beeldbestand",
  "description":"Meer informatie over CR2-bestandsindelingen en API's die CR2-bestanden kunnen maken en openen.",
  "linktitle" : "CR2",
  "menu" : {
    "docs" : {
      "identifier":"image-cr2",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## Wat is een CR2-bestand?

Een CR2-bestand (Camera RAW 2) is een RAW-beeldbestand dat is gemaakt door digitale camera's van Canon. Het slaat de originele, niet-verwerkte, verliesvrije beeldgegevens op die door de camera zijn vastgelegd. Het CR2-bestandsformaat is door Canon ontwikkeld voor zijn digitale camera's en kan beelden van hoge kwaliteit opnemen tot 14 bits RGB. Dit levert beelden van hoge kwaliteit op met voldoende ruimte voor nabewerking. Het CR2-beeldformaat is door Canon gebruikt in hun 350D-, 20D- en 1D-cameramodellen. CR2-bestanden zijn RAW-bestanden en bevatten aanvullende metadata-informatie zoals camera-informatie, lensinfo, bracketing-informatie, witbalans en andere instellingen.

## CR2-bestandsindeling

CR2-bestanden worden op de geheugenkaart van de camera opgeslagen als binaire bestanden in het eigen bestandsformaat van Canon. Het CR2-bestandsformaat verving het aanvankelijk gebruikte CRW-bestandsformaat en werd later zelf vervangen door het Canon RAW 3-bestandsformaat. Het CR2-bestandsformaat is gebaseerd op de [TIFF](/nl/image/tiff/)-specificaties met 4 Image File Directories (IFD's).

|Offset |Inhoud |Commentaar|
---|---|---|
|0x0000 |Header |bevat de bytevolgorde, de versie en de offset naar de RAW-afbeelding|
|computed |IFD#0 |dit deel bevat de Exif-sectie, die de Makernotes-sectie bevat.
Informatie over foto#0|
|computed |picture#0 |kleine versie van de afbeelding (een vierde van de grootte van het origineel), gecomprimeerd in Jpeg|
|berekend |IFD#1 |Informatie over afbeelding#1.|
|computed |picture#1 |kleine versie van de afbeelding, gecomprimeerd in Jpeg|
|berekend |IFD#2 |Informatie over afbeelding#2.|
|berekend |afbeelding#2 |kleine versie van de afbeelding, niet gecomprimeerd|
|in kop| IFD#3| Informatie over afbeelding #3, de RAW-afbeelding met volledige afmetingen|
|computed |picture#3 |RAW-beeldgegevens, lossless gecomprimeerd in Jpeg (geen RGB-gegevens!)|

## Voordeel van CR2-bestandsindeling

Het opslaan van foto's in RAW-formaat maakt veel nabewerking van de foto mogelijk, zoals het aanpassen van de witbalans. Dit is veel moeilijker en met een groot kwaliteitsverlies met andere beeldbestandsformaten zoals [JPEG](/nl/image/jpeg/).

## Is CR2 beter dan JPEG?

CR2-bestanden zijn onbewerkte bestanden zonder verlies van gegevens en dus zonder kwaliteitsverlies. JPEG aan de andere kant is een verliesgevend beeldbestandsformaat omdat het enkele gegevens verliest om het bestand te verkleinen. De CR2-bestanden zijn dus van hoge kwaliteit en meer geschikt voor retoucheren en verbeteringen.

## Referenties

* [CR2-bestandsindeling](http://lclevy.free.fr/cr2/)

