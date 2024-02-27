{
  "date": "2019-10-11",
  "keywords": [
"dng fil",
"dng filformat",
"hvad er en dng fil",
"fil",
"dng eksempel",
"dng filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DNG - Digital Camera Image File Format",
  "description": "Lær om DNG-filformat og API'er, der kan oprette og åbne DNG-filer.",
  "linktitle": "DNG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dn-dag"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en DNG fil?

DNG is a digital camera image format used for the storage of raw files. It has been developed by Adobe in September 2004. Det er grundlæggende udviklet til digital fotografering. DNG er en udvidelse af [TIFF](/image/tiff/)/EP standardformatet og bruger metadata betydeligt. For at manipulere rådata fra digitale kameraer med den lette fleksibilitet og kunstneriske kontrol, vælger fotografer Camera Raw-filer. JPEG- og TIFF-formater gemmer billeder, der behandles af kameraet, og derfor er der ikke meget plads til ændringer tilgængelig i sådanne formater.

## Historie og versioner af DNG-filformat

Till now there have been 5 versions of DNG specification so far. Version 1.0.0.0 was launched in September 2004 along with the release of "2.3" (ACR and DNG Converter). In February 2005 version 1.1.0.0 was published.  In May 2008 version 1.2.0.0 was released and was used in "4.4". Version 1.3.0.0 was published in June 2009. Version 1.4.0.0 dukkede op i 2012.

## DNG filformat

Hvorimod Camera Raw-filer fanger ubehandlede eller lavt behandlede data direkte fra sensoren. Da de ligner filmnegativer, er Camera Raw-formater også kendt som Digital Negatives. Fordelen ved råformater er den øgede kunstneriske kontrol for slutbrugeren. Brugeren kan justere forskellige parameterområder i henhold til kravene såsom hvidbalance, tonekortlægning, støjreduktion, skarphed og så videre. På den anden side skal Camera Raw-filen behandles til enhver brug gennem enhver software eller gennem en konverter.

Da der ikke var noget standardformat tilgængeligt for Camera Raw-filer, skabte det derfor flere problemer for slutbrugeren. Disse problemer blev løst af Adobe og definerede et ikke-proprietært format for Camera Raw-filer. Formatet er kendt som Digital Negative eller DNG. DNG kan bruges af en bred vifte af hardware og software til behandling af råfiler. Ydermere kan DNG også bruges som et mellemformat til lagring af billeder, som oprindeligt blev optaget af kameraer med deres egne proprietære råformater.

### DNG-filformatspecifikationer

I dette afsnit vil vi beskrive DNG-formatet som en udvidelse af TIFF 6.0.

* **Filudvidelser**: DNG bruger ".DNG"- eller ".TIF"-udvidelser.

* **SubIFD-træer**: DNG understøtter ikke SubIFD-kæder, i stedet anbefaler DNG brugen af SubIFD-træer som nævnt i TIFF-EP-specifikationerne. Højeste kvalitet og opløsning kan bruge NewSubFileType på 0, mens miniaturebilleder af reduceret kvalitet skal bruge NewSubFileType lig med 1. Det anbefales også, men ikke påkrævet, at den første IFD skal have en miniature af lav kvalitet eller opløsning.

* **Bytebestilling**: Bytebestilling skal understøttes af DNG-læsere, også for filer fra en bestemt kameramodel.

* **Maskede pixels**: De fleste af kamerasensorerne beregner fuldt maskerede pixels ved kanten af sensoren gennem sort kodning. Disse pixels kan enten inkluderes eller trimmes, før billedet gemmes i DNG-format. Hvis de maskerede pixels ikke trimmes, skal arealet af disse pixels nævnes i ActiveArea-tagget. Oplysningerne indsamlet fra disse pixels om sortkodningsniveau skal bruges til enten før de rå data gemmes eller kan inkluderes i DNG-filen, der angiver niveauet for sort.

* **Defekte pixels**: Før du lagrer rådata som DNG, skal defekte pixels udelukkes.

* **Metadata**: Metadata kan inkluderes i DNG på en af følgende måder:  

** Ved at bruge TIFF-EP eller EXIF metadata tags
** Gennem IPTC-metadata-tagget (33723)
** Brug af XMP-metadata-tagget (700)
* **Ejendomsbeskyttede data**: Normalt inkluderer leverandører proprietære data i råfil, der skal bruges af deres egne konvertere. DNG gemmer deres proprietære data i private tags, private IFD'er og i en privat MakerNote. Leverandører skal bruge DNGPrivateData- og MakerNoteSafety-tags for at sikre, at applikationer, der redigerer DNG-filer, bevarer disse proprietære data.


Følgende er nogle vigtige begrænsninger og udvidelser TIFF-tags.

**BitsPerSample**

8 til 32 bits/sample er understøttet. Der skal være samme dybde for hver sample, når SamplesPerPixel ikke er lig med 1. Men hvis BitsPerSample ikke er lig med 8 eller 16 eller 32, så skal bits pakkes i bytes ved hjælp af TIFF standard FillOrder på 1 (big-endian).

**Kompression**

To Compression tag-værdier understøttes:

* Værdi # 1: Ukomprimerede data.

* Værdi #7: JPEG-komprimerede data, enten baseline DCT JPEG eller tabsfri JPEG-komprimering.


**Fotometrisk fortolkning**

Følgende værdier understøttes kun for miniaturebilleder og forhåndsvisninger af IFD'er:

* 1 = BlackIsZero. Antages at være i et gamma 2.2 farverum.

* 2 = RGB. Antages at være i sRGB-farverummet.

* 6 = YCbCr. Bruges til JPEG-kodede forhåndsvisningsbilleder.


Følgende værdier understøttes for den rå IFD og antages at være kameraets oprindelige farverum:

* 32803 # CFA (Color Filter Array).

* 34892 # LinearRaw.


**Orientering**

Orientation tag bruges til filbrowsere, så de kan udføre tabsfri rotation af DNG-filer. DNG-læsere skal understøtte alle mulige orienteringer, inklusive spejlede orienteringer.

## Funktioner i seneste version af DNG

DNG Version 1.4 oktober 2012 har følgende avancerede funktioner.

* Standard brugerbeskæring

* Gennemsigtighed

* Flydende punkt (HDR)

* Lossy Compression

* Fuldmagter


## Referencer ##

* [DNG-specifikationer - af Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0 .0.pdf)

* [Digital Negative - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)

* [DNG - Det offentlige arkivformat for digitalkamera-rådata](https://helpx.adobe.com/camera-raw/digital-negative.html)


