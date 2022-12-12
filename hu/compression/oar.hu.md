{
  "date" : "2021-04-08",
  "keywords" :[ "oar fájl", "oar fájlformátum", "mi az oar fájl", "fájl", "oar példa", "oar fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator archív fájlformátum",
  "description":"További információ az OAR fájlformátumról és az API-król, amelyek OAR fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Mi az OAR fájl?

Az .oar kiterjesztésű fájl az OpenSimulator alkalmazás által használt archív fájl, amely egy nyílt forráskódú 3D-s alkalmazásszerver a hálózaton keresztül több felhasználó számára elérhető virtuális környezet létrehozására. Az OAR fájlformátum biztosítja a szükséges eszközadatokat a domborzat, az objektumtextúrák és a készletek teljes betöltéséhez egy másik rendszeren. Az OpenSimulator opcionális hiperrácsot is tartalmaz, amely lehetővé teszi a felhasználók számára, hogy meglátogassanak más OpenSimulator-telepítéseket az interneten. Az OAR fájlok internetes MIME típusú alkalmazással/oarral rendelkeznek, és egy vagy több archivált fájlt tartalmaznak.


## OAR fájlformátum

Az OAR bináris fájlok, amelyeket tömörített archív fájlformátumban tárolnak. Az OAR fájlformátum legújabb verziója az [1.0](http://opensimulator.org/wiki/OAR_Format_1.0), amely jelentős változásokon ment keresztül az előző [0.8-as verzióhoz] (http://opensimulator.org/wiki/OAR_Format_0) .8). A legújabb verzió támogatja több régió egyetlen OAR-ban való tárolását, és visszafelé nem kompatibilis az OpenSimulator 0.7.5 előtti verzióival. Az OAR fájl egy gzip-fájl (tar.gz) az eredeti unix tar formátumban (nem USTAR).

## Példa az OAR régiókra
Az AOR fájlok több régiót is tartalmazhatnak. Az archívum felépítése a következő (ez a példa 4 régiót tartalmaz):

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
## OAR Archívum.xml

Az archív vezérlőfájl egy fő verziószámot tartalmaz a jövőbeli formátumváltozásokkal való kompatibilitás meghatározásához. Az OAR formátumú eszközök jelenlétét a logikai elem jelzi<assets_included> . A felvett régiókra vonatkozó információkat a vezérlőfájlban található jegyzék tartalmazza. Az Archive.xml példája a következő.

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

## Hivatkozások

* [OAR Format v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

