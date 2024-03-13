{
  "date": "2021-04-08",
  "keywords": [
"avar faylı",
"oar fayl formatı",
"avar faylı nədir",
"fayl",
"avar nümunəsi",
"oar fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OAR - OpenSimulator Arxiv Fayl Formatı",
  "description": "OAR fayl formatı və OAR fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oa-azr"
}
},
  "lastmod": "2021-04-15"
}

## OAR faylı nədir?

.oar uzantılı fayl şəbəkə üzərindən çoxlu istifadəçilər üçün əlçatan olan virtual mühit yaratmaq üçün açıq mənbəli 3D proqram serveri olan OpenSimulator proqramı tərəfindən istifadə edilən arxiv faylıdır. OAR fayl formatı ərazini, obyekt teksturalarını və inventarları fərqli bir sistemə tam yükləmək üçün tələb olunan zəruri aktiv məlumatlarını təmin edir. OpenSimulator həmçinin istifadəçilərə internet üzərindən digər OpenSimulator qurğularına baş çəkməyə imkan verən əlavə hiperqridə malikdir. OAR fayllarında internet MIME tipli proqram/oar var və bir və ya daha çox arxivləşdirilmiş faylı ehtiva edir.


## OAR fayl formatı

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. OAR faylı orijinal unix tar formatında (USTAR deyil) gziplənmiş tar faylıdır (tar.gz).

## OAR Regionları Nümunəsi
AOR faylları bir neçə bölgədən ibarət ola bilər. Arxivin strukturu aşağıdakı kimidir (bu nümunədə 4 bölgə var):

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

Arxiv nəzarət faylı gələcək format dəyişiklikləri ilə uyğunluğu müəyyən etmək üçün əsas versiya nömrəsini ehtiva edir. OAR formatında aktivlərin mövcudluğu boolean elementi ilə göstərilir<assets_included> . Daxil edilmiş bölgələr haqqında məlumat nəzarət faylında mövcud olan manifestdə var. Archive.xml nümunəsi aşağıdakı kimidir.

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

## İstinadlar

 * [OAR Format v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

