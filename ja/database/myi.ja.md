---
date: 2020-11-11
keywords: myi,.myi,myi ファイル形式,myi ファイルの開き方,.myi 拡張子,myi 拡張子
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI ファイル形式
linktitle: MYI
description: "MYI ファイル形式と,MYI ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## MYI ファイルとは? ##

MYI は、MySQL MyISAM インデックス ファイルとも呼ばれます。 MySQL によって MyISAM テーブルのインデックスを格納するために使用されます。 MySQL データベース インデックスは、テーブルの構造を定義し、テーブルの整合性をチェックするための制御メカニズムを含んでいます。

## MYI ファイル形式 ##

MYI ファイルには、ヘッダーとキー値の 2 つの部分があります。

### MYI ヘッダー ###

ヘッダーには、オプション、ファイル サイズ、およびキーに関する情報が含まれています。 MySQL のキーは次のようなコマンドで作成されます

```sql
CREATE [UNIQUE] INDEX.
```

MYI ファイルを読み書きするファイルは、./myisam ディレクトリにあります。次のファイルがあります。

- mi_open.c: このファイルには、ヘッダーの各セクションを書き込むルーチンが含まれています。
- mi_create.c: このファイルには、mi_open.c ルーチンを呼び出すルーチンが含まれています。
- myisamdef.h: このファイルには構造定義が含まれています。

ヘッダーには次のセクションがあります。

- 状態: 状態は、mi_open.c、mi_state_info_write() によって書き込まれます。この構造は、ファイル内で 1 回発生します。
- ベース: ベースは、mi_open.c、mi_base_info_write() によって書き込まれます。 MI_BASE_INFO は、myisamdef.h 内のベースに対応する構造です。この構造は、ファイル内で 1 回発生します。
- keydef: keydef は、mi_open.c、mi_keydef_write() によって書き込まれます。 MI_KEYDEF は、myisamdef.h 内の keydef に対応する構造です。索引ごとに出現する複数出現構造です。
- recinfo: recinfo は、mi_open.c、mi_recinfo_write() によって書き込まれます。 MI_COLUMNDEF は、myisamdef.h 内の recinfo に対応する構造です。キーに出現するフィールドごとに 1 回出現する複数出現構造です。

### 主な値 ###

MySQL のページはブロックと呼ばれます。キー値はブロック単位です。ブロックには、1 つのインデックスのみからの情報が含まれます。各キーには、すべての列の内容全体が含まれています。通常のブロック長は 0x0400 (1024) バイトです。ポインターは、序数の行番号を含む固定行テーブルの固定サイズ (4 バイト) の数値を持ちます。キーが null の場合、バイトは 0x00 です。通常のブロックは、少なくとも 65% 使用されており、通常は 80% 使用されています。

myisamdef.h ファイルには、定数で表現された次の情報が含まれています。キーの最大数は 32 (MI_MAX_KEY) で、キー内のセグメントの最大数は 16 (MI_MAX_KEY_SEG) です。キーの最大長は 500 (MI_MAX_KEY_LENGTH) です。ブロックの最大長は 16384 (MI_MAX_KEY_BLOCK_LENGTH) です。

## 参照 ##

- [.MYI ファイル](https://dev.mysql.com/doc/internals/en/the-myi-file.html)

