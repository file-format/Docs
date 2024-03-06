{
  "date": "2022-06-24",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SY_ faila formāts — saspiests SYS fails",
  "description": "Uzziniet par SY_ faila formātu un API, kas var izveidot un atvērt SY_ failus.",
  "linktitle": "SY_",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-sy-lv_"
}
},
  "lastmod": "2022-06-24"
}

## Kas ir SY_ fails?

SY_ fails ir saspiests .sys fails, ko programmatūras instalētāji izmanto, lai samazinātu instalācijas failu lielumu, kas ir iepakots instalēšanas programmā. Tas samazina uzstādītāja kopējo izmēru. SY_ failus var paplašināt, izmantojot Microsoft Expand komandrindas utilītu, kas paplašina vienu vai vairākus saspiestus failus.

## SY_ faila formāts — vairāk informācijas

SY_ faili tiek saglabāti diskā kā saspiesti binārie faili. Tomēr viņu iekšējais faila formāts nav publiski pieejams. Komandrindas utilīta Microsoft Expand var paplašināt SY_ failus, izmantojot kādu no tālāk norādītajām komandrindām.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Pēc izvēršanas SY_ faili tiek pārveidoti par [SYS](/system/sys/) failu.

SY_ faili ir līdzīgi EX_ un DL_ failiem.

## Atsauces

 * [StuffIt — Wikipedia](https://en.wikipedia.org/wiki/StuffIt)
 * [Microsoft Expand](https://learn.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

