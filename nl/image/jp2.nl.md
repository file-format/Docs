{
  "date" : "2019-10-11",
  "keywords" :[ "jp2-bestand", "jp2-bestandsindeling", "wat is een jp2-bestand", "bestand", "jp2-voorbeeld", "jp2-bestandsextensie","extensie", "formaat"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Afbeeldingsbestandsformaat",
  "description":"Meer informatie over JP2-bestandsindelingen en API's die JP2-bestanden kunnen maken en openen.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Wat is een JP2-bestand? ##

JPEG 2000 (**JP2**) is een beeldcoderingssysteem en de modernste beeldcompressiestandaard. Het maakt gebruik van wavelet-technologie om verliesvrije inhoud in elke kwaliteit tegelijk te coderen. Bovendien heeft JPEG 2000, zonder enige substantiële boete in coderingsefficiëntie, de mogelijkheid om dezelfde inhoud op effectieve wijze te benaderen en te decoderen in een verscheidenheid aan andere resoluties en kwaliteiten. De codestromen in JPEG 2000 zijn aanzienlijk schaalbaar met interessegebieden die de mogelijkheid bieden voor ruimtelijke willekeurige toegang.

JPEG 2000 onderscheidt zich als een van de meest schaalbare standaarden. Verschillende delen van een afbeelding kunnen worden opgeslagen met verschillende kwaliteiten. Een opmerkelijke prestatie-escalatie kan worden bereikt door de codestroom op verschillende manieren te bestellen. Desalniettemin vereist JP2 als resultaat van deze flexibiliteit complexe en rekenkundig uitdagende encoders/decoders. In vergelijking met JPEG produceert JPEG 2000 alleen rinkelende artefacten die ringen nabij de beeldrand maken en wazig kunnen zijn, terwijl JPEG 8×8 visuele artefactenblokken gebruikt die zowel rinkelende als blokkerende artefacten kunnen zijn. Met tot 16384 verschillende componenten met afmetingen in terapixels en een precisie die kan oplopen tot 38 bits/sample.

## Geschiedenis ##

In 2000 ontwierp de Joint Photographic Experts Group-commissie JP2 met als doel om hun eigen op discrete cosinustransformatie gebaseerde JPEG-standaard te verbeteren met deze nieuwe op wavelet gebaseerde methode. De JPEG-commissie wilde hun basismethoden vrij van licentiekosten aanbieden. In de JP2-licentie die concurrentie kreeg van 20 bedrijven, wonnen ze met een snor. JPEG 2000 is uitgeroepen tot ISO-standaard, hoewel de meeste webbrowsers sinds 2017 niet klaar zijn om JPEG 2000 een handje te helpen.

## Onderdelen van JPEG 2000 beeldcoderingssysteem ##

Hieronder volgen de belangrijkste onderdelen die de volledige reeks standaarden voor JPEG 2000 vormen.


|Deel|Titel|Beschrijving|Nummer
---|---|---|---|
|Deel 1|Kerncoderingssysteem| Definieert de syntaxis van de codestroom. Verschillende fasen betrokken bij het decoderen van JPEG 2000-afbeeldingen. Legt het basisbestandsformaat JP2, metadata en IP-rechten uit die moeten worden verstrekt.|ISO/IEC 15444-1
|Deel 2|Extensies|Definieert extensies voor de stream van bestandsformaatcodes en maakt demonstraties van HDR-voorbeelden, kleurruimtespecificatie, bijsnijden, geometrische transformaties mogelijk; diverse animaties, metadata en meerdere codestreams.|ISO/IEC 15444-2
|Deel 3|Motion JPEG 2000 (MJ2 of MJP2)|Introduceer een bestandsformaat voor bewegingssequenties, het coderen van beelden in een onafhankelijke codestroom.|ISO/IEC 15444-3
|Deel 4|Conformiteit|Vermeldt testtechnieken voor codering en decodering en controleert bestanden op zowel bare-codestreams als JP2-bestanden.|ISO/IEC 15444-4
|Deel 5|Referentiesoftware|Bestaat uit twee broncodepakketten (Java, C) die het Core-coderingssysteem implementeren en beschikbaar zijn onder open-sourcelicenties.|ISO/IEC 15444-5
|Deel 6|Samengestelde afbeeldingsbestandsindeling|Definieert de JPM-bestandsindeling en maakt het mogelijk om documenten van meerdere pagina's te maken voor faxachtige toepassingen. Ondersteunt het gebruik van JBIG2 en JPEG.|ISO/IEC 15444-6
|Deel 8|JPEG 2000 Secured (JPSEC)|Zorgt voor de veiligheid van transacties, inhoud en technologieën en maakt beveiligde JPEG 2000-bits streams mogelijk.|ISO/IEC 15444-8
|Deel 9|JPIP|Definieert tools in een netwerkomgeving voor toegang tot metadata en beelden, en stelt interactieve en efficiënte protocollen vast|ISO/IEC 15444-9
|Deel 10|JP3D|Volumetrische uitbreiding van deel 1 en introduceert de Z-dimensie. Breidt het concept van tegels, codeblokken, terreinen en toegankelijkheidsfuncties voor 3D-regio's uit.|ISO/IEC 15444-10
|Deel 11|JPWL|Behandelt goed georganiseerde verzending via een foutgevoelig draadloos netwerk. Deze uitbreiding is compatibel met decoders|ISO/IEC 15444-11
|Deel 13|Encoder op instapniveau|Definieert een encoderimplementatie op instapniveau van het Core-coderingssysteem.|ISO/IEC 15444-13
|Deel 14|JPXML|Een weergave in XML en uitleg over markeringssegmenten en methoden voor toegang tot de interne gegevens van afbeeldingen.|ISO/IEC 15444-14
|Deel 15|HTJ2K (in ontwikkeling)|Specificeert een alternatief blokcoderingsalgoritme. Algoritme biedt een tienvoudig verhoogde doorvoer en verliesloos coderen/decoderen.|

## JP2-bestandsindeling ##

JPEG 2000 definieert zowel het bestandsformaat als de codestream op dezelfde manier als JPEG-1. Hoewel afbeeldingsvoorbeelden exclusief worden beschreven door JPEG 2000, bevat JPEG-1 andere toegevoegde informatie over de kleurruimte en resolutie die essentieel zijn om de afbeelding te coderen. Als een afbeelding is opgeslagen als JPEG 2000-bestand, wordt de **.jp2** als extensie gebruikt. Dit bestandsformaat wordt verder verbeterd door de JPEG 2000 part-2-extensie, die animatiemechanismen en configuratie van talrijke codestromen in één enkele afbeelding definieert. De extensie **.jpx** wordt gebruikt wanneer afbeeldingen worden opgeslagen met dit uitgebreide bestandsformaat. Aangezien codestreamgegevens niet in de eerste plaats in bestanden worden opgeslagen, is er voor dit doel geen standaardextensie gedefinieerd. Voor testdoeleinden krijgt het echter vaak de extensie **.jpc** of **.j2k**. In tegenstelling tot JPEG-1 kiest JPEG 2000 voor een andere manier om metadata in XML-formaat te coderen. De norm 12234-1.4 (door de ISO TC42-commissie) wordt gebruikt als referentie tussen de Exif-tags en de XML-componenten. JPEG 2000 kan een ISO-standaard bevatten, met daarin XMP.

### Brokken ###
JPEG 2000-bestanden bestaan uit opeenvolgende brokken. Elke chunk heeft een header van 8 bytes: een chunkgrootte van 4 bytes (big-endian, eerst high-byte) en een chunktype van 4 bytes - een van de vooraf gedefinieerde handtekeningen: "jP" of "jP2".

Het tweede blok moet van het type "ftyp" zijn en heeft een subtype op offset 8. JPEG 2000 gedefinieerd door een subtype dat een van de volgende waarden moet zijn: "jp2 "(bestandstype \*.JP2), "jp20" (bestand typ \*.JPA), "jpm" (bestandstype \*.JPM), "jpx" (bestandstype \*.JPX).

Door stukjes te herhalen, totdat een onbekend type wordt gedetecteerd, stellen we een JPEG 2000-beeld-/videobestand samen.

### Kleurtransformatie ###

In eerste instantie is de transformatie van afbeeldingen van RGB-kleurruimte naar een andere kleurruimte vereist. Hiervoor zijn er twee manieren: Irreversible Color Transform (ICT) en Reversible Color Transform (RCT). Eerstgenoemde gebruikt YC,,B,,C,,R,, kleurruimte en moet worden geïmplementeerd in fix/floating-point, terwijl later een gewijzigde YUV-kleurruimte en omkeerbaar van aard is.// //Niet beperkt tot RGB-model, JPEG 2000-taal maakt gebruik van transformatie met meerdere componenten.

### Tegels ###

Wanneer de kleurtransformatie is voltooid, wordt de afbeelding geconverteerd naar rechthoekige gebieden die tegels worden genoemd en die afzonderlijk kunnen worden getransformeerd en gecodeerd. De grootte van alle tegels is hetzelfde of de hele afbeelding kan als één enkele tegel worden beschouwd. Decoder maakt gebruik van tegels en verbruikt minder geheugen of kan sommige tegels gedeeltelijk coderen. Hoewel deze techniek een nadeel heeft van kwaliteitsvermindering van het beeld.

### Wavelet-transformatie ###

Afbeelding na betegeling wordt wavelet-getransformeerd dat ofwel onomkeerbaar of omkeerbaar kan zijn en geïmplementeerd met behulp van het convolutie- of hefschema.

### Compressieverhouding ###

Afhankelijk van de fysieke kenmerken van een afbeelding, wordt een compressieversterking van 20% verkregen. Ruimtelijke redundantievoorspelling van JPEG 2000 speelt een cruciale rol in het compressieproces en afbeeldingen met een hoge resolutie hebben de neiging om het meeste voordeel te behalen.

## Toepassingen bediend door de standaard ##

* Opnemen, bewerken en opslaan van op frames gebaseerde HD-video's
* Medische beelden en biometrie
* satellietbeelden, remote sensing en bewegingsdetectie
* Client/server communicatie, netwerkdistributie en opslag.
* Digitale bioscoop, Live HDTV-feedbijdrage, gedigitaliseerde audiovisuele dingen

## Referenties ##

* [Overzicht van JPEG 2000](https://jpeg.org/jpeg2000)
* [JPEG 2000 beeldcoderingssysteem](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

