{
  "date" : "2020-01-10",
  "keywords" :[ "dib-bestand", "dib-bestandsindeling", "wat is een dib-bestand", "bestand", "dib-voorbeeld", "dib-bestandsextensie","extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Meer informatie over DIB-bestandsindeling en API's die DIB-bestanden kunnen maken en openen.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Wat is een DIB-bestand?

Een apparaatonafhankelijke bitmap (DIB) is een rasterafbeeldingsbestand dat qua structuur vergelijkbaar is met de standaard bitmapbestanden ([BMP]()/image/bmp/)). Het bevat een kleurentabel die de toewijzing van RGB-kleuren aan de pixelwaarden beschrijft. Hierdoor kan DIB afbeeldingen op elk apparaat weergeven. Het kan worden geopend met bijna alle toepassingen die een standaard BMP-bestand op Windows en macOS kunnen openen. DIB zijn binaire bestanden en hebben een complexe bestandsindeling die lijkt op BMP. DIB-afbeeldingen zijn onafhankelijk van de uitvoermogelijkheden van weergaveapparaten in termen van kleurdiepte en pixel-per-inch.

## Specificaties DIB-bestandsindeling ##
Een DIB bevat de volgende kleur- en afmetingsinformatie:

* Het kleurformaat van het apparaat waarop de rechthoekige afbeelding is gemaakt.
* De resolutie van het apparaat waarop de rechthoekige afbeelding is gemaakt.
* Het palet voor het apparaat waarop de afbeelding is gemaakt.
* Een array van bits die rode, groene, blauwe (RGB) triolen toewijst aan pixels in de rechthoekige afbeelding.
* Een identificatiecode voor gegevenscompressie die het gegevenscompressieschema (indien aanwezig) aangeeft dat wordt gebruikt om de grootte van de reeks bits te verkleinen.

### DIB-gegevensblokformaat ###

DIB komt in de context van geheugenblok in vergelijking met .DIB-bestanden die op schijf zijn opgeslagen. Het geheugenblok bestaat uit een structuur die in overeenstemming is met de Windows API-specificaties voor DIB's. Daadwerkelijke DIB bestaat uit:
* Een kop
* Kleurenpalet
* Pixelgegevens

In de praktijk wordt het werken met palet-, koptekst- en afbeeldingsgegevens gedaan alsof het drie afzonderlijke geheugenblokken zijn. Een handvat aan dit gemeenschappelijke geheugenblok wordt toegewezen met behulp van GlobalAlloc en staat bekend als HDIB, dat wordt gebruikt om de koptekst, kleurentabel en pixelgegevens te extraheren en ermee te werken.

### Structuren ###
Informatie in een DIB wordt weergegeven door verschillende structuren. Waaronder:

BITMAPInfo - Definieert de dimensie- en kleurinformatie voor een DIBs
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Het bestaat uit een BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
gevolgd door twee of meer RGBQAD-structuren.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Gegevensbits ###
|Bits|Beschrijving|
---|---|
|1-bits formaat (monochroom)|Monochroom bitmaps bestaan uit twee kleuren (zwart en wit). Door dit beperkte aantal kleuren nemen deze bitmaps minder ruimte in beslag op de schijf. De bitBitCount retourneert waar of onwaar voor de weergave van beide kleuren. De meeste toepassingen slaan het palet volledig over als bitBitCount==1.
|4-bits formaat (VGA of 16 kleuren)|Elke byte beeldgegevens vertegenwoordigt twee pixels en bitBitCount==4. Deze bits vertegenwoordigen de kleur van de pixel in aflopende volgorde.
|8-bits formaat (256 kleuren)|Dit 8-bits formaat kan maximaal 256 kleuren vertegenwoordigen. Elke byte in de bitmapgegevensarray van de afbeelding vertegenwoordigt een enkele pixel. De waarde van die byte is het nummer van het kleurenpalet dat moet worden gebruikt uit de 256 ingangen zoals weergegeven door de bmciColors.
|24-bits formaat (TrueColor)|Deze bitmaps kunnen maximaal 2^24 kleuren hebben (biBitCount == 24). Elke reeks van drie bytes in de bitmapgegevensarray vertegenwoordigt de relatieve intensiteit van de drie primaire tinten van een pixel. De tinten worden beschreven als waarden van 0 tot 255 en worden opgeslagen in de drie bytes in de volgorde Blauw, Groen en Rood. Dit is een belangrijk onderscheid, omdat de meeste verwijzingen naar kleuren in Windows de tegenovergestelde volgorde gebruiken: Rood/Groen/Blauw, dus denk aan "BGR" wanneer u met TrueColor-afbeeldingen werkt in plaats van "RGB". Er kan een kleurenpalet worden opgegeven om het tekenproces voor Windows te versnellen, in welk geval biClrUsed niet 0 is. Maar zoals u kunt zien, is dit niet nodig, omdat de pixelgegevens zelf de kleurinformatie bevatten.
|32-bits formaat|32-bits afbeeldingen hebben maximaal 2^24 kleuren (biBitCount == 24).

## Referenties ##
* [Apparaatonafhankelijke bitmaps - door Microsoft](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

