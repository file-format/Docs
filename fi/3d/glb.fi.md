{
  "date" : "2019-12-03",
  "keywords" : [ "GLB","file", "format", "file type", "extension","what is an GLB file?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "GLB",
  "description":"Opi GLB-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda GLB-tiedostoja.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb-fi",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Mikä on GLB-tiedosto?

GLB on GL-lähetysmuotoon ([glTF](/3d/gltf/)) tallennettujen 3D-mallien binääritiedostomuoto. Tietoja 3D-malleista, kuten solmuhierarkiasta, kameroista, materiaaleista, animaatioista ja meshistä binäärimuodossa. Tämä binaarimuoto tallentaa glTF-resurssin (JSON, .bin ja kuvat) binääriblobiin. Sillä vältetään myös tiedostokoon kasvu, joka tapahtuu glTF:n tapauksessa. GLB-tiedostomuoto mahdollistaa kompaktin tiedostokoon, nopean latauksen, täydellisen 3D-näkymän esityksen ja laajennettavuuden jatkokehitystä varten. Muoto käyttää malli/gltf-binaaria MIME-tyyppinä.

## GLB-tiedostomuoto – lisätietoja

glTF:n käyttämät sisällön toimitustavat johtavat ylimääräiseen käsittelyyn base-64-koodatun binaaridatan dekoodaamiseen ja lisäävät myös tiedostokokoa 33 %. Nämä toimitustavat, jotka vaikuttivat GLB-tiedostomuodon muodostumiseen, ovat:

* glTF JSON osoittaa ulkoisiin binääritietoihin (geometria, avainkehykset, skinit) ja kuviin.

* glTF JSON upottaa base64-koodattua binaaridataa ja kuvia upotettuna data-URI:iden avulla.


GLB säilömuotona otettiin käyttöön binääritiedostomuotona glTF-resurssin esittämiseksi binääriblobissa glTF:n aiheuttamien ongelmien välttämiseksi. GLB-tiedostomuotoa [specifications](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) tulee käyttää kaikissa saman lukija-/kirjoitusohjelmissa sovellusten kehittämisessä.

## GLB-tiedostorakenne

GLB-tiedostomuoto perustuu little endianiin ja sen rakenne osoittaa, että se sisältää:

* 12-tavuinen johdanto, jonka otsikko on otsikko.

* Yksi tai useampi palo, joka sisältää JSON-sisältöä ja binaaridataa.


#### GLB-otsikko

GLB-tiedostomuodon otsikko koostuu kolmesta 4-tavuisesta merkinnästä:

* uint32 magic - magic on 0x46546C67. Se on ASCII-merkkijono glTF, ja sitä voidaan käyttää tietojen tunnistamiseen binaariseksi glTF:ksi

* uint32-versio - osoittaa binaarisen glTF-säilömuodon version

* uin32 pituus - binaarisen glTF:n kokonaispituus, mukaan lukien otsikko ja kaikki palat tavuina


#### Palat

Jokaisella GLB-tiedoston palalla on seuraava rakenne:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* "chunkLength" - chunkDatan pituus tavuina

* `chunkType` - osoittaa osoittaa kappaleen tyypin

* "chunkData" - kappaleen binaarinen hyötykuorma


missä palatyypit ovat:

|# |Osatyyppi|ASCII|Kuvaus|Esiintymät
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Strukturoitu JSON-sisältö|1
|2.|0x004E4942|BIN|Binaaripuskuri|0 tai 1

Kunkin palan alku ja loppu on kohdistettava 4-tavun rajaan, ja täyttöä tulee käyttää tähän tarkoitukseen.

##### Strukturoitu JSON-sisältö

Tämän pitäisi olla binaarisen glTF-resurssin ensimmäinen osa, ja sen avulla toteutus voi asteittain noutaa resursseja myöhemmistä osista. Tämä tarjoaa myös mahdollisuuden lukea vain valittu resurssien osajoukko binaarisesta glTF-omaisuudesta, kuten verkon karkein LOD. Tasausvaatimusten täyttämiseksi tämä pala on täytettävä perässä olevilla välilyönneillä (0x20).

##### Binääripuskuri #####

Tämä osa sisältää geometrian, animaation avainkehysten, skinien ja kuvien binaarisen hyötykuorman. Sen pitäisi olla binaarisen glTF-sisällön toinen osa, ja sen tulee olla täytetty loppuun nolilla (0x00), jotta tasausvaatimukset täyttyvät.

## Viitteet ##

* [GLB-tiedostomuodon tekniset tiedot – Khronos](/3d/gltf/)


