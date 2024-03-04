{
  "date" : "2019-12-03",
  "keywords" : [ "GLB","file", "format", "file type", "extension","what is an GLB file?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "GLB",
  "description":"Sužinokite apie GLB failo formatą ir API, kurios gali atidaryti ir kurti GLB failus.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb-lt",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Kas yra GLB failas?

GLB yra dvejetainis 3D modelių failo formatas, įrašytas GL perdavimo formatu ([glTF](/3d/gltf/)). Informacija apie 3D modelius, tokius kaip mazgų hierarchija, fotoaparatai, medžiagos, animacijos ir tinkleliai dvejetainiu formatu. Šis dvejetainis formatas saugo glTF išteklius (JSON, .bin ir vaizdus) dvejetainiame bloke. Taip pat išvengiama failo dydžio padidėjimo, kuris atsitinka glTF atveju. GLB failo formatas užtikrina kompaktiškus failų dydžius, greitą įkėlimą, pilną 3D scenos atvaizdavimą ir išplečiamumą tolesniam kūrimui. Formatas naudoja model/gltf-binary kaip MIME tipą.

## GLB failo formatas – daugiau informacijos

Turinio pateikimo metodai, kuriuos naudoja glTF, papildomai apdoroja bazinius 64 koduotus dvejetainius duomenis, taip pat padidina failo dydį 33%. Šie pristatymo būdai, kurie prisidėjo prie GLB failo formato formavimo, apima:

* glTF JSON nurodo išorinius dvejetainius duomenis (geometriją, raktų rėmus, apvalkalus) ir vaizdus.

* „glTF JSON“ įterpia „base64“ koduotus dvejetainius duomenis ir vaizdus, naudojant duomenų URI.


GLB kaip konteinerio formatas buvo pristatytas kaip dvejetainis failo formatas, skirtas glTF ištekliui atvaizduoti dvejetainiame bloke, kad būtų išvengta glTF sukeltų problemų. GLB failo formatas [specifications](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) turėtų būti taikomas bet kokiam skaitytuvui / rašytojui, kuris įgyvendinamas kuriant programas.

## GLB failo struktūra

GLB failo formatas yra pagrįstas little endian ir jo struktūra rodo, kad jame yra:

* 12 baitų preambulė, pavadinta antrašte.

* Vienas ar daugiau dalių, kuriose yra JSON turinio ir dvejetainių duomenų.


#### GLB antraštė

GLB failo formato antraštę sudaro trys 4 baitų įrašai:

* uint32 magic – magija lygu 0x46546C67. Tai ASCII eilutė glTF ir gali būti naudojama duomenims identifikuoti kaip dvejetainį glTF

* uint32 versija – nurodo dvejetainio glTF konteinerio formato versiją

* uin32 ilgis – bendras dvejetainio glTF ilgis, įskaitant antraštę ir visus gabalus baitais


#### Gabalai

Kiekviena GLB failo dalis turi tokią struktūrą:

|uint32|uint32|ubaitas[]
---|---|---|
|chunkLength|chunkType|chunkData

* „chunkLength“ – chunkData ilgis baitais

* `chunkType` – nurodo nurodo gabalo tipą

* `chunkData` – dvejetainė naudingoji gabalo apkrova


kur yra gabalų tipai:

|# |Laiko tipas|ASCII|Aprašymas|Pasireiškimai
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Struktūrinis JSON turinys|1
|2.|0x004E4942|BIN|Dvejetainis buferis|0 arba 1

Kiekvieno gabalo pradžia ir pabaiga turi būti sulygiuotos su 4 baitų riba ir šiuo tikslu turėtų būti naudojamas užpildymas.

##### Struktūrinis JSON turinys

Tai turėtų būti pati pirmoji dvejetainio glTF ištekliaus dalis ir leidžia diegti laipsniškai nuskaityti išteklius iš vėlesnių dalių. Tai taip pat suteikia galimybę nuskaityti tik pasirinktą išteklių poaibį iš dvejetainio glTF išteklių, pvz., stambiausią tinklelio LOD. Kad atitiktų lygiavimo reikalavimus, šis gabalas turi būti paminkštintas tarpo simboliais (0x20).

##### Dvejetainis buferis #####

Šioje dalyje yra dvejetainė geometrijos, animacijos raktų kadrų, apvalkalų ir vaizdų naudingoji apkrova. Tai turėtų būti antrasis dvejetainio glTF ištekliaus gabalas ir turi būti užpildytas galiniais nuliais (0x00), kad atitiktų lygiavimo reikalavimus.

## Nuorodos Nr.

* [GLB failo formato specifikacijos – Khronos](/3d/gltf/)


