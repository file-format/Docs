{
  "date" : "2019-10-11",
  "keywords" :[ "amf", "amf-fil", "amf-filformat", "filformat", "3d"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om AMF-filformat och API:er som kan öppna och skapa AMF-filer.",
  "title" :"AMF - Additive Manufacturing File",
  "linktitle" : "AMF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är AMF fil?
En AMF-fil består av riktlinjer för objektbeskrivning för att kunna användas av Additive Manufacturing processer. Den innehåller en öppning<amf> XML-tagg och slutar med en</amf> element. Detta föregås av en XML-deklarationsrad som anger XML-versionen och kodningen för filen. Deklarationerna kan innehålla information om måttenheter och i avsaknad av sådan information används millimeter som standardenhet.


## AMF filformat

Additive Manufacturing filformat (**AMF**) definierar öppna standarder för objektbeskrivningar för att kunna användas av additiv tillverkningsprocesser som 3D-utskrift. CAD-program använder AMF-filformatet genom att använda information som geometri, färg och material för objekten. AMF skiljer sig från STL-format eftersom lateralen inte stöder färg, material, gitter och konstellationer.

### Element i en AMF-fil

De fem toppnivåelementen definierade med<AMF> taggar är enligt beskrivningen nedan. Förekomsten av ett enda objektelement är ett måste för en fullt fungerande AMF-fil.

`<object> ` - Objektelementet definierar en eller flera volymer av material, som var och en är associerad med ett material-ID för utskrift. Minst ett objektelement måste finnas i filen. Ytterligare objekt är valfria.

`<material> ` - Det valfria materialelementet definierar ett eller flera material för utskrift med ett tillhörande material-ID. Om inget materialelement ingår antas ett enda standardmaterial.

`<texture> ` - Det valfria texturelementet definierar en eller flera bilder eller texturer för färg- eller texturmappning, var och en med tillhörande textur-ID.

`<constellation> ` - Det valfria konstellationselementet kombinerar objekt och andra konstellationer hierarkiskt till ett relativt mönster för utskrift.

`<metadata> ` - Det valfria metadataelementet specificerar ytterligare information om objektet/objekten och elementen som finns i filen.

## Exempel på AMF

Följande är ett exempel på AMF-fil som kan kopieras till en [text](/sv/ordbehandling/txt/)-fil och sparas som en komprimerad [zip](/sv/compression/zip/)-fil för öppning.
```
<?xml version="1.0" encoding="utf-8"?>
<amf unit="inch" version="1.1">
  <metadata type="name">Split Pyramid</metadata>
  <metadata type="author">John Smith</metadata>
  <object id="1">
    <mesh>
      <vertices>
        <vertex><coordinates><x>0</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>0</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>1</x><y>1</y><z>0</z></coordinates></vertex>
        <vertex><coordinates><x>0.5</x><y>0.5</y><z>1</z></coordinates></vertex>
      </vertices>
      <volume materialid="2">
        <metadata type="name">Hard side</metadata>
        <triangle><v1>2</v1><v2>1</v2><v3>0</v3></triangle>
        <triangle><v1>0</v1><v2>1</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>1</v2><v3>2</v3></triangle>
        <triangle><v1>0</v1><v2>4</v2><v3>2</v3></triangle>
      </volume>
      <volume materialid="3">
        <metadata type="name">Soft side</metadata>
        <triangle><v1>2</v1><v2>3</v2><v3>1</v3></triangle>
        <triangle><v1>1</v1><v2>3</v2><v3>4</v3></triangle>
        <triangle><v1>4</v1><v2>3</v2><v3>2</v3></triangle>
        <triangle><v1>4</v1><v2>2</v2><v3>1</v3></triangle>
      </volume>
    </mesh>
  </object>
  <material id="2">
    <metadata type="name">Hard material</metadata>
    <color><r>0.1</r><g>0.1</g><b>0.1</b></color>
  </material>
  <material id="3">
    <metadata type="name">Soft material</metadata>
    <color><r>0</r><g>0.9</g><b>0.9</b><a>0.5</a></color>
  </material>
</amf>
```
## Referenser

* [AMF - Wikipedia](https://en.wikipedia.org/wiki/Additive_manufacturing_file_format)
* [AMF-specifikationer för ISO](https://www.iso.org/standard/67472.html)

