{
  "date" : "2019-10-11",
  "keywords" :[ "dng-fil", "dng-filformat", "vad är en dng-fil", "fil", "dng-exempel", "dng-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Digital Camera Image File Format",
  "description":"Läs mer om DNG-filformat och API:er som kan skapa och öppna DNG-filer.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en DNG fil?

DNG är ett digitalkamerabildformat som används för lagring av råfiler. Den har utvecklats av Adobe i september 2004. Den utvecklades i princip för digital fotografering. DNG är en förlängning av standardformatet [TIFF](/sv/image/tiff/)/EP och använder metadata avsevärt. För att manipulera rådata från digitalkameror med enkel flexibilitet och konstnärlig kontroll väljer fotografer Camera Raw-filer. JPEG- och TIFF-format lagrar bilder som bearbetas av kameran, därför finns det inte mycket utrymme för förändringar i sådana format.

## Historik och versioner av DNG-filformat

Hittills har det funnits 5 versioner av DNG-specifikationen hittills. Version 1.0.0.0 lanserades i september 2004 tillsammans med lanseringen av "2.3" (ACR och DNG Converter). I februari 2005 publicerades version 1.1.0.0. I maj 2008 släpptes version 1.2.0.0 och användes i "4.4". Version 1.3.0.0 publicerades i juni 2009. Version 1.4.0.0 publicerades 2012.

## DNG-filformat

Medan Camera Raw-filer fångar obearbetade eller lågbearbetade data direkt från sensorn. Eftersom de liknar filmnegativ är Camera Raw-format också kända som "Digital Negatives". Fördelen med råformat är den ökade konstnärliga kontrollen för slutanvändaren. Användaren kan justera olika parameterområden enligt kraven såsom vitbalans, tonkartläggning, brusreducering, skärpa och så vidare. Å andra sidan måste Camera Raw-filen bearbetas för all användning genom vilken programvara som helst eller genom en omvandlare.

Eftersom det inte fanns något standardformat tillgängligt för Camera Raw-filer skapade det flera problem för slutanvändaren. Dessa problem åtgärdades av Adobe och definierade ett icke-proprietärt format för Camera Raw-filer. Formatet är känt som Digital Negative eller DNG. DNG kan användas av ett brett utbud av hårdvara och mjukvara för bearbetning av råfiler. Dessutom kan DNG också användas som ett mellanformat för att lagra bilder som ursprungligen tagits av kameror som har sina egna proprietära råformat.

### Specifikationer för DNG-filformat

I det här avsnittet kommer vi att beskriva DNG-formatet som en förlängning av TIFF 6.0.

* **Filtillägg**: DNG använder tilläggen ".DNG" eller ".TIF".
* **SubIFD-träd**: DNG stöder inte SubIFD-kedjor, istället rekommenderar DNG användning av SubIFD-träd som nämns i TIFF-EP-specifikationerna. Högsta kvalitet och upplösning kan använda NewSubFileType på 0, medan miniatyrbilder av reducerad kvalitet bör använda NewSubFileType lika med 1. Det rekommenderas även men inte nödvändigt att den första IFD:n måste ha en miniatyr av låg kvalitet eller upplösning.
* **Byteordning**: Byteordning måste stödjas av DNG-läsare, även för filer från en viss kameramodell.
* **Maskade pixlar**: De flesta kamerasensorer beräknar helt maskerade pixlar vid sensorns kant genom svart kodning. Dessa pixlar kan antingen inkluderas eller trimmas innan bilden lagras i DNG-format. Om de maskerade pixlarna inte trimmas, måste området för dessa pixlar anges i ActiveArea-taggen. Informationen som samlas in från dessa pixlar om svartkodningsnivån bör användas antingen innan rådata lagras eller kan inkluderas i DNG-fil som anger nivån för svart.
* **Defekta pixlar**: Innan du lagrar rådata som DNG bör defekta pixlar uteslutas.
* **Metadata**: Metadata kan inkluderas i DNG på något av följande sätt:
** Genom att använda TIFF-EP- eller EXIF-metadatataggar
** Genom IPTC-metadatataggen (33723)
** Använda XMP-metadatataggen (700)
* **Proprietära data**: Normalt inkluderar leverantörer proprietära data i råfil som ska användas av deras egna omvandlare. DNG lagrar sina egna data i privata taggar, privata IFD:er och i en privat MakerNote. Leverantörer måste använda DNGPrivateData- och MakerNoteSafety-taggarna för att se till att applikationer som redigerar DNG-filer bevarar denna proprietära data.

Följande är några viktiga begränsningar och tillägg TIFF-taggar.

**BitsPerSample**

8 till 32 bitar/sampel stöds. Det måste finnas samma djup för varje sampel när SamplesPerPixel inte är lika med 1. Men om BitsPerSample inte är lika med 8 eller 16 eller 32, måste bitar packas i byte med TIFF standard FillOrder på 1 (big-endian).

**Kompression**

Två komprimeringstaggvärden stöds:

* Värde # 1: Okomprimerad data.
* Värde #7: JPEG-komprimerad data, antingen baslinje DCT JPEG eller förlustfri JPEG-komprimering.

**Fotometrisk tolkning**

Följande värden stöds endast för miniatyrbilder och förhandsgranskningar:

* 1 = BlackIsZero. Antas vara i en gamma 2.2 färgrymd.
* 2 = RGB. Antas vara i sRGB-färgrymden.
* 6 = YCbCr. Används för JPEG-kodade förhandsvisningsbilder.

Följande värden stöds för rå IFD och antas vara kamerans ursprungliga färgrymd:

* 32803 # CFA (Color Filter Array).
* 34892 # LinearRaw.

**Orientering**

Orienteringstagg används för filwebbläsare så att de kan utföra förlustfri rotation av DNG-filer. DNG-läsare måste stödja alla möjliga orienteringar, inklusive speglade orienteringar.

## Funktioner i senaste versionen av DNG

DNG version 1.4 oktober 2012 har följande avancerade funktioner.

* Standard användarbeskärning
* Transparens
* Flytpunkt (HDR)
* Förlustkompression
* Ombud

## Referenser ##

* [DNG-specifikationer - av Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0.0.pdf)
* [Digital Negative - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG – det offentliga arkivformatet för digitalkamera rådata](https://helpx.adobe.com/photoshop/digital-negative.html)

