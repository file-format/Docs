{
  "date" : "2021-09-08",
  "keywords" :[ "PCC 파일", "PCC 파일 형식", "PCC 파일이란", "파일", "PCC 예제", "PCC 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Mass Effect PCC 파일 형식과 PCC 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"PCC - 매스 이펙트 패키지 파일",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .PCC 파일이란?

.pcc가 있는 파일은 [매스 이펙트 게임](https://www.ea.com/games/mass-effect/mass-effect-3) 파일로, 모델, 텍스처, 방. Mass Effect 2와 3은 Unreal Engine 3 게임 엔진을 기반으로 한 최초의 슈팅 게임입니다. 게임은 처음에 [Bioware](https://www.bioware.com/about/)에 의해 개발되었으며 대부분의 게임 리소스를 독점 PCC 파일 형식으로 유지했습니다. Bioware는 선도적인 글로벌 인터랙티브 엔터테인먼트 퍼블리셔인 Electronic Arts에 인수되었습니다.

## PCC 파일 형식 - 추가 정보

PCC 파일에는 전체 파일 구성에 기여하는 압축 및/또는 비압축 구조가 포함되어 있습니다.

### 압축된 PCC 구조

압축된 PCC 파일은 청크로 분할된 테이블과 데이터로 구성됩니다. 각 청크에는 가변 수의 압축 블록이 포함됩니다.

* `Chunks Header` - 청크에 대한 정보를 포함하는 16바이트 공통 헤더입니다.
* `청크 헤더` - 블록 형식에 포함된 원시 압축 데이터에 대한 정보를 포함하는 16바이트 헤더입니다.

### 압축되지 않은 PCC 구조

압축되지 않은 PCC 파일은 다음 다섯 부분으로 나뉩니다.

* `Header` - PCC 파일의 구조에 대한 기본 정보를 담고 있습니다.
* `이름 테이블` - 가져오기 클래스, 내보내기 및 내보내기 속성을 포함하여 패키지 내에서 발견된 이름을 포함합니다.
* `Import Table` - PCC에서 가져온 모든 클래스와 개체를 포함합니다.
* `Export Table` - 패키지에 저장된 모든 객체를 포함합니다. 각 내보내기의 크기는 다를 수 있습니다.

## 참고문헌

* [Me3Explorer - PCC 파일 형식](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [매스 이펙트 게임](https://www.ea.com/games/mass-effect/mass-effect-3)
* [바이오웨어](https://www.bioware.com/about/)

