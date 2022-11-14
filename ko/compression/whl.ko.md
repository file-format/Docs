{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL 파일 형식 - Python 휠 패키지 파일",
  "description":"WHL 파일 형식과 WHL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## .WHL 파일이란?

WHL(Wheel) 파일은 Python의 휠 형식으로 저장된 배포 패키지 파일입니다. Python 배포판의 표준 형식 설치이며 설치에 필요한 모든 파일과 메타데이터가 포함되어 있습니다. WHL 파일에는 이 휠 파일에서 지원하는 Python 버전 및 플랫폼에 대한 정보도 포함되어 있습니다. [MSI](/ko/executable/msi/) 설치 파일과 유사하게 WHL 파일 형식은 소스 배포판을 구축하지 않고도 설치 패키지를 실행할 수 있는 즉시 설치할 수 있는 형식입니다.

## WHL 파일 형식

WHL 파일 형식은 패키지 설치를 위해 설치 프로그램이 필요로 하는 모든 설치 파일과 메타데이터가 포함된 [ZIP](/ko/compression/zip/)(.zip) 아카이브입니다. 이러한 WHL 파일은 압축 해제 옵션이나 WinZIP 및 WinRAR와 같은 표준 압축 해제 소프트웨어 응용 프로그램을 사용하여 추출할 수 있습니다.

### WHL 파일 이름 규칙

WHL 파일은 다음 규칙에 따라 이름이 지정됩니다.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

WHL 파일 이름의 예는 다음과 같습니다.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* '암호화'는 패키지 이름입니다.
* `2.9.2`는 암호화의 패키지 버전입니다. 버전은 2.9.2, 3.4 또는 3.9.0.a3과 같은 PEP 440 호환 문자열입니다.
* `cp35`는 Python 태그이며 휠이 요구하는 Python 구현 및 버전을 나타냅니다.
* 'abi3'은 ABI 태그입니다. ABI는 응용 프로그램 바이너리 인터페이스를 나타냅니다.
* `macosx_10_9_x86_64`는 플랫폼 태그로, 꽤 많이 나옵니다.

## 참고문헌

* [파이썬 휠이란 무엇이며 왜 주의해야 하나요?](https://realpython.com/python-wheels/)
* [파이썬 휠](https://pypi.org/project/wheel/)

