{
  "date" : "2021-04-08",
  "keywords" :[ "soubor vesla", "formát souboru vesla", "co je soubor vesla", "soubor", "příklad vesla", "přípona souboru vesla", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator Archive File Format",
  "description":"Další informace o formátu souboru OAR a rozhraních API, která mohou vytvářet a otevírat soubory OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## Co je soubor OAR?

Soubor s příponou .oar je archivní soubor používaný aplikací OpenSimulator, což je open-source 3D aplikační server pro vytváření virtuálního prostředí přístupného více uživatelům přes síť. Formát souboru OAR poskytuje nezbytná data aktiv potřebná k plnému načtení terénu, textur objektů a inventářů v jiném systému. OpenSimulator má také volitelnou hypermřížku, která uživatelům umožňuje navštívit další instalace OpenSimulatoru po celém webu. Soubory OAR mají internetový MIME typ aplikace/veslo a obsahují jeden nebo více archivovaných souborů.


## Formát souboru OAR

OAR jsou binární soubory, které jsou uloženy ve formátu komprimovaného archivního souboru. Nejnovější verze formátu souboru OAR je [verze 1.0](http://opensimulator.org/wiki/OAR_Format_1.0), která má velké změny oproti předchozí [verze 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). Nejnovější verze podporuje ukládání více oblastí do jednoho OAR a není zpětně kompatibilní s verzemi OpenSimulatoru staršími než 0.7.5. Soubor OAR je soubor gzip tar (tar.gz) v původním unixovém formátu tar (ne USTAR).

## Příklad regionů OAR
Soubory AOR mohou obsahovat více oblastí. Struktura archivu je následující (tento příklad obsahuje 4 oblasti):

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
## Archiv OAR.xml

Řídicí soubor archivu obsahuje hlavní číslo verze pro definování kompatibility s budoucími změnami formátu. Přítomnost aktiv ve formátu OAR je označena logickým prvkem<assets_included> . Informace o zahrnutých oblastech jsou obsaženy v manifestu, který je přítomen v řídicím souboru. Příklad Archive.xml je následující.

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

## Reference

* [Formát OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

