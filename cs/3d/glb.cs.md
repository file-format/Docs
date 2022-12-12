{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","soubor", "formát", "typ souboru", "přípona","co je soubor GLB?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Další informace o formátu souborů GLB a rozhraních API, která mohou otevírat a vytvářet soubory GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Co je soubor GLB?

GLB je binární reprezentace 3D modelů uložených ve formátu GL Transmission Format ([glTF](/cs/3d/gltf/)). Informace o 3D modelech, jako je hierarchie uzlů, kamery, materiály, animace a sítě v binárním formátu. Tento binární formát ukládá aktivum glTF (JSON, .bin a obrázky) v binárním blobu. Také se vyhne problému zvětšení velikosti souboru, ke kterému dochází v případě glTF. Formát souboru GLB má za následek kompaktní velikosti souborů, rychlé načítání, kompletní reprezentaci 3D scény a rozšiřitelnost pro další vývoj. Formát používá model/gltf-binary jako typ MIME.

## Formát souboru GLB – Další informace

Metody doručování obsahu používané glTF mají za následek dodatečné zpracování pro dekódování binárních dat kódovaných base-64 a také zvětšují velikost souboru o 33 %. Tyto způsoby doručení, které přispěly k vytvoření formátu souboru GLB, zahrnují:

* glTF JSON ukazuje na externí binární data (geometrie, klíčové snímky, vzhledy) a obrázky.
* glTF JSON vkládá binární data zakódovaná v base64 a obrázky inline pomocí datových URI.

GLB jako kontejnerový formát byl představen jako binární formát souboru pro reprezentaci aktiva glTF v binárním blobu, aby se předešlo problémům způsobeným glTF. Formát souboru GLB [specifikace](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification) by měl být uveden pro jakoukoli jeho implementaci pro čtení/zápis pro vývoj aplikací .

## Struktura souborů GLB

Formát souboru GLB je založen na little endian a jeho struktura ukazuje, že obsahuje:

* 12bajtová preambule s názvem záhlaví.
* Jeden nebo více bloků, které obsahují obsah JSON a binární data.

#### Záhlaví GLB

Záhlaví formátu souboru GLB se skládá ze tří 4bajtových položek:

* magie uint32 - magie se rovná 0x46546C67. Je to řetězec ASCII glTF a lze jej použít k identifikaci dat jako binární glTF
* Verze uint32 – označuje verzi formátu kontejneru Binary glTF
* délka uin32 – celková délka binárního glTF, včetně záhlaví a všech částí v bajtech

#### Kousky

Každý blok v souboru GLB má následující strukturu:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - délka chunkData v bajtech
* `chunkType` - označuje typ bloku
* `chunkData` - binární užitečné zatížení bloku

kde jsou typy bloků:

|# |Typ kusu|ASCII|Popis|Výskyty
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Strukturovaný obsah JSON|1
|2.|0x004E4942|BIN|Binární vyrovnávací paměť|0 nebo 1

Začátek a konec každého bloku musí být zarovnány se 4bajtovou hranicí a pro tento účel by se mělo použít odsazení.

##### Strukturovaný obsah JSON

Toto by měl být úplně první díl binárního aktiva glTF a umožňuje implementaci postupně získávat zdroje z následujících částí. To také poskytuje možnost číst pouze vybranou podmnožinu zdrojů z binárního aktiva glTF, jako je nejhrubší LOD sítě. Aby byly splněny požadavky na zarovnání, musí být tento blok doplněn o koncové mezerníky (0x20).

##### Binární vyrovnávací paměť #####

Tento blok obsahuje binární užitečné zatížení pro geometrii, klíčové snímky animace, vzhledy a obrázky. Měl by to být druhý díl binárního aktiva glTF a musí být doplněn koncovými nulami (0x00), aby byly splněny požadavky na zarovnání.

## Reference ##

* [Specifikace formátu souboru GLB – Khronos](/cs/3D/GLTF/)

