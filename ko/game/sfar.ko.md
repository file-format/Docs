{
  "date" : "2021-10-20",
  "keywords" :[ "sfar 파일", "sfar 파일 형식", "sfar 파일이란", "파일", "sfar 예제", "Mass Effect 3 DLC 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"SFAR 파일을 만들고 열 수 있는 Mass Effect 3 SFAR 파일 형식 및 API에 대해 알아보세요.",
  "title" :"SFAR - 매스 이펙트 3 DLC 파일",
  "linktitle" : "SFAR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## .SFAR 파일이란?

확장자가 .sfar인 파일은 Mass Effect 3에서 DLC(다운로드 가능한 콘텐츠)를 압축된 독점 아카이브에 저장하는 데 사용하는 게임 데이터 파일입니다. Mass Effect 3는 최고의 게임 개발 회사인 Electronic Arts에서 만든 게임입니다. SFAR 파일에 저장된 DLC 콘텐츠는 추가 콘텐츠 및 기능으로 게임을 확장하는 데 사용됩니다.

## SFAR 파일 형식 - 추가 정보

SFAR 파일은 바이너리 파일 형식의 압축 아카이브 파일로 저장/저장됩니다. 이들은 콘텐츠를 압축하기 위해 LZX 및 LZMA 압축 알고리즘을 모두 사용합니다. SFAR 파일은 ME3 Explorer와 함께 제공되는 DLC 편집기를 사용하여 열 수 있습니다. SFAR 외에도 DLC Editor는 [PCC](/ko/game/pcc/)와 같은 다른 게임 파일을 추출할 수 있습니다.

## SFAR 파일 형식 사양

SFAR 파일은 다음 네 가지 주요 청크로 나뉩니다.

### SFAR 헤더

SFF 헤더에는 파일을 구성하는 다양한 청크에 대한 정보가 포함됩니다.

### SFAR 파일 테이블

SFAR 파일 테이블에는 각 항목의 길이가 30바이트인 파일 항목 목록이 포함되어 있습니다.

### 블록 크기 테이블

Block-Size는 각 항목의 길이가 2바이트인 여러 항목을 포함합니다. 이 값은 파일 테이블의 항목에 해당하는 블록 크기를 지정합니다.

### 블록

SFAR 파일의 블록 청크에는 SFAR 파일 내부의 데이터가 포함됩니다.

## 참고문헌

* [DLC SFAR 파일 형식 - 연구](https://www.tapatalk.com/groups/me3explorer/current-research-dlc-sfar-fileformat-t629.html)

