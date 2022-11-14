---
date: 2022-05-09
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYD 파일 형식 - Python 동적 모듈
linktitle: PYD
description: "PYD 파일 형식 및 PYD 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .PYD 파일이란?

PYD 파일은 런타임에 다른 Python 코드에서 실행할 수 있는 Python으로 작성된 동적 링크 라이브러리입니다. 여기에는 코드 재사용을 용이하게 하고 애플리케이션 작성을 위한 모듈 아키텍처를 제공하는 하나 이상의 Python 모듈이 포함됩니다. PYD 파일은 .pyd 확장자로 생성 및 저장할 수 있습니다(예: helloworld.pyd). 애플리케이션 개발자는 import 문을 사용하여 애플리케이션에 PYD 모듈을 포함할 수 있습니다. PYD 파일은 Windows, Mac 및 Linux OS에서 사용할 수 있는 Python Software Foundation Python으로 열 수 있습니다.

## PYD 파일 형식 - 추가 정보

PYD 파일은 Python 프로그래밍 언어로 작성되며 Python 코드를 컴파일하여 생성됩니다.

## PY와 PYD 파일 형식의 차이점

[PY](/ko/programming/py/) 파일에는 있는 그대로 실행되는 소스 코드가 포함되어 있으며 다른 Python 응용 프로그램에서 재사용 가능한 코드로 포함될 수 없습니다. 그러나 PYD 파일은 Windows 운영 체제에서 사용되는 동적으로 연결된 라이브러리입니다.

## PYD 파일을 만드는 방법?

PYD 파일은 exmaple.pyd와 같은 이름으로 모듈을 생성하여 생성할 수 있습니다. 이 모듈은 PyMod_example()과 같은 하나 이상의 함수 형태로 모든 기능을 포함합니다. 프로그램이 이 라이브러리를 포함하고 호출할 때 모듈을 가져와서 수행할 수 있으며 PyMod_example() 함수가 실행됩니다.

## 참조 ##

* [C/C++에서 Python Extension 만들기](https://sebsauvage.net/python/mingw.html)
* [파이썬(프로그래밍 언어) - 위키피디아](https://en.wikipedia.org/wiki/Python_(programming_language))

