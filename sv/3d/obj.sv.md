{
  "date" : "2019-10-11",
  "keywords" :[ "obj fil", "obj filformat", "vad är en obj fil", "fil", "obj exempel", "obj filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBJ-filformat",
  "description":"Läs mer om OBJ-filformat och API:er som kan öppna och skapa OBJ-filer.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en OBJ-fil?

**OBJ**-filer används av Wavefronts Advanced Visualizer-applikation för att definiera och lagra de geometriska objekten. Bakåt- och framåtöverföring av geometriska data är möjlig genom OBJ-filer. Både polygonal geometri som punkter, linjer, texturhörn, ytor och friformsgeometri (kurvor och ytor) stöds av OBJ-format. Det här formatet stöder inte animering eller information relaterad till ljus och placering av scener.

En OBJ-fil är vanligtvis en slutprodukt av 3D-modelleringsprocessen som genereras av en CAD (Computer Aided Design). Standardordningen för att lagra hörn är moturs för att undvika explicit deklaration av ansiktsnormaler. Även om OBJ-filer deklarerar skalinformation i en kommentarsrad, har inga enheter deklarerats för OBJ-koordinater.

## Historia av 3D OBJ-format

Wavefront Technologies skapade OBJ-filformat för sin Advanced Visualizer-applikation för att lagra geometriska objekt och 3D-data. Dess version 2.11 ersätts av en nyligen dokumenterad version 3. Filformatet är öppet och har implementerats av andra leverantörer för deras 3D-grafikapplikation. Wavefront Technologies höll detta filformat öppen källkod och neutral.

## OBJ filformat

I 3D-objekt är kodning av ytgeometrin ett utmanande jobb som OBJ-filformatet klarade mycket väl. Detta format är ganska mångsidigt eftersom det erbjuder ett antal val för att koda ytgeometri. Följande är tre tillåtna format med sina egna fördelar och brister:

### Tessellation med polygonala ansikten

OBJ-filformatet underlättar för användaren att tessellate en 3D-modellyta med enkla eller komplexa geometriska former. För ytgeometrikodning av en modell lagrar en fil hörnen och normalen till varje polygon. Även om tessellering ökar modellens grovhet, är det ändå nödvändigt att upptäcka den korrekta balansen mellan storleken på en fil och dess utskriftskvalitet.

### Friformskurva

OBJ-filformatet tillåter användardefinierade fria ytkurvor att specificera ytgeometrin för en modell. Eftersom friformskurvor är mer komplexa än polygonala ytor eftersom, med få matematiska parametrar, krökta linjer bäst kan definieras av friformskurvor. Därför, med färre data jämfört med polygonala tesselleringar, används friformskurvor för att generera en högkvalitativ kodning av vilken 3D-modell som helst utan att utöka filstorleken.

### Ytor i fri form

OBJ-filformatet anger också plattsättningen av ytgeometrin med ytfläckar i fri form. Den här typen av friformade ytlappar (NURBS) är mycket lämpliga för ytor utan stela radiella dimensioner som karossen på en lastbil, helikopterns vingar eller skrovet på en båt. Användning av friformsytor är mycket fördelaktigt eftersom de är mer exakta för att hålla filstorlekarna mindre med högre precision. Dessa ytor är en väsentlig del av flyg- och bilindustrin där den låga precisionen är oförlåtlig.

Följande nyckelord är ordnade efter datatyp för att definiera ytgeometri.


|Element|Friformskurva/ytkroppsangivelser|Friformskurva/ytattribut
---|---|---|
|p|Point|parm|Parametervärden|deg|Grad
|l|Linje|trim|Ytre trimningsögla|bmat|Basmatris
|f|Ansikte|hål|Inre trimningsögla|steg|Stegstorlek
|kurv|Kurva|scrv|Specialkurva|cstyp|Kurva eller yttyp
|curv2|2D curve|sp|Specialpunkt|**Anslutning och gruppering av ytor**
|surf|Surface|end|Slutsats|con|connect
|**Visa/rendera attribut**|g|Gruppnamn
|fasning|fasningsinterpolation|shadow_obj|skugggjutning|s|utjämnande grupp
|lod|Detaljnivå|trace_obj|Ray tracing|mg|Sammanslagningsgrupp
|d_interp|Lös upp interpolation|ctech|Kurvapproximationsteknik|o|Objektnamn
|c_interp|Färginterpolation|stech|Ytapproximationsteknik|
|usemtl|Materialnamn|mtllib|Materialbibliotek|
|**Geometriska hörn**|
|v|Geometriska hörn|vn|Vertexnormaler|
|vt|Texturvertices|vp|Parameterrymdsvertices|

### Färg och struktur

OBJ-fil låter färg- och texturinformation lagras i ett tillhörande filformat som kallas Material Template Library (MTL). Flerfärgade geometriska modeller återges med dessa två filer tillsammans. MTL-filer är ASCII-baserade och underlättar datorrendering genom att beskriva ljusreflekterande egenskaper hos en yta med hjälp av modellen för Phong-reflektion. Standarden har antagits av ett stort antal mjukvaruleverantörer som utnyttjar sin fördel för utbyte av material. MTL-formatet är något föråldrat eftersom det inte har stöd för den senaste tekniken som spegel- och parallaxkartor.

## Referenser

* [Wavefront .obj-fil](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

