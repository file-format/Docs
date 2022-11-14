{
  "date" : "2021-02-25",
  "keywords": [ "ttc file", "ttc file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TTC - 트루타입 컬렉션 파일 형식",
  "description":"TrueType Collection(TTC) 파일은 여러 글꼴을 단일 파일로 결합합니다. Apple과 Microsoft 모두 Mac 및 Windows 운영 체제에서 TTF를 사용했습니다.",
  "linktitle" : "TTC",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## .TTC 파일이란?
TTC는 TrueType Collection이 True Type 형식의 확장으로 약칭됩니다. TTC 파일은 여러 글꼴 파일을 결합할 수 있습니다. 이러한 파일은 많은 글리프를 공유하는 여러 글꼴을 결합하는 데 유용합니다. Windows 2000 이전에는 TTC 파일이 중국어, 일본어 및 한국어 버전의 Windows에서 사용되었지만 이후에는 모든 지역에서 지원이 가능해졌습니다.


## 글꼴 모음 파일의 구조
TTC 파일은 TTC 헤더 테이블, 테이블 디렉토리 및 여러 OpenType 테이블로 구성됩니다. TTC 헤더는 파일 시작 부분에서 찾아야 합니다. 각 글꼴에 대한 완전한 테이블 디렉토리가 있어야 합니다. TableDirectory 형식은 비컬렉션 파일에 있는 것과 유사해야 합니다. TTC 파일 내의 모든 디렉토리에 있는 테이블 수는 TTC 파일의 시작 부분에서 계산됩니다.
TTC 파일의 테이블은 해당 글꼴의 테이블 디렉토리를 통해 참조됩니다. 일부 OpenType 테이블은 TTC에 추가된 각 글꼴에 대해 한 번씩 여러 번 나타나야 합니다. 다른 테이블은 TTC 파일의 여러 글꼴에서 공유할 수 있습니다.

### TTC 헤더
지금까지 두 가지 버전의 TTC 헤더 테이블을 사용할 수 있습니다.
- 버전 1.0은 디지털 서명이 없는 TTC 파일에 사용됩니다.
- 버전 2.0은 디지털 서명이 있거나 없는 TTC 파일에 사용할 수 있습니다.
다음은 두 버전의 TTC 헤더 테이블입니다.

**TTC 헤더 버전 1.0:**

|유형|이름|설명|
---|---|---|
|TAG|ttcTag|글꼴 모음 ID 문자열: 'ttcf'(CFF 또는 CFF2 윤곽선 및 TrueType 윤곽선이 있는 글꼴에 사용됨)|
|uint16|majorVersion|TTC 헤더의 주 버전, = 1.|
|uint16|minorVersion|TTC 헤더의 부 버전, = 0.|
|uint32|numFonts|TTC의 글꼴 수|
|Offset32|tableDirectoryOffsets[numFonts]|파일 시작 부분에서 각 글꼴에 대한 TableDirectory에 대한 오프셋 배열|

**TTC 헤더 버전 2.0:**

|유형|이름|설명|
---|---|---|
|TAG|ttcTag |글꼴 모음 ID 문자열: 'ttcf'|
|uint16| majorVersion |TTC 헤더의 주 버전, = 2.|
|uint16| minorVersion |TTC 헤더의 부 버전, = 0.|
|uint32| numFonts |TTC의 글꼴 수|
|오프셋32| tableDirectoryOffsets[numFonts] |파일 시작 부분에서 각 글꼴에 대한 TableDirectory에 대한 오프셋 배열|
|uint32| dsigTag |DSIG 테이블이 존재함을 나타내는 태그, 0x44534947('DSIG')(서명이 없으면 null)|
|uint32| dsigLength |DSIG 테이블의 길이(바이트)(서명이 없으면 null)|
|uint32| dsigOffset |TTC 파일의 시작 부분에서 DSIG 테이블의 오프셋(바이트 단위)(서명이 없으면 null)|

## 참고문헌
* [오픈타입 글꼴 파일](https://docs.microsoft.com/en-us/typography/opentype/spec/otff)
* [트루타입(위키피디아)](https://en.wikipedia.org/wiki/TrueType)

