{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "soubor", "přípona", "formát", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o souborech GLTF a rozhraních API, která mohou vytvářet a otevírat soubory GLTF.",
  "title" :"GLTF - Formát souboru přenosu GL",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor GLTF?

glTF (GL Transmission Format) je formát 3D souboru, který ukládá informace o 3D modelu ve formátu JSON. Použití JSON minimalizuje jak velikost 3D aktiv, tak běhové zpracování potřebné k rozbalení a použití těchto aktiv. Byl přijat pro efektivní přenos a načítání 3D scén a modelů aplikacemi. glTF byl vyvinut Khronos Group 3D Formats Working Group a jeho tvůrci jej také popisují jako [JPEG](/cs/image/jpeg/) 3D.

Formát souboru GLTF definuje rozšiřitelný, běžný formát publikování pro nástroje a služby 3D obsahu, který zjednodušuje pracovní postupy tvorby a umožňuje interoperabilní použití obsahu v celém odvětví. Záměrem za vytvořením formátu souboru glTF bylo definovat rozšiřitelný, společný publikační formát pro nástroje a služby 3D obsahu, který by měl zjednodušit pracovní postupy tvorby a umožnit interoperabilní používání obsahu v celém odvětví. Minimalizuje zpracování za běhu aplikacemi používajícími WebGL a další API.

## Stručná historie souboru GLTF

První specifikace pro formát souboru glTF 1.0 byly oznámeny v říjnu 2015. Přišlo to jako série snah, které v březnu 2012 zahájila společnost Khronos. Cílem těchto snah bylo posoudit příležitosti kolem trakce WebGL. V důsledku toho bylo na setkání WebGl v roce 2012 představeno první demo formátu glTF založeného na formátu JSON. Formát čas od času přijalo několik společností včetně Cesium, 3D Tiles, Oculus, Microsoft, Archilogic a dalších.

glTF 2.0 byl publikován 5. června 2017 na konferenci Web3D 2017. Existuje dlouhý seznam společností, které poté přijaly formát souboru glTF.

## Formát souboru GLTF

Specifikace formátu souboru pro glTF 2.0 jsou k dispozici [online](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) pro referenci a měly by být konzultovány při jakékoli implementaci související se čtením/zápisem pro podporu formát souboru glTF.

glTF definuje aktiva jako soubory JSON s podporou externích dat. Představuje 3D modely pomocí:

* Úplný popis scény obsažený v souboru .glTF ve formátu JSON, který obsahuje informace o hierarchii uzlů, materiálech, kamerách a také informace o deskriptorech sítí, animací a dalších konstrukcí.
* Binární soubory (.bin) obsahující data geometrie a animace a další data založená na vyrovnávací paměti
* Soubory obrázků ([.jpg](/cs/image/jpeg/), [.png](/cs/image/png/)) pro textury

Jakékoli externí zdroje, jako jsou obrázky, jsou uloženy v externích souborech, na které se odkazuje prostřednictvím URI. Tyto URI jsou uloženy vedle kontejneru GLB nebo vloženy přímo do JSON pomocí datových URI. Každý platný glTF musí specifikovat jeho verzi.

glTF byl navržen pro dosažení malé velikosti souboru, rychlého načítání, kompletní reprezentace 3D scény a rozšiřitelnosti. Tyto jedinečné designové cíle jsou hlavními důvody popularity formátu glTF ve 3D doméně. Níže jsou uvedeny typy mime podporované formátem souboru glTF pro různé typy souborů:

* Soubory .gltf používají model/gltf+json
* Soubory .bin používají application/octet-stream
* Soubory textur používají oficiální typ obrázku/* na základě konkrétního formátu obrázku. Pro kompatibilitu s moderními webovými prohlížeči jsou podporovány následující formáty obrázků: image/jpeg, image/png.

### Kódování JSON

glTF ukládá následující další omezení pro formát souboru JSON

Pro zjednodušení implementace na straně klienta má glTF další omezení formátu JSON a kódování.

1. JSON musí používat kódování UTF-8 bez kusovníku.
1. Všechny řetězce definované v této specifikaci (názvy vlastností, výčty) používají pouze znakovou sadu ASCII a musí být zapsány jako prostý text, např. "buffer" místo `"\u0062\u0075\u0066\u0066\u0065\u0072"`.
1. Názvy (klíče) v objektech JSON musí být jedinečné, tj. duplicitní klíče nejsou povoleny.

### URI

Vyrovnávací paměti a zdroje obrázků jsou odkazovány pomocí URI. Klienti musí podporovat následující dva typy URI.

**URI dat:** Identifikátory URI dat jsou definovány v RFC 2397 a používá je glTF k vkládání zdrojů do JSON.

**Relativní cesty URI:** nebo schéma cesty, jak je definováno v RFC 3986, [část 4.2] (https://tools.ietf.org/html/rfc3986#section-4.2) – bez schématu, oprávnění nebo parametrů. Vyhrazené znaky musí být zakódovány v procentech podle RFC 3986, [sekce 2.2] (https://tools.ietf.org/html/rfc3986#section-2.2).

## Reference ##

* [glTF 2.0 Specifikace – Khronos](https://github.com/KhronosGroup/glTF)
* [Formát souboru glTF – podle Wikipedie](https://en.wikipedia.org/wiki/GlTF)

