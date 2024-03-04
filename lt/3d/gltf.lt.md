{
  "date": "2019-12-12",
  "keywords": [
"GLTF",
"failą",
"pratęsimas",
"formatu",
"3D",
"Khronos grupė 3D"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie GLTF failus ir API, kurios gali kurti ir atidaryti GLTF failus.",
  "title": "GLTF – GL perdavimo failo formatas",
  "linktitle": "GLTF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-glt-ltf"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra GLTF failas?

glTF (GL perdavimo formatas) yra 3D failo formatas, kuriame saugoma 3D modelio informacija JSON formatu. JSON naudojimas sumažina 3D išteklių dydį ir vykdymo laiką, reikalingą tiems ištekliams išpakuoti ir naudoti. Jis buvo pritaikytas efektyviam 3D scenų ir modelių perdavimui ir įkėlimui naudojant programas. glTF sukūrė Khronos Group 3D formatų darbo grupė, o jo kūrėjai taip pat apibūdino kaip [JPEG](/image/jpeg/) iš 3D.

GLTF failo formatas apibrėžia išplečiamą, įprastą 3D turinio įrankių ir paslaugų publikavimo formatą, kuris supaprastina kūrimo darbo eigą ir leidžia sąveikiai naudoti turinį visoje pramonės šakoje. Kuriant glTF failo formatą buvo siekiama apibrėžti išplečiamą bendrą 3D turinio įrankių ir paslaugų publikavimo formatą, kuris turėtų supaprastinti kūrimo darbo eigą ir sudaryti sąlygas sąveikiai naudoti turinį visoje pramonėje. Tai sumažina vykdymo laiką, kai programos naudoja WebGL ir kitas API.

## Trumpa GLTF failo istorija

The first specifications for glTF file format 1.0 were announced in October 2015. Tai buvo daugybė pastangų, kurias 2012 m. kovo mėn. pradėjo Khronos. Šių pastangų tikslas buvo įvertinti WebGL traukos galimybes. 2012 m. WebGl susitikime buvo pristatyta pirmoji JSON formato glTF formato demonstracinė versija. Retkarčiais šį formatą perėmė kelios įmonės, įskaitant Cesium, 3D Tiles, Oculus, Microsoft, Archilogic ir kt.

glTF 2.0 buvo paskelbtas 2017 m. birželio 5 d. Web3D 2017 konferencijoje. Yra ilgas sąrašas įmonių, kurios po to priėmė glTF failo formatą.

## GLTF failo formatas

glTF 2.0 failo formato specifikacijos yra prieinamos [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) ir jas reikia peržiūrėti bet kokio diegimo, susijusio su glTF failo formato palaikymu, skaitymu / rašymu.

glTF apibrėžia išteklius kaip JSON failus su išoriniais duomenimis. Jis vaizduoja 3D modelius naudojant:

* Full scene description contained in a JSON-formatted .glTF file that includes information about node hierarchy, materials, cameras, as well as descriptor information for meshes, animations and other constructs
* Dvejetainiai failai (.bin), kuriuose yra geometrijos ir animacijos duomenų bei kiti buferio duomenys

* Vaizdo failai ([.jpg](/image/jpeg/), [.png](/image/png/)) tekstūroms


Bet koks išorinis turtas, pvz., vaizdai, saugomas išoriniuose failuose, kurie nurodomi per URI. Šie URI saugomi kartu su GLB sudėtiniu rodiniu arba įterpiami tiesiai į JSON naudojant duomenų URI. Kiekvienas galiojantis glTF turi nurodyti savo versiją.

glTF buvo sukurta taip, kad būtų pasiektas mažas failo dydis, greitas įkėlimas, pilnas 3D scenos atvaizdavimas ir išplečiamumas. Šie unikalūs dizaino tikslai yra pagrindinės glTF failo formato populiarumo 3D srityje priežastys. Toliau pateikiami mime tipai, kuriuos palaiko glTF failo formatas skirtingiems failų tipams:

* .gltf failuose naudojamas modelis/gltf+json

* .bin failai naudoja programą / octet-stream

* Tekstūros failuose naudojamas oficialus vaizdo/* tipas pagal konkretų vaizdo formatą. Siekiant suderinamumo su šiuolaikinėmis interneto naršyklėmis, palaikomi šie vaizdo formatai: image/jpeg, image/png.


### JSON kodavimas

glTF nustato šiuos papildomus JSON failo formato apribojimus

Siekiant supaprastinti diegimą kliento pusėje, glTF taikomi papildomi JSON formato ir kodavimo apribojimai.

1. JSON turi naudoti UTF-8 kodavimą be MK.
1. Visos šiose specifikacijose apibrėžtos eilutės (ypatybių pavadinimai, sąrašai) naudoja tik ASCII simbolių rinkinį ir turi būti parašytos kaip paprastas tekstas, pvz., buferis, o ne `\u0062\u0075\u0066\u0066\u0065\u0072`.
1. JSON objektų pavadinimai (raktai) turi būti unikalūs, ty raktų kopijos neleidžiamos.

### URI

Buferiai ir vaizdo ištekliai nurodomi per URI. Klientai turi palaikyti šiuos du URI tipus.

**Duomenų URI:** Duomenų URI apibrėžti RFC 2397 ir juos naudoja glTF, kad įterptų išteklius į JSON.

**Relative URI Paths:** or path-noscheme as defined by RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — without scheme, authority, or parameters. Reserved characters must be percent-encoded, per RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## Nuorodos Nr.

* [glTF 2.0 specifikacijos – „Khronos“](https://github.com/KhronosGroup/glTF)

* [glTF failo formatas – pagal Vikipediją](https://en.wikipedia.org/wiki/GlTF)


