---
date: 2019-10-11
keywords: py, python, .py, py 파일 형식, py 파일을 여는 방법, py 파일을 실행하는 방법, python 파일을 실행하는 방법, 파이썬을 실행하는 방법
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PY 파일 형식
linktitle: PY
description: "PY 파일 형식 및 PY 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## .PY 파일이란? ##

확장자가 .py인 파일에는 Python 소스 코드가 포함되어 있습니다. Python 언어는 이제 매우 유명한 언어가 되었습니다. 시스템 스크립팅, 웹 및 소프트웨어 개발 및 수학에 사용할 수 있습니다. Python은 플랫폼 간 호환성을 지원합니다. Python으로 개발된 애플리케이션이 Windows, MAC, Linux, Raspberry Pi 등과 같은 다양한 플랫폼에서 작동할 수 있음을 의미합니다. Python은 영어와 유사한 간단하고 읽기 쉬운 구문을 제공합니다. 개발자는 몇 줄의 Python 코드를 작성하여 합리적인 소프트웨어 응용 프로그램을 작성할 수 있습니다. 파이썬은 인터프리터 시스템에서 실행되기 때문에 코드가 작성되자마자 실행될 수 있어 프로토타이핑에 매우 좋습니다.

## 간략한 역사 ##

Python은 1980년대 후반 Guido van Rossum이 ABC 프로그래밍 언어의 후계자로 생각했습니다. 1989년 12월 Van Rossum이 유일한 수석 개발자로 구현되기 시작했습니다. 그는 2018년 7월 12일까지 파이썬에서 일했습니다. 2019년 1월에 활동적인 Python 핵심 개발자는 Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw 및 Van Rossum으로 구성된 5명의 "운영 위원회"를 프로젝트를 이끌도록 선출했습니다.

### 버전 ###

- Python 2.0은 2000년 10월 16일에 출시되었습니다.
- Python 3.0은 2008년 12월 3일에 릴리스되었습니다.

## py 파일을 실행하는 방법 ##

설치된 Python 버전을 확인하려면 다음 명령을 사용할 수 있습니다.

```cmd
python --version
```

이렇게 하면 콘솔에 다음과 같은 버전이 출력됩니다.

```cmd
Python 3.7.4
```

컴퓨터에 Python이 설치되어 있지 않은 경우 [python.org](https://www.python.org/)로 이동하여 관련 운영 체제에 맞는 Python을 다운로드하여 설치할 수 있습니다.

Python 스크립트를 실행하려면 다음 명령을 사용할 수 있습니다.

```cmd
python helloworld.py
```

*helloworld.py*는 다음 코드를 포함하는 스크립트 파일입니다.

```py
print("Hello World from Python")
```

그러면 콘솔 창에 다음이 인쇄됩니다.

```cmd
Hello World from Python
```

참고: IDE를 사용하는 경우 IDE는 화면에 버튼을 제공하거나 Python을 실행하기 위한 다른 키보드 단축키를 제공합니다. 예를 들어 Python 스크립트를 실행할 수 있는 PyCharm의 편집기가 있는 여백에 재생 버튼이 표시됩니다.

## PY 파일 형식 ##

Python은 가독성을 위해 설계되었으며 영어 및 수학과 유사합니다. Python은 다른 언어에서 사용되는 세미콜론이나 괄호와 달리 새 줄을 사용하여 완전한 명령을 나타냅니다. 범위, 루프 및 함수의 경우 Python은 다른 언어에서 사용되는 중괄호와 달리 들여쓰기와 공백에 의존합니다.

### 구문 ###

다음은 Python 구문의 예입니다.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## 참조 ##

- [Python(프로그래밍 언어) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

