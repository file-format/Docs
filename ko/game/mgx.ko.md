{
  "date" : "2021-09-08",
  "keywords" :[ "mgx 파일", "mgx 파일 형식", "mgx 파일이란", "파일", "mgx 예제", "mgx 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Age of Empires 2 Expansion Replay MGX 파일 형식과 MGX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"MGX - Age of Empires 2 확장판 리플레이",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .MGX 파일이란?

확장자가 .mgx인 파일은 Age of Empires II 프로그램 내에서 재생할 수 있는 Age of Empires II: The Conquerors 게임의 녹화 파일입니다. 여기에는 사용자가 플레이한 캠페인의 전체 기록이 포함됩니다. Age of Empires II 프로그램 내에서 로드하고 재생할 수 있습니다. 게임을 다시 플레이하면 사용자가 캠페인을 위해 계획하고 플레이한 모든 이벤트와 시나리오가 표시됩니다.

## MGX 파일 형식 - 추가 정보

MGX 파일의 내부 파일 형식은 [Age of Empires 2: The Conquerors - Savegame 파일 형식 사양](https://github.com/stefan-kolb/aoc-mgx- 체재). 사양은 다음 섹션에서 세부 정보를 간략하게 설명합니다.

### 구조 정의

GPX 파일 형식의 구조 정의는 구조화된 바이너리 데이터를 읽고 쓰는 방법을 제공하는 [BinData Ruby Gem 선언](https://github.com/dmendel/bindata/wiki)을 기반으로 하는 것으로 믿어집니다. 이를 통해 프로그래머는 BinData에서 읽고 쓰는 이진 데이터의 형식을 지정할 수 있습니다.

### MGX 메시징

MGX 메시징은 두 가지 유형의 메시지를 기반으로 합니다.

* GAMESTART - 게임 시작 명령을 지정하며 현재까지 검증되지 않았습니다.
* 채팅 - 게임 내 채팅 메시지를 설명합니다. 플레이어와 게임 자체(Gaia) 모두 게임 내 메시지를 보낼 수 있습니다.

### 게임 플레이 액션

검색된 몇 가지 [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) 및 세부 정보가 있습니다.

## 참고문헌

* [Age of Empires 2: The Conquerors - Savegame 파일 형식 사양](https://github.com/stefan-kolb/aoc-mgx-format)

