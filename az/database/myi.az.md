---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI Fayl Formasıat
linktitle: MYI
description: LMYI fayl formatı və MYI faylını yarada və aça bilən API-lər haqqında qazanıns.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## MYI faylı nədir? ##

MYI həm də MySQL MyISAM İndeksi faylı kimi tanınır. MySQL tərəfindən MyISAM cədvəli üçün indeksləri saxlamaq üçün istifadə olunur. MySQL verilənlər bazası indeksi cədvəlin strukturunu müəyyən edir və cədvəllərin bütövlüyünü yoxlamaq üçün idarəetmə mexanizmini ehtiva edir.

## MYI Fayl Format ##

MYI faylı iki hissədən ibarətdir, başlıq və açar dəyərlər.

### MYI Başlığı ###

Başlıqda seçimlər, fayl ölçüləri və açarlar haqqında məlumat var. MySQL-dəki açarlar kimi bir əmrlə yaradılır

```sql
CREATE [UNIQUE] INDEX.
```

MYI fayllarını oxuyan və yazan fayllar ./myisam qovluğundadır. Aşağıdakı fayllar var:

- mi_open.c: Bu fayl başlığın hər bir hissəsini yazan rutinləri ehtiva edir.
- mi_create.c: Bu faylda mi_open.c rutinlərini çağıran rutinlər var.
- myisamdef.h: Bu fayl struktur təriflərinə malikdir.

Başlıqda aşağıdakı bölmələr var:

- dövlət: Dövlət mi_open.c, mi_state_info_write() tərəfindən yazılır. Bu struktur faylda bir dəfə baş verir.
- baza: Baza mi_open.c, mi_base_info_write() tərəfindən yazılmışdır. MI_BASE_INFO myisamdef.h-də baza üçün müvafiq strukturdur. Bu struktur faylda bir dəfə baş verir.
- keydef: Keydef mi_open.c, mi_keydef_write() tərəfindən yazılmışdır. MI_KEYDEF myisamdef.h-də keydef üçün müvafiq strukturdur. Bu, hər bir indeks üçün görünən çoxillik strukturdur.
- recinfo: Recinfo mi_open.c, mi_recinfo_write() tərəfindən yazılmışdır. MI_COLUMNDEF myisamdef.h-də recinfo üçün müvafiq strukturdur. Bu, açarda görünən hər sahədən bir dəfə görünən çoxlu baş verən strukturdur.

### Əsas Dəyərlər ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. Normal blok ən azı 65% doludur və adətən 80% doludur.

myisamdef.h faylı sabitlərlə ifadə olunan aşağıdakı məlumatları ehtiva edir. Açarların maksimum sayı 32 (MI_MAX_KEY) və açardakı seqmentlərin maksimum sayı 16-dır (MI_MAX_KEY_SEG). Açarın maksimum uzunluğu 500-dür (MI_MAX_KEY_LENGTH). Blokun maksimum uzunluğu 16384 (MI_MAX_KEY_BLOCK_LENGTH) təşkil edir.

## İstinadlar ##

- [The .MYI File](https://dev.mysql.com/doc/dev/mysql-server/latest/)

