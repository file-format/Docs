{
  "date": "2021-04-08",
  "keywords": [
"comhad ramha",
"formáid comhaid oar",
"cad is comhad ramhaí ann",
"comhad",
"oar shampla",
"síneadh comhad oar",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OAR - Formáid Chomhaid Cartlainne OpenSimulator",
  "description": "Foghlaim faoi fhormáid comhaid OAR agus APIs ar féidir leo comhaid OAR a chruthú agus a oscailt.",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oa-gar"
}
},
  "lastmod": "2021-04-15"
}

## Cad is comhad OAR ann?

Is comhad cartlainne é comhad le síneadh .oar a úsáideann an feidhmchlár OpenSimulator ar freastalaí feidhmchláir foinse oscailte 3D é chun timpeallacht fhíorúil a chruthú a bhfuil rochtain ag il-úsáideoirí air thar an líonra. Soláthraíonn formáid comhaid OAR na sonraí sócmhainne riachtanacha a theastaíonn chun an tír-raon, uigeachtaí réada, agus fardail a luchtú go hiomlán ar chóras difriúil. Tá hypergrid roghnach ag OpenSimulator freisin a ligeann d’úsáideoirí cuairt a thabhairt ar shuiteálacha OpenSimulator eile ar fud an ghréasáin. Tá feidhmchlár/mamha de chineál MIME idirlín ag comhaid OAR agus tá comhad amháin nó níos mó sa chartlann iontu.


## Formáid Chomhaid OAR

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. Is comhad tarra gzipped (tar.gz) san fhormáid bhunaidh unix tar (ní USTAR) é comhad OAR.

## Sampla Réigiúin OAR
Is féidir le réigiúin iolracha a bheith i gcomhaid AOR. Seo a leanas struchtúr na cartlainne (tá 4 réigiún sa sampla seo):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## Cartlann OAR.xml

Tá uimhir leagain mhór sa chomhad rialaithe cartlainne chun comhoiriúnacht le hathruithe formáide sa todhchaí a shainiú. Léirítear láithreacht sócmhainní i bhformáid OAR leis an eilimint Boole<assets_included> . Tá faisnéis faoi na réigiúin san áireamh i bhfoilseachán atá sa chomhad rialaithe. Seo a leanas sampla de Archive.xml.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Tagairtí

 * [Formáid OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

