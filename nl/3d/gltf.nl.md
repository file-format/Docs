{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "bestand", "extensie", "format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over GLTF-bestanden en API's die GLTF-bestanden kunnen maken en openen.",
  "title" :"GLTF - GL-verzendingsbestandsformaat",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Wat is een GLTF-bestand?

glTF (GL Transmission Format) is een 3D-bestandsindeling die 3D-modelinformatie opslaat in JSON-indeling. Het gebruik van JSON minimaliseert zowel de grootte van 3D-assets als de runtime-verwerking die nodig is om die assets uit te pakken en te gebruiken. Het werd gebruikt voor het efficiënt verzenden en laden van 3D-scènes en -modellen door applicaties. glTF is ontwikkeld door de Khronos Group 3D Formats Working Group en wordt door de makers ook beschreven als [JPEG](/nl/image/jpeg/) van 3D.

Het GLTF-bestandsformaat definieert een uitbreidbaar, algemeen publicatieformaat voor 3D-contenttools en -services die de authoringworkflows stroomlijnen en interoperabel gebruik van content in de hele branche mogelijk maken. De bedoeling achter de creatie van het glTF-bestandsformaat was om een uitbreidbaar, algemeen publicatieformaat te definiëren voor 3D-contenttools en -services die de authoringworkflows moeten stroomlijnen en interoperabel gebruik van content in de hele sector mogelijk moeten maken. Het minimaliseert runtime-verwerking door applicaties die WebGL en andere API's gebruiken.

## Korte geschiedenis van het GLTF-bestand

De eerste specificaties voor glTF-bestandsformaat 1.0 werden aangekondigd in oktober 2015. Dit was een reeks inspanningen die in maart 2012 door Khronos begonnen waren. Het doel van deze inspanningen was om de kansen rond de WebGL-tractie te beoordelen. Het resultaat was dat de eerste demo van het glTF-formaat, gebaseerd op het JSON-formaat, werd gepresenteerd tijdens de WebGl-bijeenkomst in 2012. Het formaat werd van tijd tot tijd door verschillende bedrijven overgenomen, waaronder Cesium, 3D Tiles, Oculus, Microsoft, Archilogic en anderen.

glTF 2.0 werd op 5 juni 2017 gepubliceerd op de Web3D 2017 Conference. Er is een lange lijst van bedrijven die daarna het glTF-bestandsformaat hebben overgenomen.

## GLTF-bestandsindeling

De specificaties van het bestandsformaat voor glTF 2.0 zijn beschikbaar [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) ter referentie en moeten worden geraadpleegd in elke implementatie met betrekking tot lezen/schrijven voor ondersteuning van glTF-bestandsindeling.

glTF definieert activa als JSON-bestanden met ondersteunende externe gegevens. Het vertegenwoordigt 3D-modellen met behulp van:

* Volledige scènebeschrijving in een JSON-geformatteerd .glTF-bestand dat informatie bevat over knooppunthiërarchie, materialen, camera's, evenals descriptorinformatie voor meshes, animaties en andere constructies
* Binaire bestanden (.bin) met geometrie- en animatiegegevens en andere op buffers gebaseerde gegevens
* Afbeeldingsbestanden ([.jpg](/nl/image/jpeg/), [.png](/nl/image/png/)) voor texturen

Alle externe middelen zoals afbeeldingen worden opgeslagen in externe bestanden waarnaar wordt verwezen via URI. Deze URI's worden naast de GLB-container opgeslagen of rechtstreeks in de JSON ingesloten met behulp van gegevens-URI's. Elke geldige glTF moet zijn versie specificeren.

glTF is ontworpen om een kleine bestandsgrootte, snel laden, volledige 3D-scèneweergave en uitbreidbaarheid te bereiken. Deze unieke ontwerpdoelen zijn de belangrijkste redenen voor de populariteit van het glTF-bestandsformaat in het 3D-domein. Hieronder volgen de mime-typen die worden ondersteund door het glTF-bestandsformaat voor verschillende bestandstypen:

* .gltf-bestanden gebruiken model/gltf+json
* .bin-bestanden gebruiken application/octet-stream
* Textuurbestanden gebruiken het officiële type afbeelding/* op basis van het specifieke afbeeldingsformaat. Voor compatibiliteit met moderne webbrowsers worden de volgende afbeeldingsindelingen ondersteund: afbeelding/jpeg, afbeelding/png.

### JSON-codering

glTF legt de volgende aanvullende beperkingen op aan het JSON-bestandsformaat:

Om de implementatie aan de clientzijde te vereenvoudigen, heeft glTF aanvullende beperkingen op het JSON-formaat en de codering.

1. JSON moet UTF-8-codering gebruiken zonder stuklijst.
1. Alle tekenreeksen die in deze specificatie zijn gedefinieerd (eigenschapsnamen, opsommingen) gebruiken alleen ASCII-tekensets en moeten als platte tekst worden geschreven, bijv. "buffer" in plaats van `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Namen (sleutels) binnen JSON-objecten moeten uniek zijn, dwz dubbele sleutels zijn niet toegestaan.

### URI's

Er wordt verwezen naar buffers en afbeeldingsbronnen via URI's. De volgende twee URI-typen moeten door de clients worden ondersteund.

**Gegevens-URI's:** De gegevens-URI's zijn zoals gedefinieerd door de RFC 2397 en worden door glTF gebruikt om bronnen in de JSON in te sluiten.

**Relatieve URI-paden:** of path-noscheme zoals gedefinieerd door RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — zonder schema, autoriteit of parameters. Gereserveerde tekens moeten procentgecodeerd zijn, volgens RFC 3986, [Sectie 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Referenties ##

* [glTF 2.0-specificaties - Khronos](https://github.com/KhronosGroup/glTF)
* [glTF-bestandsindeling - door Wikipedia](https://en.wikipedia.org/wiki/GlTF)

