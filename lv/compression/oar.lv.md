{
  "date": "2021-04-08",
  "keywords": [
"aira fails",
"oar faila formāts",
"kas ir aira fails",
"failu",
"aira piemērs",
"oar faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OAR — OpenSimulator arhīva faila formāts",
  "description": "Uzziniet par OAR faila formātu un API, kas var izveidot un atvērt OAR failus.",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oa-lvr"
}
},
  "lastmod": "2021-04-15"
}

## Kas ir OAR fails?

Fails ar paplašinājumu .oar ir arhīva fails, ko izmanto lietojumprogramma OpenSimulator, kas ir atvērtā koda 3D lietojumprogrammu serveris, lai izveidotu virtuālo vidi, kas tīklā ir pieejama vairākiem lietotājiem. OAR faila formāts nodrošina nepieciešamos līdzekļu datus, kas nepieciešami, lai pilnībā ielādētu reljefu, objektu faktūras un krājumus citā sistēmā. OpenSimulator piedāvā arī papildu hiperrežģi, kas ļauj lietotājiem apmeklēt citas OpenSimulator instalācijas tīmeklī. OAR failiem ir interneta MIME tipa lietojumprogramma/oar, un tajos ir viens vai vairāki arhivēti faili.


## OAR faila formāts

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. OAR fails ir gzip fails tar fails (tar.gz) sākotnējā unix tar formātā (nevis USTAR).

## OAR reģionu piemērs
AOR faili var saturēt vairākus reģionus. Arhīva struktūra ir šāda (šajā piemērā ir 4 reģioni):

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
## OAR Archive.xml

Arhīva vadības fails satur galveno versijas numuru, lai noteiktu saderību ar turpmākām formāta izmaiņām. Līdzekļu esamību OAR formātā norāda Būla elements<assets_included> . Informācija par iekļautajiem reģioniem ir ietverta manifestā, kas atrodas vadības failā. Archive.xml piemērs ir šāds.

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

## Atsauces

 * [OAR formāts v1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

