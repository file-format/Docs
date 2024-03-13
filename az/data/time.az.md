{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME faylı - .time faylı nədir? Linux-da Faylın yaradıldığı vaxt",
  "description" : "TIME faylı haqqında məlumat əldə edin və faylın Linux-da yaradıldığı vaxtı öyrənin",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-az",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## TIME faylı nədir?

TIME fayl formatı istifadəçilərə həyatlarını qeyd etməyə, təşkil etməyə və paylaşmağa kömək edən LIGHT adlı veb sistemi tərəfindən istifadə edilmişdir. Əsasən, o, yazılar toplusunu saxlayır və sistem daxilində istifadəçinin həyat səhifəsində bir qovluğu təmsil edirdi.

## Linux-da faylın nə vaxt yaradıldığını necə öyrənmək olar

Linux-da faylın nə vaxt yaradıldığını öyrənmək üçün `stat` əmrindən istifadə edə bilərsiniz. Bunu necə edə bilərsiniz:

Terminal açın və aşağıdakı əmri yazın:

```
stat <file_path>
```

` ilə əvəz edin<file_path> ` sizi maraqlandıran faylın yolu ilə. Məsələn:

```
stat /path/to/your/file.txt
```

Bu əmr fayl haqqında müxtəlif məlumatları, o cümlədən onun yaradılma vaxtı göstərəcək. Doğum və ya Fayl: ilə başlayan sətri axtarın. Doğum vaxtı faylın fayl sistemində nə vaxt yaradıldığını göstərir.

Çıxışın necə görünə biləcəyinə dair bir nümunə:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Bu nümunədə Doğum vaxtı faylın nə vaxt yaradıldığını göstərir.

