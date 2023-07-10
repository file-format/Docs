{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "fil", "tillägg", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om GLTF-filer och API:er som kan skapa och öppna GLTF-filer.",
  "title" :"GLTF - GL Transmission File Format",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är GLTF fil?

glTF (GL Transmission Format) är ett 3D-filformat som lagrar 3D-modellinformation i JSON-format. Användningen av JSON minimerar både storleken på 3D-tillgångar och den körtidsbearbetning som krävs för att packa upp och använda dessa tillgångar. Det antogs för effektiv överföring och laddning av 3D-scener och modeller av applikationer. glTF utvecklades av Khronos Group 3D Formats Working Group och beskrivs också som [JPEG](/sv/image/jpeg/) av 3D av dess skapare.

GLTF-filformatet definierar ett utbyggbart, vanligt publiceringsformat för 3D-innehållsverktyg och tjänster som effektiviserar författararbetsflöden och möjliggör interoperabel användning av innehåll i hela branschen. Avsikten bakom skapandet av glTF-filformatet var att definiera ett utbyggbart, vanligt publiceringsformat för 3D-innehållsverktyg och tjänster som skulle effektivisera författararbetsflöden och möjliggöra interoperabel användning av innehåll i branschen. Det minimerar körtidsbearbetning av applikationer som använder WebGL och andra API:er.

## Kort historik om GLTF-fil

De första specifikationerna för glTF-filformat 1.0 tillkännagavs i oktober 2015. Detta hade kommit som en serie insatser som startade i mars 2012 av Khronos. Syftet med dessa ansträngningar var att bedöma möjligheterna kring WebGL-dragkraften. Resultatet blev att den första demon av glTF-formatet, baserat på JSON-formatet, presenterades vid WebGl-mötet 2012. Formatet antogs av flera företag då och då, inklusive Cesium, 3D Tiles, Oculus, Microsoft, Archilogic och andra.

glTF 2.0 publicerades den 5 juni 2017 på Web3D 2017-konferensen. Det finns en lång lista med företag som anammat filformatet glTF efter det.

## GLTF filformat

Filformatspecifikationerna för glTF 2.0 är tillgängliga [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) för referens och bör konsulteras i alla implementeringar som är relaterade till läsning/skrivande för stöd för glTF filformat.

glTF definierar tillgångar som JSON-filer med stödjande externa data. Den representerar 3D-modeller med hjälp av:

* Fullständig scenbeskrivning i en JSON-formaterad .glTF-fil som innehåller information om nodhierarki, material, kameror samt deskriptorinformation för maskor, animationer och andra konstruktioner
* Binära filer (.bin) som innehåller geometri- och animationsdata och andra buffertbaserade data
* Bildfiler ([.jpg](/sv/image/jpeg/), [.png](/sv/image/png/)) för texturer

Alla externa tillgångar som bilder lagras i externa filer som refereras via URI. Dessa URI:er lagras bredvid GLB-behållaren eller bäddas in direkt i JSON:er med hjälp av data-URI:er. Varje giltig glTF måste ange sin version.

glTF har utformats för att uppnå liten filstorlek, snabb laddning, komplett 3D-scenerepresentation och utökningsbarhet. Dessa unika designmål är huvudorsakerna till glTF-filformatets popularitet i 3D-domän. Följande är de mimetyper som stöds av filformatet glTF för olika filtyper:

* .gltf-filer använder model/gltf+json
* .bin-filer använder application/octet-stream
* Texturfiler använder den officiella bilden/*-typen baserat på det specifika bildformatet. För kompatibilitet med moderna webbläsare stöds följande bildformat: image/jpeg, image/png.

### JSON-kodning

glTF inför följande ytterligare begränsningar för JSON-filformat

För att förenkla implementeringen på klientsidan har glTF ytterligare begränsningar för JSON-format och kodning.

1. JSON måste använda UTF-8-kodning utan BOM.
1. Alla strängar som definieras i denna spec (egenskapsnamn, enums) använder endast ASCII-teckenuppsättning och måste skrivas som vanlig text, t.ex. "buffert" istället för `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Namn (nycklar) i JSON-objekt måste vara unika, dvs dubbletter av nycklar är inte tillåtna.

### URI:er

Buffertar och bildresurser refereras via URI:er. Följande två URI-typer måste stödjas av klienterna.

**Data-URI:** Data-URI:er är enligt definitionen av RFC 2397 och används av glTF för att bädda in resurser i JSON.

**Relativ URI-sökväg:** eller path-noscheme enligt definitionen i RFC 3986, [avsnitt 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — utan schema, auktoritet eller parametrar. Reserverade tecken måste vara procentkodade enligt RFC 3986, [avsnitt 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Referenser ##

* [glTF 2.0-specifikationer - Khronos](https://github.com/KhronosGroup/glTF)
* [glTF-filformat - av Wikipedia](https://en.wikipedia.org/wiki/GlTF)

