{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"OSZ 파일을 만들고 열 수 있는 OSZ 파일 형식 및 API에 대해 알아보십시오.",
  "title" :"OSZ 파일 - osu! 비트맵 파일 형식",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## .OSZ 파일이란?

OSZ 파일은 리듬 게임 osu!에서 사용하는 압축 파일 형식입니다. 비트맵 데이터를 저장합니다. 비트맵은 기본적으로 게임의 레벨이며 여기에는 노래, 비트 타이밍, 게임 화면의 히트 오브젝트 배치와 같은 정보가 포함됩니다. OSZ 파일을 사용하면 비트맵을 쉽게 배포할 수 있으며 일반적으로 인터넷에서 다운로드하여 게임으로 가져옵니다. OSU! 또한 게임 리플레이 파일인 [OSR](/ko/game/osr/) 파일 형식을 가지고 있으며 게임 플레이어가 다시 플레이할 수 있습니다.

**OSR 파일 형식의 MIME 유형:** x-osu-replay

## OSZ 파일 형식

OSZ 파일 형식의 내부 파일 형식 세부 정보는 공개적으로 사용할 수 없습니다. 여기에는 [ZIP](/ko/compression/zip/) 압축 데이터가 포함되어 있어 음악을 재생하고, 그래픽을 표시하고, 플레이어가 게임과 상호 작용해야 하는 이벤트에 대한 플레이어를 표시하는 정보가 포함되어 있습니다.

## OSZ 파일을 만드는 방법?

OSU! [OSZ 생성](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files) 에 대한 자세한 지침이 있습니다.
및 OSK 파일. OSU!를 사용하여 OSZ 파일을 생성하려면 다음 단계를 사용할 수 있습니다.

1. 편집기를 통해 비트맵을 엽니다.
1. 상단 메뉴에서 파일 > 패키지 내보내기...를 선택합니다.
1. .osz 아카이브는 osu! 내부의 Exports 폴더에 저장됩니다. 폴더.

## 참조

* [오쓰! 리듬게임](https://osu.ppy.sh/home)
