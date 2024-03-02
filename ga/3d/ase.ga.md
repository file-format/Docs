{
  "date": "2021-01-22",
  "keywords": [
"ASE",
"comhad",
"formáid",
"cineál comhaid",
"síneadh",
"cad is comhad ASE ann?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid ASE agus APIanna ar féidir leo comhaid ASE a oscailt agus a chruthú.",
  "title": "ASE - Autodesk ASCII Comhad Easpórtála Radharc",
  "linktitle": "ASE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-as-gae"
}
},
  "lastmod": "2021-01-22"
}

## Cad is comhad ASE ann?

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## Formáid Chomhaid ASE - Tuilleadh Eolais

Is comhaid téacs iad comhaid ASE atá stóráilte i bhformáid ASCII is féidir a oscailt in aon eagarthóir téacs. Féadfaidh na cineálacha faisnéise seo a leanas a sholáthraíonn Autodesk a bheith i gcomhad ASE.

### Roghanna Aschuir

 * `Mogalra Sainmhíniú` - Onnmhairítear an sainmhíniú ar gach mogaill, lena n-áirítear faisnéis rinn agus aghaidh le haghaidh réad geoiméadrach. Ina theannta sin, cuireann sé seo ar chumas na míreanna sa bhosca grúpa Roghanna Mogall, a gcuirtear síos orthu thíos.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * `Eochracha Beochana Trasfhoirmigh` - Áirítear leis na sonraí beochana claochlaithe do na rudaí. Más ceamara sprice nó spotsolas é an réad, beidh sonraí sprice beochana san áireamh.
 * `Mogalra Beoite` - Onnmhairítear sainmhíniú mogalra iomlán ar gach n fráma. Tá an minicíocht sonraithe ag rothlóir Aschuir an Rialaitheora, a gcuirtear síos air thíos. Tá an fhaisnéis chéanna atá sonraithe i ngach bloc sa bhosca grúpa Roghanna Mogall, a gcuirtear síos orthu thíos. Is féidir comhad ollmhór a bheith mar thoradh air seo a chur ar siúl, fiú i gcás radhairc bheaga.
 * `Ceamara Beoite/Socruithe Solais` - Onnmhairítear na sonraí beochana le haghaidh ceamaraí agus soilse, amhail dath, déine, falloff, laofacht léarscáile, agus mar sin de. Aschuir bloc gach n fráma, mar atá sonraithe ag rothlóir Aschuir an Rialaitheora.
 * `Inverse Kinematic Joints` - Onnmhairítear comhshocruithe IK sa bhrainse Ordlathais.

### Cineálacha Réada

Ligeann na míreanna anseo duit a shonrú cén chatagóir oibiachta a theastaíonn uait a áireamh san aschur. Is féidir leat rudaí geoiméadracha, cruthanna, ceamaraí, soilse, agus rudaí cúntóra a áireamh.

 * Geoiméadrach
 * Cruthanna
 * Ceamaraí
 * Soilse
 * Cúntóirí

### Roghanna mogalra

 * `Normálta Mogall` - Onnmhairítear na gnásanna aghaidhe agus rinn. Tá gnáth an aghaidh liostaithe ar dtús, agus na trí rinn a thacaíonn leis an aghaidh ina dhiaidh sin. Tá sé seo á chur ar siúl i gcomhad i bhfad níos mó.
 * `Comhordanáidí Mapála` - Onnmhairítear liosta de rinn agus d'aghaidheanna mapála, de réir struchtúir TVert agus TVFace a bhfuil cur síos orthu sa 3ds Max Software Development Kit. Má úsáideann réad léarscáiliú aghaidhe, easpórtáiltear liosta aghaidhléarscáileanna ina bhfuil comhordanáidí UVW do gach aghaidh.
 * `Dathanna rinn` - Easpórtálacha dathanna rinn.

### Aschur Rialaitheora

 * `Eochracha Úsáide` - Onnmhairítear luachanna tábhachtacha. Mura n-úsáideann an rialaitheoir eochracha, úsáidtear an modh Sampla Fórsa. I gcás rialtóirí claochlaithe, ní oibríonn an rogha Eochracha Úsáide ach amháin más rud é go bhfuil na rialaitheoirí trasfhoirmithe go léir Líneach/TCB nó Bezier. Má úsáideann ceann de na rianta claochlaithe cineál difriúil rialtóra, ansin úsáidtear an modh Sampla Fórsa do gach rian claochlaithe.
 * `Samplaí Fórsa` - Samplaí de luachanna rialtóra bunaithe ar an minicíocht a shonraítear sna Frámaí in aghaidh an Rialaitheora Samplach.

## Tagairtí

 * [Autodesk - Á onnmhairiú chuig ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

