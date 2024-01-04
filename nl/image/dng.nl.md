{
  "date" : "2019-10-11",
  "keywords" :[ "dng-bestand", "dng-bestandsformaat", "wat is een dng-bestand", "bestand", "dng-voorbeeld", "dng-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Digital Camera Image File Format",
  "description":"Meer informatie over DNG-bestandsindelingen en API's die DNG-bestanden kunnen maken en openen.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een DNG-bestand?

DNG is een beeldformaat voor digitale camera's dat wordt gebruikt voor de opslag van onbewerkte bestanden. Het is in september 2004 door Adobe ontwikkeld. Het is in feite ontwikkeld voor digitale fotografie. DNG is een uitbreiding van het [TIFF](/nl/image/tiff/)/EP-standaardformaat en maakt veel gebruik van metadata. Om onbewerkte gegevens van digitale camera's te manipuleren met het gemak van flexibiliteit en artistieke controle, kiezen fotografen voor Camera Raw-bestanden. JPEG- en TIFF-formaten slaan afbeeldingen op die door de camera worden verwerkt, daarom is er niet veel ruimte voor wijziging in dergelijke formaten.

## Geschiedenis en versies van DNG-bestandsindeling

Tot nu toe zijn er tot nu toe 5 versies van de DNG-specificatie geweest. Versie 1.0.0.0 werd gelanceerd in september 2004 samen met de release van "2.3" (ACR en DNG Converter). In februari 2005 werd versie 1.1.0.0 gepubliceerd. In mei 2008 werd versie 1.2.0.0 uitgebracht en gebruikt in "4.4". Versie 1.3.0.0 werd gepubliceerd in juni 2009. Versie 1.4.0.0 verscheen in 2012.

## DNG-bestandsindeling

Terwijl Camera Raw-bestanden onverwerkte of weinig verwerkte gegevens rechtstreeks van de sensor vastleggen. Omdat ze vergelijkbaar zijn met filmnegatieven, worden Camera Raw-formaten ook wel "digitale negatieven" genoemd. Voordeel van onbewerkte formaten is de grotere artistieke controle voor de eindgebruiker. De gebruiker kan verschillende parameterbereiken aanpassen aan de vereisten, zoals witbalans, tonemapping, ruisonderdrukking, verscherping enzovoort. Aan de andere kant moet het Camera Raw-bestand voor elk gebruik worden verwerkt via software of via een converter.

Omdat er geen standaardformaat beschikbaar was voor Camera Raw-bestanden, zorgde dit voor meerdere problemen voor de eindgebruiker. Deze problemen zijn verholpen door Adobe en hebben een niet-eigen indeling voor Camera Raw-bestanden gedefinieerd. Het formaat staat bekend als Digital Negative of DNG. DNG kan worden gebruikt door een breed scala aan hardware en software voor de verwerking van onbewerkte bestanden. Bovendien kan DNG ook worden gebruikt als een tussenformaat voor het opslaan van afbeeldingen die oorspronkelijk zijn vastgelegd door camera's met hun eigen gepatenteerde onbewerkte formaten.

### Specificaties DNG-bestandsindeling

In deze sectie zullen we het DNG-formaat beschrijven als een uitbreiding van TIFF 6.0.

* **Bestandsextensies**: DNG gebruikt de extensies ".DNG" of ".TIF".
* **SubIFD Trees**: DNG ondersteunt geen SubIFD-ketens, maar DNG raadt het gebruik van SubIFD-trees aan zoals vermeld in de TIFF-EP-specificaties. De hoogste kwaliteit en resolutie kunnen NewSubFileType van 0 gebruiken, terwijl de miniaturen van lagere kwaliteit NewSubFileType gelijk aan 1 moeten gebruiken. Het wordt ook aanbevolen, maar niet vereist, dat de eerste IFD een miniatuur van lage kwaliteit of resolutie moet hebben.
* **Bytevolgorde**: Bytevolgorde moet worden ondersteund door DNG-lezers, ook voor bestanden van een bepaald cameramodel.
* **Gemaskeerde pixels**: de meeste camerasensoren berekenen volledig gemaskeerde pixels aan de rand van de sensor door middel van zwarte codering. Deze pixels kunnen worden opgenomen of bijgesneden voordat de afbeelding in DNG-indeling wordt opgeslagen. Als de gemaskeerde pixels niet worden bijgesneden, moet het gebied van deze pixels worden vermeld in de ActiveArea-tag. De informatie die uit deze pixels wordt verzameld over het zwartcoderingsniveau, moet worden gebruikt voordat de onbewerkte gegevens worden opgeslagen of kan worden opgenomen in een DNG-bestand waarin het zwartniveau wordt gespecificeerd.
* **Defecte pixels**: voordat u onbewerkte gegevens als DNG opslaat, moeten defecte pixels worden uitgesloten.
* **Metadata**: Metadata kan op een van de volgende manieren in DNG worden opgenomen:
** Door TIFF-EP- of EXIF-metadatatags te gebruiken
** Via de IPTC-metadatatag (33723)
** De XMP-metadatatag gebruiken (700)
* **Gepatenteerde gegevens**: normaal gesproken nemen leveranciers eigen gegevens op in onbewerkte bestanden die door hun eigen converters kunnen worden gebruikt. DNG slaat hun eigen gegevens op in privétags, privé-IFD's en in een privé MakerNote. Leveranciers moeten de DNGPrivateData- en MakerNoteSafety-tags gebruiken om ervoor te zorgen dat toepassingen die DNG-bestanden bewerken deze eigen gegevens behouden.

Hieronder volgen enkele belangrijke beperkingen en extensies TIFF-tags.

**Bits per monster**

8 tot 32 bits/sample worden ondersteund. Elke sample moet dezelfde diepte hebben als SamplesPerPixel niet gelijk is aan 1. Maar als BitsPerSample niet gelijk is aan 8 of 16 of 32, dan moeten bits in bytes worden verpakt met de TIFF-standaard FillOrder van 1 (big-endian).

**Compressie**

Er worden twee compressietagwaarden ondersteund:

* Waarde #1: ongecomprimeerde data.
* Waarde # 7: JPEG-gecomprimeerde gegevens, ofwel baseline DCT JPEG of lossless JPEG-compressie.

**Fotometrische interpretatie**

De volgende waarden worden alleen ondersteund voor miniatuur- en voorbeeld-IFD's:

* 1 = ZwartIsZero. Aangenomen in een gamma 2.2 kleurruimte.
* 2 = RGB. Aangenomen in de sRGB-kleurruimte.
* 6 = YCbCr. Gebruikt voor JPEG-gecodeerde voorbeeldafbeeldingen.

De volgende waarden worden ondersteund voor de onbewerkte IFD en worden verondersteld de oorspronkelijke kleurruimte van de camera te zijn:

* 32803 # CFA (kleurenfilterarray).
* 34892 # LinearRaw.

**Oriëntatie**

Oriëntatietag wordt gebruikt voor bestandsbrowsers, zodat ze DNG-bestanden zonder verlies kunnen roteren. DNG-lezers moeten alle mogelijke oriëntaties ondersteunen, inclusief gespiegelde oriëntaties.

## Functies in de nieuwste versie van DNG

DNG versie 1.4 oktober 2012 heeft de volgende geavanceerde functies.

* Standaard gebruikers bijsnijden
* Transparantie
* Zwevende komma (HDR)
* Compressie met verlies
* Volmachten

## Referenties ##

* [DNG-specificaties - door Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0.0.pdf)
* [Digital Negative - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - het openbare archiefformaat voor onbewerkte gegevens van digitale camera's](https://helpx.adobe.com/photoshop/digital-negative.html)

