{
  "date" : "2019-12-03",
  "keywords" : [ "GLB","file", "format", "file type", "extension","what is an GLB file?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "GLB",
  "description":"Lær om GLB-filformat og API'er, der kan åbne og oprette GLB-filer.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb-da",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Hvad er en GLB fil?

GLB er den binære filformatrepræsentation af 3D-modeller gemt i GL-transmissionsformatet ([glTF](/3d/gltf/)). Information om 3D-modeller såsom nodehierarki, kameraer, materialer, animationer og mesh i binært format. Dette binære format gemmer glTF-aktivet (JSON, .bin og billeder) i en binær blob. Det undgår også spørgsmålet om stigning i filstørrelse, som sker i tilfælde af glTF. GLB-filformat resulterer i kompakte filstørrelser, hurtig indlæsning, komplet 3D-scenerepræsentation og udvidelsesmuligheder til videreudvikling. Formatet bruger model/gltf-binær som MIME-type.

## GLB-filformat - flere oplysninger

Indholdsleveringsmetoderne brugt af glTF resulterer i ekstra behandling for at afkode de base-64-kodede binære data og øger også filstørrelsen med 33 %. Disse leveringsmetoder, som bidrog til dannelsen af GLB-filformat, omfatter:

* glTF JSON peger på eksterne binære data (geometri, nøglerammer, skins) og billeder.

* glTF JSON indlejrer base64-kodede binære data og billeder inline ved hjælp af data-URI'er.


GLB som containerformat blev introduceret som binært filformat til repræsentation af glTF-aktiv i en binær blob for at undgå problemer forårsaget af glTF. GLB-filformatet [specifications](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) skal henvises til enhver læser/skriverimplementering af samme til applikationsudvikling.

## GLB filstruktur

GLB-filformatet er baseret på little endian, og dets struktur viser, at det indeholder:

* En 12-byte præamble med titlen overskriften.

* En eller flere chunks, der indeholder JSON-indhold og binære data.


#### GLB Header

GLB filformatheaderen består af tre 4-byte poster:

* uint32 magi - magi er lig med 0x46546C67. Det er ASCII-streng glTF og kan bruges til at identificere data som binær glTF

* uint32 version - angiver versionen af binært glTF containerformat

* uin32 længde - den samlede længde af den binære glTF, inklusive Header og alle bidder i bytes


#### Klumper

Hver chunk i en GLB-fil har følgende struktur:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - længden af chunkData i bytes

* `chunkType` - angiver angiver typen af chunk

* `chunkData` - binær nyttelast af chunk


hvor chunk typerne er:

|# |Chunk Type|ASCII|Beskrivelse|Forekomster
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Struktureret JSON-indhold|1
|2.|0x004E4942|BIN|Binær buffer|0 eller 1

Starten og slutningen af hver chunk skal justeres til 4-byte-grænsen, og polstring skal bruges til dette formål.

##### Struktureret JSON-indhold

Dette bør være den allerførste del af binær glTF-aktiv og gør det muligt for implementeringen gradvist at hente ressourcer fra efterfølgende bidder. Dette giver også mulighed for kun at læse et udvalgt undersæt af ressourcer fra et binært glTF-aktiv, såsom den groveste LOD af en maske. For at opfylde tilpasningskravene skal denne chunk være polstret med efterfølgende mellemrumstegn (0x20).

##### Binær buffer #####

Denne del indeholder den binære nyttelast til geometri, animationsnøgleframes, skins og billeder. Det bør være den anden del af det binære glTF-aktiv og skal være polstret med efterfølgende nuller (0x00) for at opfylde tilpasningskravene.

## Referencer ##

* [GLB-filformatspecifikationer - Khronos](/3d/gltf/)


