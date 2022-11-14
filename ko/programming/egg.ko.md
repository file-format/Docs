{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG 파일 형식 - Python 배포 파일",
  "description":"EGG 파일 형식과 EGG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## .EGG 파일이란?

Python Egg라고도 하는 EGG 파일은 이전 배포 형식의 Python 배포입니다. 확장자가 .egg인 [ZIP](/ko/compression/zip/) 압축 아카이브이며 배포에 대한 메타 정보와 함께 Python 응용 프로그램의 소스 파일을 포함합니다. EGG 파일은 Windows 실행 [EXE](/ko/executable/exe/) 파일의 대안이지만 플랫폼 간입니다. Python 배포판의 이 이전 형식은 2010년 초에 새로운 Wheel(WHL) 파일 형식으로 대체되었습니다.

## EGG 파일 형식

EGG 파일은 압축된 ZIP 아카이브로 저장됩니다. 즉, .egg 확장자를 .zip으로 바꾸면 Corel WinZIP, Microsoft Explorer 또는 RARLAB WinRAR와 같은 표준 압축 해제 유틸리티로 열 수 있습니다.

EGG 파일은 Python에서 제공하는 **distutils** 패키지를 사용하여 생성할 수 있습니다. EGG 파일을 만들고 열 수 있는 또 다른 도구는 **SetupTools**입니다. EGG 파일은 **easy_install**을 사용하여 패키지로 설치할 수 있습니다.

`참고 - EGG 파일 형식은 더 이상 사용되지 않으며 새로운 휠 WHL 파일 형식을 사용합니다.`

## 참조 ##

* [파이썬 EGG](https://python101.pythonlibrary.org/chapter38_eggs.html)

