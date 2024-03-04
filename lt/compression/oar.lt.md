{
  "date": "2021-04-08",
  "keywords": [
"irklo failas",
"oar failo formatas",
"kas yra irklo failas",
"failą",
"irklo pavyzdys",
"oar failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OAR – OpenSimulator archyvo failo formatas",
  "description": "Sužinokite apie OAR failo formatą ir API, kurios gali kurti ir atidaryti OAR failus.",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oa-ltr"
}
},
  "lastmod": "2021-04-15"
}

## Kas yra OAR failas?

Failas su plėtiniu .oar yra archyvo failas, naudojamas OpenSimulator programoje, kuri yra atvirojo kodo 3D taikomųjų programų serveris, skirtas sukurti virtualią aplinką, prieinamą keliems vartotojams tinkle. OAR failo formatas pateikia būtinus ištekliaus duomenis, reikalingus visiškai įkelti reljefą, objektų tekstūras ir atsargas kitoje sistemoje. OpenSimulator taip pat turi pasirenkamą hipertinklelį, leidžiantį vartotojams apsilankyti kituose OpenSimulator įrenginiuose žiniatinklyje. OAR failai turi interneto MIME tipo programą / irklą ir juose yra vienas ar daugiau archyvuotų failų.


## OAR failo formatas

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. OAR failas yra gzipped tar failas (tar.gz) originaliu unix tar formatu (ne USTAR).

## OAR regionų pavyzdys
AOR failuose gali būti keli regionai. Archyvo struktūra yra tokia (šiame pavyzdyje yra 4 regionai):

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
## OAR archyvas.xml

Archyvo valdymo faile yra pagrindinis versijos numeris, skirtas apibrėžti suderinamumą su būsimais formato pakeitimais. Turtų buvimas OAR formatu nurodomas loginiu elementu<assets_included> . Informacija apie įtrauktus regionus yra manifeste, kuris yra valdymo faile. Archive.xml pavyzdys yra toks.

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

## Nuorodos

 * [OAR formatas v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

