{
  "date": "2019-12-12",
  "keywords": [
"GLTF",
"fil",
"udvidelse",
"format",
"3D",
"Khronos Group 3D"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om GLTF-filer og API'er, der kan oprette og åbne GLTF-filer.",
  "title": "GLTF - GL-transmissionsfilformat",
  "linktitle": "GLTF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-glt-daf"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en GLTF fil?

glTF (GL Transmission Format) er et 3D-filformat, der gemmer 3D-modeloplysninger i JSON-format. Brugen af JSON minimerer både størrelsen af 3D-aktiver og den runtime-behandling, der er nødvendig for at udpakke og bruge disse aktiver. Det blev vedtaget til effektiv transmission og indlæsning af 3D-scener og modeller efter applikationer. glTF blev udviklet af Khronos Group 3D Formats Working Group og beskrives også som [JPEG](/image/jpeg/) af 3D af dets skabere.

GLTF-filformatet definerer et udvideligt, almindeligt udgivelsesformat for 3D-indholdsværktøjer og -tjenester, der strømliner forfatterarbejdsgange og muliggør interoperabel brug af indhold på tværs af industrien. Hensigten bag skabelsen af glTF-filformatet var at definere et udvideligt, fælles publiceringsformat for 3D-indholdsværktøjer og -tjenester, der skulle strømline forfatterarbejdsgange og muliggøre interoperabel brug af indhold på tværs af industrien. Det minimerer runtime-behandling af applikationer, der bruger WebGL og andre API'er.

## Kort historie om GLTF-fil

The first specifications for glTF file format 1.0 were announced in October 2015. Dette var kommet som en række indsatser, der startede i marts 2012 af Khronos. Formålet med disse bestræbelser var at vurdere mulighederne omkring WebGL-trækkraften. Resultatet blev, at den første demo af glTF-format, baseret på JSON-formatet, blev præsenteret på WebGl-mødet i 2012. Formatet blev vedtaget af flere virksomheder fra tid til anden, herunder Cesium, 3D Tiles, Oculus, Microsoft, Archilogic og andre.

glTF 2.0 blev offentliggjort den 5. juni 2017 på Web3D 2017-konferencen. Der er en lang liste over virksomheder, der har overtaget glTF-filformatet efter det.

## GLTF filformat

Filformatspecifikationerne for glTF 2.0 er tilgængelige [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) til reference og bør konsulteres i enhver implementering relateret til læsning/skrivning for at understøtte glTF-filformatet.

glTF definerer aktiver som JSON-filer med understøttende eksterne data. Det repræsenterer 3D-modeller ved hjælp af:

* Full scene description contained in a JSON-formatted .glTF file that includes information about node hierarchy, materials, cameras, as well as descriptor information for meshes, animations and other constructs
* Binære filer (.bin) indeholdende geometri- og animationsdata og andre bufferbaserede data

* Billedfiler ([.jpg](/image/jpeg/), [.png](/image/png/)) til teksturer


Alle eksterne aktiver, såsom billeder, gemmes i eksterne filer, der refereres til via URI. Disse URI'er gemmes sammen med GLB-beholderen eller indlejres direkte i JSON'en ved hjælp af data-URI'er. Hver gyldig glTF skal angive sin version.

glTF er designet til at opnå lille filstørrelse, hurtig indlæsning, komplet 3D-scenerepræsentation og udvidelsesmuligheder. Disse unikke designmål er hovedårsagerne til glTF-filformatets popularitet i 3D-domæne. Følgende er de mime-typer, der understøttes af glTF-filformatet for forskellige filtyper:

* .gltf-filer bruger model/gltf+json

* .bin filer bruger application/octet-stream

* Teksturfiler bruger den officielle image/* type baseret på det specifikke billedformat. For kompatibilitet med moderne webbrowsere understøttes følgende billedformater: image/jpeg, image/png.


### JSON-kodning

glTF pålægger følgende yderligere begrænsninger på JSON-filformat

For at forenkle implementering på klientsiden har glTF yderligere begrænsninger for JSON-format og -kodning.

1. JSON skal bruge UTF-8-kodning uden stykliste.
1. Alle strenge defineret i denne spec (egenskabsnavne, enums) bruger kun ASCII-tegnsæt og skal skrives som almindelig tekst, f.eks. buffer i stedet for `\u0062\u0075\u0066\u0066\u0065\u0072`.
1. Navne (nøgler) i JSON-objekter skal være unikke, dvs. duplikerede nøgler er ikke tilladt.

### URI'er

Der henvises til buffere og billedressourcer via URI'er. Følgende to URI-typer skal understøttes af klienterne.

**Data-URI'er:** Data-URI'erne er som defineret af RFC 2397 og bruges af glTF til at integrere ressourcer i JSON.

**Relative URI Paths:** or path-noscheme as defined by RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — without scheme, authority, or parameters. Reserved characters must be percent-encoded, per RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Referencer ##

* [glTF 2.0-specifikationer - Khronos](https://github.com/KhronosGroup/glTF)

* [glTF-filformat - af Wikipedia](https://en.wikipedia.org/wiki/GlTF)


