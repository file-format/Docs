{
  "date" : "2020-11-11",
  "keywords" :[ "NSF", "확장자", "파일", "파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일 형식", "데이터베이스 파일" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NSF 파일을 생성하고 열 수 있는 NSF 파일 형식과 API에 대해 알아보세요.",
  "title" :"NSF 파일 형식 - Lotus Notes 데이터베이스 형식",
  "linktitle" : "NSF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## .NSF 파일이란?

.nsf(Notes Storage Facility) 확장자를 가진 파일은 이전에 Lotus Notes로 알려진 [IBM Notes 소프트웨어](https://en.wikipedia.org/wiki/HCL_Domino)에서 사용되는 데이터베이스 파일 형식입니다. 이메일, 약속, 문서, 양식 및 보기와 같은 다양한 종류의 개체를 저장하는 스키마를 정의합니다. 이 모든 정보는 PST/OST 파일과 유사한 비즈니스 협업을 위한 단일 NSF 파일에 포함됩니다. NSF 파일을 열 수 있는 일부 응용 프로그램에는 IBM Lotus Notes 및 IBM Domino가 있습니다.

## NSF 파일 형식 사양

NSF 파일은 본질적으로 바이너리이며 해당 사양은 [Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%)에서 Joachim Metz가 제공합니다. 20file%20format.asciidoc). 이러한 세부 정보에 따라 NSF 파일은 다음으로 구성됩니다.

* 파일 헤더
* 데이터베이스 헤더

또한 다음으로 구성됩니다.

* 슈퍼블록
* 버킷 설명자 블록
* 비트맵
* 레코드 재배치 벡터 버킷
* 요약 버킷
* 비요약 버킷


### NSF 파일 헤더

NSF 파일 헤더의 크기는 6바이트입니다. 구성:

|오프셋|크기|값|설명|
---|---|---|---|
0|2|0x1a 0x00|서명|
2|4| |데이터베이스 헤더 크기|

### 데이터베이스 헤더

NSD 데이터베이스 헤더에는 다음과 같은 확인된 값이 포함되어 있습니다.

* 데이터베이스 정보
* 데이터베이스 식별자(DBID)
* 복제 정보
* 데이터베이스 정보 버퍼 플래그
* 제목
* 카테고리
* 수업
* 디자인 클래스(템플릿 이름)
* 특수 메모 식별자
* 패딩
* 데이터베이스 정보 2
* 데이터베이스 정보 3
* 데이터베이스 정보 4
* 데이터베이스 정보 5
* 패딩
* 데이터베이스 인스턴스 식별자(DBIID)
* 복제 기록

## 참고문헌

* [NSF 형식 - Github](https://github.com/libyal/libnsfdb/blob/main/documentation/Notes%20Storage%20Facility%20(NSF)%20database%20file%20format.asciidoc)

