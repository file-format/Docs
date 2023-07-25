{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "File", "Format", "Öppna", "Läs", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD Design File Format",
  "description" :"Läs mer om DGN-filformat och API:er som kan skapa och öppna DGN-filer.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Vad är en DGN fil?

En fil med filtillägget .dgn (Design) är en ritningsfil som skapats av och stöds av CAD-applikationer som MicroStation och Intergraph Interactive Graphics Design System. Den används för att skapa och spara design för byggprojekt som motorvägar, broar och byggnader. Formatet liknar Autodesks [DWG](/sv/cad/dwg/) filformat och anses vara dess konkurrent. DNG-filer kan antingen sparas som Intergraph Standard File Format eller V8 DGN. DGN kan konverteras till flera andra format som DWG, [BMP](/sv/image/bmp/), [JPEG](/sv/image/jpeg/), [PDF](/sv/pdf/), [GIF](/sv/image/ gif/) och andra. Den kan öppnas med Autodesk AutoCAD, Bentley View och Bentley Systems MicroStation förutom andra programvaror som Corel PaintShop Photo Pro och IMSI TurboCAD Deluxe versioner.

## V8 DGN-filformat

En MicroStation V8 DGN-fil består av en eller flera modeller. En modell är en behållare för element. V8 DGN tar bort alla filformatbaserade begränsningar som fanns i tidigare versioner av MicroStation. Följande är en lista över förbättringar i DGN-filformatet.

* Gräns för antalet nivåer i en DGN-fil har tagits bort, och varje nivå namnges och lagras som ett element.
* Den maximala fysiska storleken på DGN-filen har ingen begränsning och begränsas endast av operativsystemet (som NT-gränsen är 4 GB)
* Den maximala storleken på ett enskilt element är 128 KB.
* Det finns ingen gräns för den maximala storleken på en cell.
* Cellnamn är begränsade till cirka 500 tecken.
* Det finns ingen gräns för antalet referenser som kan bifogas en DGN-fil.
* En linjesträng, form eller punktkurva kan ha upp till 5000 hörn.
* Det finns ingen gräns för antalet komponenter i en komplex kedja eller komplex form.
* Det finns ingen gräns för antalet grafiska grupper i en DGN-fil.
* Staketet är parallellt med vyn där det är placerat.
* En enda textrad kan innehålla 65 535 tecken.
* Det finns ingen gräns för den maximala storleken på en textnod.
* Det finns ingen gräns för antalet textnoder i en DGN-fil.
* Varje element har en unik 64-bitars identifierare som inte ändras under elementets livscykel.
* Varje element har en tidsstämpel som anger tidpunkten för den senaste ändringen.

## Referenser

* [DNG - av Wikipedia](https://en.wikipedia.org/wiki/DGN)
* [MicroStation V8 DGN-filformat](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

