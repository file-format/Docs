{
  "date" : "2021-08-27",
  "keywords" :[ "wsh 파일", "wsh 파일 형식", "wsh 파일이란", "파일", "wsh 예", "wsh 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"WSH 파일을 만들고 열 수 있는 WSH 파일 형식 및 API에 대해 알아보세요.",
  "title" :"WSH - Windows 스크립트 파일",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## .WSH 파일이란?
확장자가 .wsh인 파일에는 VB 또는 VBS 등과 같은 특정 프로그래밍 언어 스크립트에 대한 속성 및 매개변수가 포함되어 있습니다. WSH의 실제 필요는 특정 스크립트의 실행을 사용자 정의하는 데 사용하는 것입니다. 실행하려면 WScript 또는 CScript가 필요하며 둘 다 Windows 운영 체제에 포함되어 있습니다. WSH 파일은 처음에 Windows 95에서 제어판에 대해 구성 및 설치가 가능한 선택적 구성 요소로 설치 디스크에 제공된 다음 Windows 98의 기본 구성 요소로 제공되었습니다.

## WSH 파일 형식
WSH(Windows Script Host)는 관리, 로그온 스크립트, 일반 자동화 등 다양한 용도로 사용될 수 있습니다. WSH는 스크립트를 실행할 환경을 설정합니다. 적절한 스크립트 엔진을 호출하고 스크립트가 작업할 서비스 및 개체 집합을 할당합니다. 이러한 스크립트는 COM 개체 또는 명령줄 모드에서 GUI 모드로 실행할 수 있으므로 대화형 또는 비대화형 스크립트 모두에 대해 사용자에게 유연성을 제공합니다.

### 예
다음은 루트 WSH COM 개체 "WScript"를 사용하여 '확인' 버튼이 있는 메시지를 표시하는 일부 VBScript를 보여주는 매우 간단한 예입니다. 이 스크립트가 실행될 때 CScript 또는 WScript 엔진이 호출되고 런타임 환경이 설정됩니다.

```
WScript.Echo "Hello world"
WScript.Quit
```


## 참고문헌

* [Windows 스크립트 호스트 - Wikipedia 제공](https://en.wikipedia.org/wiki/Windows_Script_Host)



