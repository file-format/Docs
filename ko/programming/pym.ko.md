---
date: 2022-05-09
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYM 파일 형식 - PYM 매크로 전처리기 파일
linktitle: PYM
description: "PYM 파일 형식 및 PYM 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .PYM 파일이란?

PYM 파일은 Python 프로그래밍 언어를 기반으로 하는 매크로 전처리기 파일입니다. VRVis Research에서 개발했으며 매크로 바로 가기를 저장합니다. PYM 파일이 Python 인터프리터의 전처리 단계에서 해석될 때 이러한 단축키는 전체 텍스트를 대체하기 위해 확장됩니다. 또한 매크로 전처리기가 수행할 수 있는 세 번째 선택적 작업은 파일 포함입니다. PYM 파일은 메모장, 메모장++, Apple TextEdit 및 Linux의 VI와 같은 텍스트 편집기에서 열 수 있습니다.

## PYM 파일 형식

PYM 파일은 디스크에 일반 텍스트 파일로 저장됩니다. PYM 파일은 `#include` 지시문을 사용하여 다른 파일을 포함할 수도 있습니다.

### PYM 구문

PYM 문은 아래와 같이 ""#begin python"과 "#end python" 마커 사이에 포함됩니다.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### PYM 매크로 확장

PYM 매크로 확장은 <[ 및 ]>의 두 시퀀스로 표시됩니다. 이것은 특별한 html 태그이며 한 줄의 아무 곳에나 나타날 수 있습니다. 약간의 PYM 예는 다음과 같습니다.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

PYM을 통해 실행한 결과는 다음과 같습니다.

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## 참조 ##

* [PYM - Python 기반 매크로 전처리기](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [PYM 통역사](https://github.com/interpreters/pym)

