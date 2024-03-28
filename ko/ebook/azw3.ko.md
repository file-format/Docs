{
  "date" : "2019-12-12",
  "keywords" :[ "KF8", "확장자", "파일", "형식", "전자책", "킨들 파일 형식", "AZW3 파일 구조" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"AZW3 파일 형식과 AZW3 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"AZW3 파일이란 무엇입니까?",
  "linktitle" : "AZW3",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-06-04"
}

## .AZW3 파일이란?

Kindle 형식 8(**KF8**)이라고도 하는 AZW3은 Amazon Kindle 장치용으로 개발된 [AZW](/ko/ebook/azw/) 전자책 디지털 파일 형식의 수정된 버전입니다. 형식은 이전 AZW 파일에 대한 개선 사항이며 [MOBI](/ko/ebook/mobi/) 및 AZW와 같은 상위 파일 형식에 대한 이전 버전과의 호환성이 있는 Kindle Fire 장치에서만 사용됩니다. Amazon은 최신 Kindle 장치에서 사용되는 KF8 이후에 KFX(KF 버전 10) 형식을 도입했습니다. AZW3 파일에는 인터넷 미디어 유형이 application/vnd.amazon.mobi8-ebook입니다. AZW3 파일은 [PDF](/ko/pdf/), [EPUB](/ko/ebook/epub/), [AZW](/ko/ebook/azw/), [DOCX](/ko/word-processing/docx/) 및 [RTF](/ko/word-processing/rtf/).

## AZ3/KF8 파일 형식 ##

KF8 파일은 본질적으로 바이너리이며 MOBI 파일 형식의 구조를 PDB 파일로 유지합니다. 앞서 언급했듯이 KF8 파일은 MOBI와 최신 KF8 버전의 EPUB로 구성될 수 있습니다. 형식의 내부 세부 정보는 [Kindle Unpack](https://github.com/kevinhendricks/KindleUnpack)에 의해 디코딩되었으며, 이는 최종 컴파일된 데이터베이스를 구문 분석하고 MOBI 또는 AZW 소스 파일을 추출하는 Python 스크립트입니다. AZW3(KF8) 파일은 EPUB에 대한 이전 버전과도 호환되는 EPUB3 버전을 대상으로 합니다. KF8은 EPUB 파일을 컴파일하고 PDB 파일 형식을 기반으로 바이너리 구조를 생성합니다.

## 참조 ##

* [KF8 - 위키피디아 작성](https://en.wikipedia.org/wiki/Kindle_File_Format)
* [킨들 언팩](https://github.com/kevinhendricks/KindleUnpack)

