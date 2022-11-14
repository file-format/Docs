{
  "date" : "2019-12-12",
  "keywords" :[ "LRF", "파일", "확장자", "포맷", "eBook", "디지털 북"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"LRF 파일을 만들고 열 수 있는 LRF 파일 형식과 API에 대해 알아보세요.",
  "title" :"LRF 파일 형식 - 소니 휴대용 리더 파일",
  "linktitle" : "LRF",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2019-12-12"
}

## .LRF 파일이란?

확장자가 .lrf인 파일은 텍스트, 이미지 및 페이지 매김 데이터를 포함하여 Sony BBeB용 데이터가 포함된 BBeB(광대역 eBook) 파일입니다. 파일은 헤더, 지정된 수의 개체 및 개체 색인을 포함하는 압축된 이진 형식으로 저장됩니다. LRF 및 LRX 파일은 사용 가능한 두 가지 BBeB 책 형식을 포함합니다. LRF 파일은 암호화되지 않으며 [LRX](/ko/ebook/lrf/) 파일에서 컴파일할 수 있습니다. LRF 파일은 PDF 및 HTML을 포함한 여러 다른 파일 형식에서 변환할 수 있습니다. 컴퓨터에서 LRF 파일을 열 수 없으면 LRF 파일을 열거나 편집하기 위한 소프트웨어가 설치되어 있지 않을 수 있습니다. LRF 파일을 열 수 있는 프로그램은 Windows용 Calibre, BookDesigner, Makelrf 및 Canon Book Creator, Linux용 Calibre, Calibre 및 Macintosh용 Sony Reader입니다.

## 약력

LRF 파일 형식은 [inXile 엔터테인먼트](https://en.wikipedia.org/wiki/InXile_Entertainment)의 Line Rider와 가장 먼저 연관되어 있습니다. Line Rider는 인터넷 물리학 장난감으로 2006년 9월 슬로베니아 대학생 Boštjan Čadež가 발명했습니다. Sony 브랜드 eBook eReader(예: Sony PRS-500 리더 및 Sony Librie)는 문서 및 텍스트에 LRF 파일 확장자를 사용합니다. 이 독점 파일 유형은 이제 관련 LRS 및 LRX 파일과 함께 더 이상 사용되지 않습니다. 이 세 가지 파일 형식은 2010년 Sony가 EPUB 형식으로 전자책을 판매하기 시작하면서 중단된 BroadBand eBook(BBeB)을 구성했습니다.

## LRF 파일 형식

LRF 파일 형식에 대한 자세한 사양은 [웹 아카이브](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)에서 확인할 수 있습니다. LRF 파일은 다음으로 구성됩니다.
* 헤더
* 개체의 수
* 객체 인덱스.

이 모든 값은 Intel(LSB 우선) 순서입니다.

### LRF 헤더

|오프셋(16진수) |크기(바이트) |이름/의미| 예시 값|
---|---|---|---|
|0 |8| LRF 서명| 4C 00 52 00 46 00 00 00 = 유니코드의 "LRF"|
|8 |2| 버전?| 대부분의 파일에서 999|
|A |2| "의사 암호화" |키 바이트 48|
|0C |4| 루트 개체 ID| 0x0044|
|10 |8| 개체 수 |342|
|18 |8| 개체 인덱스 오프셋| 0x00093440|
|20 |4| 알 수 없음| 0|
|24 |1| 깃발| (16 - 뒤에서 앞으로, 1 = 앞에서 뒤로) 16|
|25 |1| 알 수 없음 |(패딩?) 0|
|26 |2| 알 수 없음| 1600|
|28 |2| 알 수 없음| (패딩?) 0|
|2A |2| 키?| 600|
|2C |2| 너비?| 800|
|2E |1| 알 수 없음| 24|
|2층 |1| 알 수 없음 |(패딩?) 0|
|30 |0x14| 알 수 없음| 0|
|44 |4| PlaneStream(0x1E) 개체의 개체 ID만 | 0x0042|
|48 |4| 알 수 없음 |0x1536|
|4C |2| XMLCompSize| 0x035C|


## 참고문헌

* [LRF 파일 형식](https://web.archive.org/web/20110809071744/http://www.sven.de/librie/Librie/LrfFormat)
* [BBeB - 위키피디아 작성](https://en.wikipedia.org/wiki/BBeB)

