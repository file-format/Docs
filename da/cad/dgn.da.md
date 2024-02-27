{
  "date": "2020-01-12",
  "keywords": [
"DGN",
"Fil",
"Format",
"Åben",
"Læs",
"API",
"MicroStation",
"Intergraph interaktivt grafisk designsystem"
],
  "author":{
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DGN - MicroStation CAD-designfilformat",
  "description": "Lær om DGN filformat og API'er, der kan oprette og åbne DGN filer.",
  "linktitle": "DGN",
  "menu":{
    "docs":{
      "parent": "cad",
      "identifier": "cad-dg-dan"
}
},
  "lastmod": "2020-01-12"
}

## Hvad er en DGN fil?

En fil med filtypenavnet .dgn (Design) er en tegnefil, der er oprettet af og understøttet af CAD-applikationer såsom MicroStation og Intergraph Interactive Graphics Design System. Det bruges til at skabe og gemme design til byggeprojekter såsom motorveje, broer og bygninger. Formatet ligner Autodesks [DWG](/cad/dwg/) filformat og betragtes som dets konkurrent. DNG-filer kan enten gemmes som Intergraph Standard File Format eller V8 DGN. DGN kan konverteres til flere andre formater såsom DWG, [BMP](/image/bmp/), [JPEG](/image/jpeg/), [PDF](/pdf/), [GIF](/image/gif/) og andre. Den kan åbnes med Autodesk AutoCAD, Bentley View og Bentley Systems MicroStation ud over andre softwareapplikationer som Corel PaintShop Photo Pro og IMSI TurboCAD Deluxe versioner.

## V8 DGN filformat

En MicroStation V8 DGN-fil er sammensat af en eller flere modeller. En model er en beholder til elementer. V8 DGN fjerner alle filformatbaserede begrænsninger, der var til stede i tidligere versioner af MicroStation. Følgende er en liste over forbedringer i DGN-filformatet.

 * Begrænsningen for antallet af niveauer i en DGN-fil er blevet fjernet, og hvert niveau navngives og gemmes som et element.
 * Den maksimale fysiske størrelse af DGN-filen har ingen begrænsninger og er kun begrænset af operativsystemet (såsom NT-grænsen er 4 GB)
 * Den maksimale størrelse af et enkelt element er 128 KB.
 * Der er ingen grænse for den maksimale størrelse af en celle.
 * Cellenavne er begrænset til cirka 500 tegn.
 * Der er ingen grænse for antallet af referencer, der kan vedhæftes til en DGN-fil.
 * En linjestreng, form eller punktkurve kan have op til 5000 hjørner.
 * Der er ingen grænse for antallet af komponenter i en kompleks kæde eller kompleks form.
 * Der er ingen grænse for antallet af grafiske grupper i en DGN-fil.
 * Hegnet er parallelt med det syn, det er placeret i.
 * En enkelt tekstlinje kan indeholde 65.535 tegn.
 * Der er ingen grænse for den maksimale størrelse af en tekstnode.
 * Der er ingen grænse for antallet af tekstnoder i en DGN-fil.
 * Hvert element har en unik 64-bit identifikator, der ikke ændres gennem elementets livscyklus.
 * Hvert element har et tidsstempel, der angiver tidspunktet for den seneste ændring.

## Referencer

* [DNG - af Wikipedia](https://en.wikipedia.org/wiki/DGN)

* [MicroStation V8 DGN File Format](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

