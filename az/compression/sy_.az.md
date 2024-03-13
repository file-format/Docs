{
  "date": "2022-06-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SY_ Fayl Format - Sıxılmış SYS Faylı",
  "description": "SY_ fayl formatı və SY_ fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "SY_",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-sy-az_"
}
},
  "lastmod": "2022-06-24"
}

## SY_ faylı nədir?

SY_ faylı sıxılmış .sys faylıdır və proqram quraşdırıcıları tərəfindən quraşdırıcı daxilində paketlənmiş quraşdırma fayllarının ölçüsünü azaltmaq üçün istifadə olunur. Bu, quraşdırıcının ümumi ölçüsünü azaldır. SY_ faylları bir və ya daha çox sıxılmış faylı genişləndirən Microsoft Expand əmr satırı yardım proqramından istifadə edərək genişləndirilə bilər.

## SY_ Fayl Format - Ətraflı Məlumat

SY_ faylları sıxılmış ikili fayllar kimi diskdə saxlanılır. Lakin onların daxili fayl formatı ictimaiyyətə açıq deyil. Microsoft Expand əmr satırı yardım proqramı aşağıdakı əmr sətirlərindən birini istifadə edərək SY_ fayllarını genişləndirə bilər.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Genişləndirildikdə, SY_ faylları [SYS](/system/sys/) faylına çevrilir.

SY_ faylları EX_ və DL_ fayllarına bənzəyir.

## İstinadlar

 * [StuffIt - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/StuffIt)
 * [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

