---
date: 2020-11-11
keywords: myi, .myi, myi 파일 형식, myi 파일을 여는 방법, .myi 확장자, myi 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: MYI 파일 형식
linktitle: MYI
description: "MYI 파일 형식과 MYI 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "database"
lastmod: 2020-13-01
---

## MYI 파일이란? ##

MYI는 MySQL MyISAM 인덱스 파일이라고도 합니다. MySQL에서 MyISAM 테이블에 대한 인덱스를 저장하는 데 사용됩니다. MySQL 데이터베이스 인덱스는 테이블의 구조를 정의하고 테이블의 무결성을 확인하는 제어 메커니즘을 포함합니다.

## MYI 파일 형식 ##

MYI 파일은 헤더와 키 값의 두 부분으로 구성됩니다.

### MYI 헤더 ###

헤더에는 옵션, 파일 크기 및 키에 대한 정보가 포함됩니다. MySQL의 키는 다음과 같은 명령으로 생성됩니다.

```sql
CREATE [UNIQUE] INDEX.
```

MYI 파일을 읽고 쓰는 파일은 ./myisam 디렉토리에 있습니다. 다음 파일이 있습니다.

- mi_open.c: 이 파일은 헤더의 각 섹션을 작성하는 루틴을 포함합니다.
- mi_create.c: 이 파일에는 mi_open.c 루틴을 호출하는 루틴이 있습니다.
- myisamdef.h: 이 파일에는 구조 정의가 있습니다.

헤더에는 다음 섹션이 있습니다.

- state: 상태는 mi_open.c, mi_state_info_write()에 의해 작성됩니다. 이 구조는 파일에서 한 번 발생합니다.
- base: 베이스는 mi_open.c, mi_base_info_write()에 의해 작성됩니다. MI_BASE_INFO는 myisamdef.h의 베이스에 해당하는 구조입니다. 이 구조는 파일에서 한 번 발생합니다.
- keydef: keydef는 mi_open.c, mi_keydef_write()에 의해 작성됩니다. MI_KEYDEF는 myisamdef.h에 있는 keydef에 해당하는 구조입니다. 각 인덱스에 대해 나타나는 다중 발생 구조입니다.
- recinfo: recinfo는 mi_open.c, mi_recinfo_write()에 의해 작성됩니다. MI_COLUMNDEF는 myisamdef.h에 있는 recinfo에 해당하는 구조입니다. 키에 나타나는 각 필드마다 한 번씩 나타나는 다중 발생 구조입니다.

### 키 값 ###

MySQL에서 페이지는 블록이라고 합니다. 키 값은 블록에 있습니다. 블록에는 한 인덱스의 정보만 포함됩니다. 각 키는 모든 열의 전체 내용을 포함합니다. 일반 블록 길이는 0x0400(1024)바이트입니다. 포인터는 순서 행 번호를 포함하는 고정 행 테이블에 대해 고정 크기(4바이트) 번호를 갖습니다. 키가 null이면 바이트는 0x00입니다. 일반 블록은 65% 이상 차고 일반적으로 80% 차 있습니다.

myisamdef.h 파일에는 상수로 표현된 다음과 같은 정보가 포함되어 있습니다. 최대 키 수는 32(MI_MAX_KEY)이고 키의 최대 세그먼트 수는 16(MI_MAX_KEY_SEG)입니다. 키의 최대 길이는 500(MI_MAX_KEY_LENGTH)입니다. 블록의 최대 길이는 16384(MI_MAX_KEY_BLOCK_LENGTH)입니다.

## 참조 ##

- [.MYI 파일](https://dev.mysql.com/doc/dev/mysql-server/latest/)

