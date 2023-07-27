{
  "date" : "2019-12-12",
  "keywords" :[ "LRX", "파일", "확장자", "포맷", "전자책", "디지털 북"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"LRX 파일 형식과 LRX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"LRX - Librie Reader 소스 파일 형식",
  "linktitle" : "LRX",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2020-11-04"
}

## .LRX 파일이란?

확장자가 .lrx인 파일은 BBeB(Sony Broadband eBook) 관련 파일입니다. 여기에는 이미지, 텍스트 및 페이지 매김 정보와 같은 데이터가 포함됩니다. BBeB 형식은 사용자가 eBook을 읽을 수 있는 모바일 장치인 Sony Portable Reader에서 사용됩니다. 그러나 2010년 7월부로 이 형식은 더 이상 사용되지 않으며 Sony는 이제 전자책에 [EPUB](/ko/ebook/epub/) 파일 형식을 사용합니다. LRX 파일을 열 수 있는 응용 프로그램에는 Windows와 Mac OS 모두에서 사용할 수 있는 Sony Reader가 있습니다.

## LRX 파일 형식

LRX 파일은 바이너리 파일 형식으로, 비암호화 형식인 [LRS](/ko/ebook/lrs/)와 달리 파일의 모든 내용이 암호화됩니다. 또 다른 관련 BBeB 파일 형식은 XML 기반이며 모든 텍스트 편집기에서 사람이 읽을 수 있는 LRS입니다. LRX 파일의 헤더에는 다음과 같은 정보가 포함되어 있습니다.

* 버전
* 루트 객체 식별
* 썸네일 이미지의 종류
* 수축된 데이터 값
* 난독화 키
* 방향 플래그 바인딩
* 디플레이션 후 데이터 크기

## 참고문헌

* [BBeB - 위키피디아 작성](https://en.wikipedia.org/wiki/BBeB)

