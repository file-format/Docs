{
  "date" : "2019-12-03",
  "keywords" :[ "GLB","fișier", "format", "tip fișier", "extensie","ce este un fișier GLB?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GLB",
  "description":"Aflați despre formatul de fișier GLB și despre API-urile care pot deschide și crea fișiere GLB.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Ce este un fișier GLB?

GLB este reprezentarea în format de fișier binar a modelelor 3D salvate în formatul de transmisie GL ([glTF](/ro/3d/gltf/)). Informații despre modele 3D, cum ar fi ierarhia nodurilor, camerele, materialele, animațiile și rețelele în format binar. Acest format binar stochează activul glTF (JSON, .bin și imagini) într-un blob binar. De asemenea, evită problema creșterii dimensiunii fișierului care se întâmplă în cazul glTF. Formatul de fișier GLB are ca rezultat dimensiuni compacte de fișier, încărcare rapidă, reprezentare completă a scenei 3D și extensibilitate pentru dezvoltare ulterioară. Formatul folosește model/gltf-binary ca tip MIME.

## Format de fișier GLB - Mai multe informații

Metodele de livrare a conținutului utilizate de glTF au ca rezultat o procesare suplimentară pentru a decoda datele binare codificate în bază 64 și, de asemenea, măresc dimensiunea fișierului cu 33%. Aceste metode de livrare, care au contribuit la formarea formatului de fișier GLB, includ:

* glTF JSON indică date binare externe (geometrie, cadre cheie, skin) și imagini.
* glTF JSON încorporează date binare codificate în base64 și imagini în linie folosind URI-uri de date.

GLB ca format container a fost introdus ca format de fișier binar pentru reprezentarea activului glTF într-un blob binar pentru a evita problemele cauzate de glTF. Formatul de fișier GLB [specificații](https://github.com/KhronosGroup/glTF/tree/master/specification/2.0#glb-file-format-specification) ar trebui să fie referit pentru orice implementare de cititor/scriitor a acestuia pentru dezvoltarea aplicațiilor .

## Structura fișierului GLB

Formatul de fișier GLB se bazează pe Little Endian și structura sa arată că conține:

* Un preambul de 12 octeți, intitulat antet.
* Una sau mai multe bucăți care conține conținut JSON și date binare.

#### Antet GLB

Antetul formatului de fișier GLB este format din trei intrări de 4 octeți:

* uint32 magic - magia este egală cu 0x46546C67. Este șir ASCII glTF și poate fi folosit pentru a identifica datele ca GlTF binar
* versiunea uint32 - indică versiunea formatului containerului binary glTF
* lungime uin32 - lungimea totală a glTF binar, inclusiv antetul și toate bucățile în octeți

#### Bucăți

Fiecare bucată dintr-un fișier GLB are următoarea structură:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - lungimea chunkData în octeți
* `chunkType` - indică tipul de bucată
* `chunkData` - sarcina utilă binară a fragmentului

unde tipurile de bucăți sunt:

|# |Tipul blocului|ASCII|Descriere|Apariții
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Conținut JSON structurat|1
|2.|0x004E4942|BIN|Buffer binar|0 sau 1

Începutul și sfârșitul fiecărei bucăți trebuie aliniate la granița de 4 octeți, iar umplutura trebuie utilizată în acest scop.

##### Conținut JSON structurat

Aceasta ar trebui să fie prima bucată a activului Binary glTF și permite implementării să recupereze progresiv resurse din bucățile ulterioare. Acest lucru oferă, de asemenea, capacitatea de a citi doar un subset selectat de resurse dintr-un activ binar glTF, cum ar fi cea mai grosieră LOD a unei rețele. Pentru a îndeplini cerințele de aliniere, această bucată trebuie să fie acoperită cu caractere spațiale (0x20).

##### Buffer binar #####

Această bucată conține sarcina utilă binară pentru geometrie, cadre cheie de animație, skinuri și imagini. Ar trebui să fie a doua bucată a activului binar glTF și trebuie să fie completată cu zerouri finale (0x00) pentru a satisface cerințele de aliniere.

## Referințe ##

* [Specificații de format de fișier GLB - Khronos](/ro/3D/GLTF/)

