{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSU 파일을 만들고 열 수 있는 OSU 파일 형식 및 API에 대해 알아보세요.",
  "title" :"OSU 파일 - Osu! 스크립트 파일 형식",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## .OSU 파일이란?

OSU 파일은 osu를 위해 작성된 게임 스크립트입니다! 리듬게임. 여기에는 난이도, 재생할 노래, 플레이어가 음악과 동기화해야 하는 히트 오브젝트의 타이밍과 같이 게임에서 사용되는 비트맵에 대한 정보가 포함됩니다. 이를 통해 리듬 게임 플레이어는 맞춤형 챌린지를 개발하고 게임 커뮤니티와 공유할 수 있습니다.

**OSR 파일 형식의 MIME 유형:** x-osu-beatmap

## OSU 파일 형식

OSU 파일은 일반 텍스트 파일로 디스크에 저장되며 그 구조는 다음을 통해 [OSU 파일 형식](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)에 매우 명확하게 정의됩니다. 오스!.

### OSU 파일의 섹션

일반적인 OSU 파일에는 다음 섹션이 있습니다.

|섹션 |설명 |콘텐츠 유형|
---|---|---|
|[일반]| 비트맵에 대한 일반 정보| 키: 값 쌍|
|[편집자]| 비트맵 편집기에 대한 저장된 설정| 키: 값 쌍|
|[Metadata] |비트맵을 식별하는 데 사용되는 정보| 키:값 쌍|
|[난이도] |난이도 설정| 키:값 쌍|
|[이벤트]| 비트맵 및 스토리보드 그래픽 이벤트| 쉼표로 구분된 목록|
|[타이밍 포인트]| 타이밍 및 제어 포인트| 쉼표로 구분된 목록|
|[색상]| 콤보 및 스킨 색상| 키 : 값 쌍|
|[히트 오브젝트]| 히트 오브젝트| 쉼표로 구분된 목록|

## 참조

* [오쓰! 리듬게임](https://osu.ppy.sh/home)
* [OSU 파일 형식](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)

