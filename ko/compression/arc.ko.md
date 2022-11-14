---
date: 2019-12-09
keywords: arc, .arc, arc 파일 형식, arc 파일을 여는 방법, .arc 확장자, arc 확장자
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: ARC 파일 형식
linktitle: ARC
description: "ARC 파일 형식과 ARC 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "compression"
lastmod: 2020-13-01
---

## .ARC 파일이란?

ARC는 SEA(System Enhancement Associates)에서 개발한 무손실 데이터 압축 및 보관 형식입니다. 파일 형식과 이를 생성하는 응용 프로그램을 모두 ARC라고 합니다. ARC는 동일한 파일에 여러 파일을 압축하고 보관하는 기능을 결합했기 때문에 전화 접속 BBS 초기에 매우 인기가 있었습니다. ARC는 나중에 더 나은 압축 비율을 제공하는 [ZIP](/ko/compression/zip/)으로 대체되었습니다.

.arc 파일 확장자는 여러 웹 리소스를 저장하기 위해 Internet Archive에서 사용하는 ARC 형식, FreeArc 아카이버에서 사용하는 다른 ARC 형식, Nintendo에서 리소스에 사용하는 다른 형식 등과 같은 여러 다른 관련 없는 아카이브 파일 유형에서 사용됩니다. .

## ARC 파일 형식의 간략한 역사

ARC 프로그램은 1985년 System Enhancement Associates의 Thom Henderson이 작성했습니다. 이 프로그램은 파일을 단일 아카이브 파일로 그룹화하고 압축하기도 했습니다. ARC 프로그램에 의해 생성된 파일은 .arc 확장자를 사용했습니다. SEA는 1986년 ARC용 소스 코드를 발표했고 ARC는 1987년 Howard Chu에 의해 Unix와 Atari ST로 이식되었습니다.

Phil Katz는 파일 보관 및 추출을 위해 PKARC 및 PKXARC를 개발했습니다. 파일은 ARC 파일 형식으로 작업했으며 훨씬 더 빨랐습니다. ARC와 달리 Katz는 압축 및 보관 기능을 두 개의 다른 파일로 분할하여 실행에 필요한 메모리를 줄였습니다.

SEA와 Katz 간의 소송 이후 SEA는 셰어웨어 시장에서 철수하고 전체 화면 사용자 인터페이스를 갖춘 ARC+Plus를 개발했습니다. ARC 형식은 더 이상 PC에서 일반적이지 않습니다.

## ARC 파일 형식

ARC 파일은 아래와 같이 파일 헤더와 파일의 순서로 구성되며 아카이브 끝 마커가 뒤따릅니다.

```console
  file header 1
    file 1
  file header 2
    file 2
  .
  .
  file header n
    file n
EOF
```

### ARC 파일 헤더 ###

|오프셋|레이블|유형|값|설명|
|---|---|---|---|---|
|00|ARCID |DB|$1A| |
|01|ARCMTD|DB|00|메소드|
|02|ARCFNT|DS|12|파일명|
|0E| |DB|00| |
|0F|ARCNSZ|HEX|00000000|압축 사이즈|
|13|ARCDAT|DW|0000|파일 날짜(MSDOS)|
|15|ARCTIM|DW|0000|파일 시간(MSDOS)|
|17|ARCRCRC|DW|0000| |
|19|ARCOSZ|HEX|00000000|압축되지 않은 크기|
|1D|ARCFIL|DS|ARCNSZ| |

### 압축 방법 ###

압축 방법 바이트는 사용된 압축 방법을 나타냅니다. 다음은 ARC 파일에 사용되는 압축 방법입니다.

|방법|이름|설명|
|---|---|---|
|0|저장됨|압축 사용 안함|
|1|패키지|반복 실행 길이 인코딩(RLE)|
|2|압축|허프만 인코딩|
|3|크런치|4K 버퍼가 있는 LZW, 12비트 코드|
|4|크런치|첫 번째 패킹, 그 다음 12비트의 LZW 4K 버퍼|
|5|크런치|패킹, LZW, 4K 버퍼, 가변 길이(9-12비트)|
|6|스쿼시|LZW, 8K 버퍼, 가변 길이(9-13비트)|
|7|압쇄|패킹, LZW 8K 버퍼, 2-13비트(PAK 1.0)|
|8|증류|8K 버퍼가 있는 동적 허프만(PAK 2.0)|

## 참고문헌

- [ARC(파일 형식) - Wikipedia](https://en.wikipedia.org/wiki/ARC_(file_format))

