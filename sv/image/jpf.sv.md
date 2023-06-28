{
  "date" : "2021-02-10",
  "keywords" :[ "jpf-fil", "jpf-filformat", "vad är en jpf-fil", "fil", "jpf-exempel", "jpf-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPF - Bildfilformat",
  "description":"Läs mer om JPF-filformat och API:er som kan skapa och öppna JPF-filer.",
  "linktitle" : "JPF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## Vad är JPF fil? ##

En fil med filtillägget .jpf är ett tillägg till JPEG 2000 bildkodningssystemet ISO/IEC 15444 och kallas dess del 2 ISO/IEC 15444-2. Den definierar och specificerar en uppsättning förlustfria (bitbevarande) och förlustfria komprimeringsmetoder för kodning av kontinuerliga toner, bi-nivå, gråskala, digitala färgstillbilder eller flerkomponentsbilder. Den första delen av ISO/IEC 15444-1 hänvisas till [JP2](/sv/image/jp2/) som använder wavelet-tekniken för att koda förlustfritt innehåll och är basen för JPEG 2000-bildfilformat. JPF-filformatet fick ingen varm mottagning på grund av den omfattande användningen av JPEG-format. JPF-filer kan öppnas med populära bildbehandlingsprogram som Adobe Photoshop 2020, Adobe Illustrator 2020 och CorelDraw Graphics Suite 2020.

## Kortfattad bakgrund

År 2000 designade Joint Photographic Experts Group-kommittén JP2 med målet att förbättra sin egen diskreta cosinustransformationsbaserade JPEG-standard med denna nya wavelet-baserade metod. JPEG-kommittén hade som mål att tillhandahålla sina baslinjemetoder fria från licensavgifter. I JP2-licensen som fick konkurrens bland 20 företag vann de med ett morrhår. JPEG 2000 har deklarerats som en ISO-standard, även om de flesta webbläsare inte är redo att ge en hand till JPEG 2000 sedan 2017. 2004 accepterades ISO/IEC 15444-2-formatet offentligt som tillägg till JP2-filformatet.

## JPF filformat

JPF-filformatet definierar utökade avkodningsprocesser för konvertering av komprimerade bilddata för rekonstruktion. Det är ett utökat filformat som specificerar utökad kodströmssyntax som innehåller information för tolkning av komprimerad bilddata. Denna utökade standard specificerar en behållare för att lagra bildmetadata och ger vägledning om utökade kodningsprocesser för att konvertera källbilddata till komprimerad bilddata.

### Filorganisation

JPF är det formella lagringsfilformatet när JPX-filer lagras i datorfilsystem. Dessutom kan andra rekommendationer/internationella standarder definiera andra rutor för användning i JPX-filer. All information som finns i en JPX-fil ska dock vara i boxformat; byteströmmar som inte är i boxformatet ska inte hittas i filen. Den binära strukturen för en ruta i en JPX-fil är identisk med den som definieras i filformatet [JP2](/sv/image/jp2/).

## Referenser ##

* [Översikt över JPEG 2000](https://jpeg.org/jpeg2000/)
* [ISO/IEC 15444-2:2004](https://www.iso.org/standard/33160.html)

