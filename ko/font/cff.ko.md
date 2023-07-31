{
  "date" : "2020-08-20",
  "keywords" :[ "cff 파일", "cff 파일 형식", "cff 파일이란", "파일", "cff 예제", "cff 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF - 컴팩트 글꼴 파일 형식",
  "description":"CFF 파일 형식 및 CFF 파일을 만들고 여는 API에 대해 알아보세요.",
  "linktitle" : "CFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## .CFF 파일이란?

확장자가 .cff인 파일은 컴팩트 글꼴 형식이며 PostScript Type 1 또는 CIDFont라고도 합니다. CFF는 여러 글꼴을 FontSet이라는 단일 단위에 함께 저장하는 컨테이너 역할을 합니다. CFF 글꼴의 디자인은 프린터 환경에서 사용할 수 있는 형식의 추가 유연성과 확장성을 허용하는 PostScript 언어 코드를 포함할 수 있도록 합니다. CFF 글꼴 파일은 [Aspose.Font](https://products.aspose.com/font)와 같은 API를 사용하여 열고 변환할 수 있습니다.

## CFF 파일 형식

CFF 파일은 구조화된 데이터 레이아웃을 포함하고 정의된 데이터 유형, 헤더, 글리프 구성 및 테이블 사전을 포함하는 이진 파일입니다. 이에 대한 자세한 내용은 [컴팩트 글꼴 형식 사양](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)에서 확인할 수 있습니다.

### 데이터 레이아웃
CFF 파일 형식의 데이터 레이아웃은 다음과 같습니다.

|항목|댓글|
---|---|
|헤더|-|
|이름INDEX|–|
|상위 DICT 색인|–|
|문자열 인덱스|–|
|글로벌 하위 인덱스|–|
|인코딩–문자 집합|–|
|FDSelect|CIDFont만|
|CharStrings INDEX|글꼴당|
|글꼴 DICT INDEX|글꼴당, CIDF글꼴만|
|비공개 DICT|글꼴별|
|Local Subr INDEX|CIDFonts용 글꼴별 또는 개인별 DICT|
|저작권 및 상표권 고지|–|

### 데이터 유형

CFF 데이터 유형은 다음 표와 같습니다.

|이름|범위|설명|
---|---|---|
|Card8|0 –255|1바이트 부호 없는 숫자|
|Card16|0 – 65535|2바이트 부호 없는 숫자|
|오프셋|변함|1, 2, 3 또는 4바이트 오프셋(OffSize 필드로 지정)|
|OffSize|1–4|1바이트 부호 없는 숫자는 오프셋 필드의 크기를 지정합니다|
|SID|0 – 64999|2바이트 문자열 식별자|

### 헤더

이진 데이터는 다음 표에 표시된 형식의 헤더로 시작합니다.

|유형|이름|설명|
---|---|---|
|Card8|major|주 버전 포맷(1부터 시작)|
|Card8|부|부 버전 포맷(0부터 시작)|
|카드8|hdr크기| 헤더 크기(바이트)|
|OffSize|offSize|절대 오프셋(0) 크기|

## 참고문헌

* [컴팩트한 글꼴 형식 테이블](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
* [CFF 파일 형식](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
* [CFF2 차트셋](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

