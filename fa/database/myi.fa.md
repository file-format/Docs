---
date: 2020-11-11
keywords: myi, .myi, myi file format, how to open myi files, .myi extension, myi extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Mفرم فایل YIat
linktitle: MYI
description: Lدر مورد فرمت فایل MYI و APIهایی که می توانند فایل MYI را ایجاد و باز کنند، کسب درآمد کنیدs.
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## فایل MYI چیست؟ ##

MYI همچنین به عنوان فایل MyISAM Index MySQL شناخته می شود. برای ذخیره شاخص های جدول MyISAM توسط MySQL استفاده می شود. نمایه پایگاه داده MySQL ساختار جدول را تعریف می کند و مکانیزم کنترلی برای بررسی یکپارچگی جداول را در بر می گیرد.

## فرمت فایل MYI ##

فایل MYI دارای دو بخش سربرگ و مقادیر کلیدی است.

### سربرگ MYI ###

هدر حاوی اطلاعاتی در مورد گزینه ها، اندازه فایل ها و کلیدها است. کلیدهای MySQL با دستوری مانند ایجاد می شوند

```sql
CREATE [UNIQUE] INDEX.
```

فایل هایی که فایل های MYI را می خوانند و می نویسند در دایرکتوری ./myisam قرار دارند. دارای فایل های زیر است:

- mi_open.c: این فایل شامل روال هایی است که هر بخش از هدر را می نویسد.
- mi_create.c: این فایل دارای روال هایی است که روتین های mi_open.c را فراخوانی می کند.
- myisamdef.h: این فایل دارای تعاریف ساختار است.

سربرگ دارای بخش های زیر است:

- state: حالت توسط mi_open.c, mi_state_info_write() نوشته شده است. این ساختار یک بار در فایل رخ می دهد.
- base: پایه توسط mi_open.c، mi_base_info_write() نوشته شده است. MI_BASE_INFO ساختار مربوط به پایه در myisamdef.h است. این ساختار یک بار در فایل رخ می دهد.
- keydef: keydef توسط mi_open.c، mi_keydef_write() نوشته شده است. MI_KEYDEF ساختار مربوط به keydef در myisamdef.h است. این یک ساختار چند رخدادی است که برای هر شاخص ظاهر می شود.
- recinfo: recinfo توسط mi_open.c، mi_recinfo_write() نوشته شده است. MI_COLUMNDEF ساختار مربوط به recinfo در myisamdef.h است. این یک ساختار چند رخدادی است که یک بار از هر فیلدی که در یک کلید ظاهر می شود ظاهر می شود.

### مقادیر کلیدی ###

Pages in MySQL are called blocks. Key values are in blocks. A block contains information from only one index. Each key contains the entire contents of all the columns. The normal block length is 0x0400 (1024) bytes. The pointer has a fixed size (4-byte) number for fixed-row tables that contains an ordinal row number. If the key is null then the byte is 0x00. یک بلوک معمولی حداقل 65 درصد پر است و معمولاً 80 درصد پر است.

فایل myisamdef.h حاوی اطلاعات زیر است که به صورت ثابت بیان شده است. حداکثر تعداد کلیدها 32 (MI_MAX_KEY) و حداکثر تعداد بخش ها در یک کلید 16 (MI_MAX_KEY_SEG) است. حداکثر طول کلید 500 (MI_MAX_KEY_LENGTH) است. حداکثر طول بلوک 16384 (MI_MAX_KEY_BLOCK_LENGTH) است.

## منابع ##

- [The .MYI File](https://dev.mysql.com/doc/dev/mysql-server/latest/)

