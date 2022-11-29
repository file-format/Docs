{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "fil", "tillägg", "format", "videoformat","Vad är en SWF-fil", "swf-filformat", "swf-filspelare","hur man öppnar en SWF-fil"] ,
  "title" :"SWF-fil - Shockwave Flash Movie File Format",
  "description":"Läs mer om vad en SWF-fil är och API:er som kan skapa och visa hur man öppnar SWF-filen.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en SWF-fil?

En SWF-fil är en animationsfil som skapas med Adobe Flash. Den kan innehålla olika typer av element som text, vektorbilder, rasterbilder, actionscripts, objekt som cirklar, linjer, kvadrater och rektangel för att skapa animationen. SWF-filer arrangerar dessa multimediaobjekt i bildrutor som kan spelas upp på olika bildrutor per sekund (fps). SWF betyder Short Web File men är också känt har Shockwave Format.

Program som kunde *öppna SWF-filer** inkluderade Adobe Flash Player (nu upphört) och Eltima Elmedia Player.

## SWF-filformat - Mer information

SWF-filer användes för att lagras som binära filer på skiva. SWF-filformatet användes för att utveckla animationer och spel som kunde bäddas in på webbplatser och spelas självständigt också. Det stödde också videor och ljud som gav utvecklare många val att skapa interaktiva multimediaapplikationer. SWF-filer kan spelas upp i webbläsare som har Adobe Shockwave installerat. Adobe Flash lades ner i december 2020 på grund av dess brister och säkerhetsproblem.

## Kort historik över SWF-filformat

SWF-filformatet designades ursprungligen av FutureWave Software, för att visa animationer med avsikt att köras på en spelarprogramvara på alla system med långsammare nätverksanslutningar, samtidigt som filstorleken hålls liten. I december 1996 ägde Macromedia FutureWave och konverterade till Macromedia Flash 1.0.

2005 förvärvades Macromedia av Adobe, som tillkännagav SWF som en del av sitt open source-projekt 2008. Under samma år släppte Adobe kod till världens populära webbmotorer för att de skulle kunna genomsöka och indexera SWF-filer. Men eftersom SWF-filer verkar bli ett standardformat för att publicera Flash-innehåll på internet, har SWF:en reviderats till att betyda Small Web Format.

## SWF-filstruktur

Path är det grundläggande grafiska elementet i SWF, som är en sekvens av segment av grundläggande element, allt från enkla linjer till Bezier-kurvor. Dessa enkla element hjälper också till att göra andra extra primitiver som kuber, ellipser och till och med texter. De grafiska primitiverna i SWF har likheter med de grafiska elementen i andra format som SVG och MPEG-4 BIFS.

Visningslistor och återanvändning/byte av redan definierade element tillåts också av formatet. Det binära strömformatet för SWF kan jämföras med QuickTime-atomer som är liknande när det gäller tagg, storlek och nyttolast. Det binära strömformatet tillåter äldre spelare att hoppa över innehåll som inte stöds. Även om originalversioner av SWF var begränsade till att erbjuda vektorgrafik och bilder, tillåter därför nya versioner även ljud- och videoinnehåll.

En ny, lågnivå 3D API för Flash Player med namnet "Stage3D" introducerades i version 11. Detta API var tänkt att vara en motsvarighet till OpenGL eller Direct3D. Stage3D definierar färger i ett lågnivåspråk som kallas Adobe Graphics Assembly Language (AGAL). Följande är några grundläggande datatyper av SWF-filformat.

### Koordinater

XY-koordinater i SWF-filformat lagras som heltal och mäts i en enhet som kallas twip. En twip består av 1/20 av en logisk pixel. Logisk pixel och skärmpixel är samma när filen spelas upp utan skalning till 100 %.

### Heltalstyper och byteordning

De signerade och osignerade heltalstyperna på 8, 16, 32 och 64 bitar är tillåtna i SWF-filformat. Little-endian byte-ordning används för att lagra heltalsvärden. Även inom byte lagras bitordningen i big-endian. Alla heltalsvärden ska vara bytejusterade. Signerade heltal representeras genom att använda traditionella 2-komplement bitmönster.

### Fastpunktsnummer

Två typer av fastpunktsnummer stöds av SWF-filformatet, dvs. 32 och 16 bitar.

### Flyttal

SWF 8 och senare versioner använder tre typer av flyttalstal (FLOAT, FLOAT 16, DOUBLE) som är kompatibla med IEEE Standard 754 för flyttalstyper.

### Kodade heltal

En typ av kodat heltal stöds av SWF 9 och senare med variabelt antal byte.

## Referenser

* [SWF-filformat](https://en.wikipedia.org/wiki/Swf)

