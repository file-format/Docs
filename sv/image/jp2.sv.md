{
  "date" : "2019-10-11",
  "keywords" :[ "jp2 fil", "jp2 filformat", "vad är en jp2 fil", "fil", "jp2 exempel", "jp2 filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JP2 - Bildfilformat",
  "description":"Läs mer om JP2-filformat och API:er som kan skapa och öppna JP2-filer.",
  "linktitle" : "JP2",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-08-10"
}

## Vad är JP2 fil? ##

JPEG 2000 (**JP2**) är ett bildkodningssystem och en toppmodern bildkomprimeringsstandard. Den använder wavelet-teknik för att koda förlustfritt innehåll i valfri kvalitet på en gång. Dessutom har JPEG 2000, utan några betydande straff i kodningseffektivitet, förmågan att komma åt och avkoda samma innehåll effektivt till en mängd andra upplösningar och kvaliteter. Kodströmmarna i JPEG 2000 är avsevärt skalbara med områden av intresse som tillhandahåller möjligheten för rumslig direktåtkomst.

JPEG 2000 framstår som en av de mest skalbara standarderna. Olika delar av en bild kan lagras med olika kvaliteter. En anmärkningsvärd prestandaeskalering kan uppnås genom att beställa kodströmmen på en mängd olika sätt. Ändå kräver JP2 komplexa och beräkningsmässigt utmanande kodare/avkodare, som ett resultat av denna flexibilitet. Jämfört med JPEG producerar JPEG 2000 endast ringartefakter som gör ringar nära bildkanten och kan vara suddiga, medan JPEG använder 8×8 visuella artefakterblock som kan vara både ringande och blockerande artefakter. Innehar upp till 16384 olika komponenter med dimensionerna i terapixels, och precision som kan vara hög som 38 bitar/prov.

## Historik ##

År 2000 designade Joint Photographic Experts Group-kommittén JP2 med målet att förbättra sin egen diskreta cosinustransformationsbaserade JPEG-standard med denna nya wavelet-baserade metod. JPEG-kommittén hade som mål att tillhandahålla sina baslinjemetoder fria från licensavgifter. När JP2-licensen fick konkurrens bland 20 företag vann de med morrhår. JPEG 2000 har deklarerats som en ISO-standard, även om de flesta webbläsare inte är redo att ge en hand till JPEG 2000 sedan 2017.

## Delar av JPEG 2000 bildkodningssystem ##

Följande är huvuddelarna som utgör den kompletta uppsättningen av standarder för JPEG 2000.


|Del|Titel|Beskrivning|Nummer
---|---|---|---|
|Del 1|Kärnkodningssystem| Definierar syntax för kodström. Olika steg involverade i avkodningen av JPEG 2000-bilder. Förklarar grundläggande filformat JP2, metadata och IP-rättigheter som ska tillhandahållas.|ISO/IEC 15444-1
|Del 2|Tillägg|Definierar tillägg för filformatkodström och tillåter HDR-exempeldemonstrationer, färgrymdsspecifikation, beskärning, geometriska transformationer; olika animationer, metadata och flera kodströmmar.|ISO/IEC 15444-2
|Del 3|Motion JPEG 2000 (MJ2 eller MJP2)|Introducera ett filformat för rörelsesekvenser, som kodar bilder i en oberoende kodström.|ISO/IEC 15444-3
|Del 4|Konformans|Anger testtekniker för kodning och avkodning och kontrollerar filer för både blotta kodströmmar och JP2-filer.|ISO/IEC 15444-4
|Del 5|Referensprogramvara|Består av två källkodspaket (Java, C) som implementerar Core-kodningssystem och tillgängliga under öppen källkod.|ISO/IEC 15444-5
|Del 6|Sammansatt bildfilformat|Definierar JPM-filformatet och tillåter flersidig dokumentavbildning för faxliknande applikationer. Stöder användningen av JBIG2 och JPEG.|ISO/IEC 15444-6
|Del 8|JPEG 2000 Secured (JPSEC)|Säkerställer säkerheten för transaktioner, innehåll och teknologier och tillåter säkrade JPEG 2000-bitarsströmmar.|ISO/IEC 15444-8
|Del 9|JPIP|Definierar verktyg i en nätverksmiljö för åtkomst till metadata och bilder, och anger interaktiva och effektiva protokoll|ISO/IEC 15444-9
|Del 10|JP3D|Volumetrisk förlängning av Del 1 och introducerar Z-dimensionen. Utvidgar konceptet med brickor, kodblock, distrikt och 3D-regioner av intresse tillgänglighetsfunktioner.|ISO/IEC 15444-10
|Del 11|JPWL|Gäller välorganiserad överföring över ett felbenäget trådlöst nätverk. Detta tillägg är kompatibelt med avkodare|ISO/IEC 15444-11
|Del 13|Entry-level Encoder|Definierar en ingångsnivåkodarimplementering av Core-kodningssystem.|ISO/IEC 15444-13
|Del 14|JPXML|En representation i XML och förklarar markörsegment och metoder för att komma åt interna data i bilder.|ISO/IEC 15444-14
|Del 15|HTJ2K (Under-utveckling)|Anger en alternativ blockkodningsalgoritm. Algoritmen erbjuder en tiofaldigt ökad genomströmning och förlustfri kodning/avkodning.|

## JP2 filformat ##

JPEG 2000 definierar filformat såväl som kodström på samma sätt som JPEG-1. Även om bildprover uteslutande beskrivs av JPEG 2000, innehåller JPEG-1 ytterligare information om färgrymd och upplösning som är nödvändig för att koda bilden. Om en bild lagras som JPEG 2000-fil, används **.jp2** som tillägg. Detta filformat förbättras ytterligare av JPEG 2000 del-2-tillägget, som definierar animeringsmekanismer och konfiguration av många kodströmmar till en enda bild. **.jpx** tillägget används när bilder sparas med detta utökade filformat. Eftersom kodströmsdata inte anses vara sparad i filer i första hand, så finns inget standardtillägg definierat för detta ändamål. Även för teständamål får den ofta tillägget **.jpc** eller **.j2k**. I motsats till JPEG-1 väljer JPEG 2000 ett annat sätt att koda metadata i XML-format. Standarden 12234-1.4 (av ISO TC42-kommittén) används som referens mellan Exif-taggarna och XML-komponenterna. JPEG 2000 kan innehålla en ISO-standard, XMP inom.

### bitar ###
JPEG 2000-filer består av på varandra följande bitar. Varje chunk har 8 byte header: 4-byte chunk storlek (big-endian, high byte first) och 4-byte chunk typ - en av fördefinierade signaturer: "jP" eller "jP2".

Den andra delen måste vara av typen "ftyp" och ha en undertyp vid offset 8. JPEG 2000 definierad av undertyp som måste vara ett av värdena: "jp2 "(filtyp \*.JP2), "jp20" (fil typ \*.JPA), "jpm " (filtyp \*.JPM), "jpx " (filtyp \*.JPX).

Itererande bitar, tills okänd typ upptäcks, komponerar vi JPEG 2000-bild-/videofil.

### Färgomvandling ###

Inledningsvis krävs omvandling av bilder från RGB-färgrymd till en annan färgrymd. För detta ändamål finns det två sätt: Irreversible Color Transform (ICT) och Reversible Color Transform (RCT). Tidigare använder YC,,B,,C,,R,, färgrymd och måste implementeras i fix/flytande punkt medan senare en modifierad YUV-färgrymd och reversibel till sin natur.// //Inte begränsad till RGB-modell, JPEG 2000-språket använder transformering av flera komponenter.

### Plattläggning ###

När färgomvandlingen är klar omvandlas bilden till rektangulära områden som kallas brickor som kan transformeras och kodas separat. Storleken på alla brickor kommer att ha samma eller hela bilden kan betraktas som en enda bricka. Decoder drar fördelen av kakel och förbrukar mindre minne eller kan delvis koda vissa brickor. Även om denna teknik har en nackdel med kvalitetsförsämring av bilden.

### Wavelet transform ###

Bilden efter plattsättning är wavelet-transformerad som kan vara antingen irreversibel eller reversibel och implementeras genom att använda faltnings- eller lyftschemat.

### Kompressionsförhållande ###

Beroende på de fysiska egenskaperna hos en bild erhålls en komprimeringsvinst på 20 %. Spatial-redundansförutsägelse av JPEG 2000 spelar en avgörande roll i komprimeringsprocessen och högupplösta bilder tenderar att få störst fördel.

## Applikationer som betjänas av standarden ##

* Inspelning, redigering och lagring av rambaserade HD-videor
* Medicinsk bildspråk och biometri
* satellitbilder, fjärranalys och rörelsedetektion
* Klient/serverkommunikation, nätverksdistribution och lagring.
* Digital bio, Live HDTV-flödesbidrag, digitaliserade audiovisuella saker

## Referenser ##

* [Översikt över JPEG 2000](https://jpeg.org/jpeg2000)
* [JPEG 2000 bildkodningssystem](https://en.wikipedia.org/wiki/JPEG_2000#JPEG_2000_image_coding_system_-_Parts)

