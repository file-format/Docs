{
  "date" : "2019-10-11",
  "keywords" :[ "pot 파일", "pot 파일 형식", "pot 파일이란", "file", "pot 예제", "pot 파일 확장자","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"POT - Microsoft PowerPOint 템플릿 파일 형식",
  "description":"POT 파일 형식과 POT 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "POT",
  "menu" : {
    "docs" : {
      "parent" : "presentation"
}
},
  "lastmod" : "2019-09-10"
}

## .POT 파일이란?

.POT 확장자를 가진 파일은 PowerPoint 97-2003 버전에서 만든 Microsoft PowerPoint 템플릿 파일을 나타냅니다. 이러한 버전의 Microsoft PowerPoint로 만든 파일은 상위 버전의 PowerPoint를 사용하여 Office OpenXML 파일 형식으로 만든 파일과 비교하여 이진 형식입니다. 따라서 생성된 파일을 사용하여 새 파일에 적용해야 하는 레이아웃 및 기타 설정이 동일한 프레젠테이션을 만들 수 있습니다. 이러한 설정에는 스타일, 배경, 색상 팔레트, 글꼴 및 기본값이 포함될 수 있습니다. 이러한 파일은 공식적으로 사용할 준비가 된 템플릿 파일을 만들기 위해 생성됩니다.

## 파일 형식 사양 ##

POT 파일 형식에 대한 파일 형식 사양은 Microsoft에서 개별적으로 제공하지 않습니다. 단, 템플릿 형식은 바이너리 [PPT](/ko/presentation/ppt/) 파일 형식과 동일하며 MS PowerPoint에서 열어서 편집할 수 있습니다. POT 파일은 다음과 같이 HEX 식별자로 식별됩니다.

```
D0 CF 11 E0 A1 B1 1A E1 00 00 00 00
```

POT 파일 형식과 관련된 MIME 유형은 다음과 같습니다.

* application/vnd.ms-powerpoint [공식]
* 응용 프로그램/mspowerpoint
* 응용 프로그램/x-mspowerpoint
* 응용 프로그램/파워포인트
* 응용 프로그램/x-파워포인트
* 응용 프로그램/x-dos_ms_powerpnt
* 응용 프로그램/냄비
* 응용 프로그램/x-soffic

## 참조 ##

* [PPT 파일 형식 사양](https://msdn.microsoft.com/en-us/library/office/cc313106(v#office.12).aspx)
* [[MS-OSHARED]: Office 공통 데이터 유형 및 개체 구조](https://msdn.microsoft.com/en-us/library/office/cc313156(v#office.12).aspx)
* [[MS-OFFCRYPTO] - Office 문서 암호화 구조](https://msdn.microsoft.com/en-us/library/office/cc313071(v#office.12).aspx)
* [파워포인트 파일 형식](https://en.wikipedia.org/wiki/Microsoft_PowerPoint#File_formats)

