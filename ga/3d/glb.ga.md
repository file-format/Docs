{
  "date" : "2019-12-03",
  "keywords" : [ "GLB","file", "format", "file type", "extension","what is an GLB file?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "GLB",
  "description":"Foghlaim faoi fhormáid comhaid GLB agus APIs is féidir comhaid GLB a oscailt agus a chruthú.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb-ga",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## Cad is comhad GLB ann?

Is ionann GLB agus formáid dhénártha de mhúnlaí 3D a shábháiltear i bhFormáid Tarchuir GL ([glTF](/3d/gltf/)). Eolas faoi shamhlacha 3D Mar shampla ordlathas nód, ceamaraí, ábhair, beochan agus meshes i bhformáid dhénártha.... Stórálann an fhormáid dhénártha seo an tsócmhainn glTF (JSON, .bin agus íomhánna) i mbileog dhénártha. Seachnaíonn sé freisin an cheist maidir le méadú ar mhéid comhaid a tharlaíonn i gcás glTF. Mar thoradh ar fhormáid comhaid GLB tá méideanna comhaid dlúth, luchtú tapa, léiriú radharc 3D iomlán, agus insínteacht le haghaidh tuilleadh forbartha. Úsáideann an fhormáid model/gltf-dénártha mar chineál MIME.

## Formáid Chomhaid GLB - Tuilleadh Eolais

Mar thoradh ar na modhanna seachadta ábhair a úsáideann glTF déantar próiseáil bhreise chun na sonraí dénártha ionchódaithe bonn-64 a dhíchódú agus méadaítear méid an chomhaid 33%. I measc na modhanna seachadta seo, a chuidigh le foirmiú formáid comhaid GLB, tá:

* Díríonn glTF JSON ar shonraí dénártha seachtracha (céimseata, eochairfhrámaí, craicne), agus íomhánna.

* Le glTF JSON sonraí dénártha ionchódaithe base64 a leabú, agus íomhánna inlíne ag baint úsáide as URIanna sonraí.


Tugadh GLB isteach mar fhormáid coimeádáin isteach mar fhormáid comhaid dhénártha chun sócmhainn glTF a léiriú i blob dhénártha chun fadhbanna glTF a sheachaint. Ba cheart formáid comhaid GLB [specifications](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) a tharchur le haghaidh aon léitheoir/scríbhneoir a chur i bhfeidhm chun feidhmchláir a fhorbairt.

## Struchtúr Comhad GLB

Tá formáid comhaid GLB bunaithe ar bheagán endian agus léiríonn a struchtúr go bhfuil:

* Brollach 12 beart, dar teideal an ceanntásc.

* Smután amháin nó níos mó ina bhfuil inneachar JSON agus sonraí dénártha.


#### Ceanntásc GLB

Tá trí iontráil 4-bheart i gceanntásc formáid comhaid GLB:

* draíocht uint32 - is ionann draíocht agus 0x46546C67. Is glTF teaghrán ASCII é, agus is féidir é a úsáid chun sonraí a aithint mar glTF Dénártha

* Leagan uint32 - léiríonn an leagan de formáid coimeádán Dénártha glTF

* Fad uin32 - fad iomlán an glTF Dénártha, lena n-áirítear Ceanntásc agus gach smután i mbearta


#### Smután

Tá an struchtúr seo a leanas ag gach smután i gcomhad GLB:

|uint32|uint32|ubyte[]
---|---|---|
|ChunkFad|Cineál chuimne|Sonraí Chun Cinn

* `chunkLength` - fad an chunkData i mbearta

* `ChunkType` - léiríonn sé an cineál smután

* `chunkData` - pálasta dhénártha de smután


Cá bhfuil na cineálacha smután:

|# |Cineál smután|ASCII|Cur Síos|Teagmhais
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Ábhar struchtúrtha JSON|1
|2.|0x004E4942|ARAID|Maolán dénártha|0 nó 1

Ní mór tús agus deireadh gach smután a ailíniú le teorainn 4 beart agus ba chóir stuáil a úsáid chun na críche sin.

##### Ábhar JSON Struchtúrtha

Ba cheart go mbeadh sé seo ar an gcéad chuid de shócmhainn Dénártha glTF agus cuireann sé ar chumas an fhorfheidhmithe acmhainní a aisghabháil de réir a chéile ó shócmhainní ina dhiaidh sin. Soláthraíonn sé seo freisin an cumas gan ach fo-thacar roghnaithe acmhainní a léamh ó shócmhainn Dénártha glTF cosúil leis an LOD is garbh de mhogalra. Chun na riachtanais ailínithe a chomhlíonadh, ní mór an smután seo a stuáil le carachtair spáis (0x20).

##### Maolán Dénártha #####

Sa smután seo tá an pálasta dhénártha le haghaidh céimseata, frámaí eochracha beochana, craicne agus íomhánna. Ba cheart go mbeadh sé ar an dara smután den tsócmhainn Dénártha glTF agus ní mór é a stuáil le nialais rianaithe (0x00) chun na ceanglais ailínithe a shásamh.

## Tagairtí ##

* [Sonraíochtaí Formáid Comhaid GLB - Khronos](/3d/gltf/)


