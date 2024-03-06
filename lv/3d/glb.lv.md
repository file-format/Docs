{
  "date" : "2019-12-03",
  "keywords" : [ "GLB","file", "format", "file type", "extension","what is an GLB file?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "GLB",
  "description":"Uzziniet par GLB failu formātu un API, kas var atvērt un izveidot GLB failus.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb-lv",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Kas ir GLB fails?

GLB ir 3D modeļu binārā faila formāta attēlojums, kas saglabāts GL pārraides formātā ([glTF](/3d/gltf/)). Informācija par 3D modeļiem, piemēram, mezglu hierarhiju, kamerām, materiāliem, animācijām un tīkliem binārā formātā. Šis binārais formāts saglabā glTF īpašumu (JSON, .bin un attēlus) binārā blobā. Tas arī novērš faila lieluma palielināšanos, kas notiek glTF gadījumā. GLB faila formāts nodrošina kompaktus failu izmērus, ātru ielādi, pilnīgu 3D ainas attēlojumu un paplašināmību turpmākai attīstībai. Formāts izmanto model/gltf-binary kā MIME veidu.

## GLB faila formāts — vairāk informācijas

Satura piegādes metodes, ko izmanto glTF, rada papildu apstrādi, lai atšifrētu bāzes 64 kodētos bināros datus, kā arī palielina faila lielumu par 33%. Šīs piegādes metodes, kas veicināja GLB faila formāta veidošanos, ietver:

* glTF JSON norāda uz ārējiem binārajiem datiem (ģeometriju, atslēgu rāmjiem, apvalkiem) un attēliem.

* glTF JSON iegulst base64 kodētus bināros datus un attēlus, izmantojot datu URI.


GLB kā konteinera formāts tika ieviests kā binārais faila formāts glTF līdzekļa attēlošanai binārā blobā, lai izvairītos no glTF radītajām problēmām. GLB faila formāts [specifications](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) ir jāatsaucas uz jebkuru lasītāju/rakstītāju, kas ir ieviests lietojumprogrammu izstrādei.

## GLB failu struktūra

GLB faila formāts ir balstīts uz mazo endianu, un tā struktūra parāda, ka tajā ir:

* 12 baitu preambula ar virsrakstu.

* Viens vai vairāki gabali, kas satur JSON saturu un bināros datus.


#### GLB galvene

GLB faila formāta galvene sastāv no trim 4 baitu ierakstiem:

* uint32 maģija — maģija ir vienāda ar 0x46546C67. Tā ir ASCII virkne glTF, un to var izmantot, lai identificētu datus kā bināro glTF

* uint32 versija — norāda binārā glTF konteinera formāta versiju

* uin32 garums — kopējais binārā glTF garums, ieskaitot galveni un visus gabalus baitos


#### Gabali

Katrai daļai GLB failā ir šāda struktūra:

|uint32|uint32|ubaits[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` — chunkData garums baitos

* `chunkType` — norāda norāda gabala veidu

* `chunkData` — gabala binārā lietderīgā slodze


kur ir gabalu veidi:

|# |Daļa veids|ASCII|Apraksts|Atgadījumi
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Strukturēts JSON saturs|1
|2.|0x004E4942|BIN|Binārais buferis|0 vai 1

Katra gabala sākumam un beigām ir jābūt saskaņotiem ar 4 baitu robežu, un šim nolūkam ir jāizmanto polsterējums.

##### Strukturēts JSON saturs

Tam vajadzētu būt pirmajam binārā glTF īpašuma gabalam, un tas ļauj ieviešanai pakāpeniski izgūt resursus no nākamajiem gabaliem. Tas arī nodrošina iespēju nolasīt tikai atlasītu resursu apakškopu no binārā glTF līdzekļa, piemēram, acs rupjāko LOD. Lai atbilstu izlīdzināšanas prasībām, šim gabalam jābūt polsterētam ar atstarpes rakstzīmēm (0x20).

##### Binārais buferis #####

Šajā daļā ir binārā slodze ģeometrijai, animācijas atslēgu kadriem, apvalkiem un attēliem. Tam ir jābūt otrajam binārā glTF līdzekļa gabalam, un tam jābūt polsterētam ar beigu nullēm (0x00), lai atbilstu līdzināšanas prasībām.

## Atsauces Nr.

* [GLB faila formāta specifikācijas — Khronos](/3d/gltf/)


