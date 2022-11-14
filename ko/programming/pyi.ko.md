---
date: 2022-05-09
작가:
  display_name: Kashif Iqbal
draft: false
toc: true
title: PYI 파일 형식 - Python 인터페이스 정의
linktitle: PYI
description: "PYI 파일 형식 및 PYI 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## .PYI 파일이란?

PYI 파일은 인터페이스 구현을 위한 코드 스텁 참조를 포함하는 Python 인터페이스 정의 파일입니다. 각 Python 모듈은 일반 Python 파일이지만 빈 메서드가 있는 .pyi 스텁으로 표시됩니다. PYI 파일의 구문은 일반 Python 모듈의 구문과 동일합니다. 빈 메소드의 구현은 최종 사용자가 모듈이 작성된 특정 목표를 달성하도록 남겨둡니다. PYI 파일은 프로그램의 완전한 구현을 포함하는 [PY](/ko/programming/py/) 파일과 다릅니다. PYI 파일은 메모장, 메모장++, Microsoft Visual Studio Code 및 JetBrains PyCharm과 같은 텍스트 편집기로 열 수 있습니다.

## PYI 파일 형식

PYI 파일은 모든 텍스트 편집기로 열 수 있는 일반 텍스트 파일로 저장됩니다. Python은 코드가 실행될 때 유형 검사를 수행하는 인터프리터 언어입니다. 이러한 경우 PYI 파일은 개발자가 애플리케이션을 작성하는 동안 모듈 유형을 수동으로 정의하고 확인할 수 있다는 점에서 유용합니다.

## 참조 ##

* [인터페이스 - 자바](https://en.wikipedia.org/wiki/Interface_(Java))
* [PYM 통역사](https://github.com/interpreters/pym)

