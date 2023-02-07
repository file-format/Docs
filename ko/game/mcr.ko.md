{
  "date" : "2022-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"MCR 파일을 만들고 열 수 있는 MCR 파일 형식 및 API에 대해 알아보십시오.",
  "title" :"MCR - Minecraft 지역 파일 형식",
  "linktitle" : "MCR",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2022-12-14"
}

## .MCR 파일이란?

Minecraft MCR 파일 형식은 Minecraft에서 Minecraft World의 지형 청크를 저장하는 데 사용하는 데이터 형식입니다. 인기 있는 오픈 소스 게임 엔진인 Minecraft Forge의 개발자가 개발한 NBT(Named Binary Tag) 형식을 기반으로 합니다. MCR 파일 형식은 처음에 소개되었고 나중에 [MCA 파일 형식](/ko/game/mca/)으로 대체되었습니다.

## MCR 파일 형식

MCR 파일 형식은 각각 특정 유형의 데이터를 포함하는 일련의 명명된 이진 태그로 구성됩니다. 최상위 태그는 단일 게임 레벨에 대한 모든 데이터를 포함하는 "Level" 태그입니다. Level 태그 내에는 게임 세계에 대한 정보를 저장하는 "Data" 태그, 게임 세계에 대한 데이터를 저장하는 "Entities" 및 "TileEntities" 태그와 같이 다양한 유형의 데이터를 저장하는 몇 가지 다른 명명된 태그가 있습니다. 게임 개체와 타일 엔터티는 각각 세계에 있습니다.

## MCR 파일 형식 안에 무엇이 있습니까?

Minecraft MCR 파일 형식에서 영역은 게임 세계의 32x32 블록 영역입니다. MCR 형식은 데이터를 보다 효율적으로 관리하고 게임 레벨을 더 빠르게 로드하고 저장할 수 있도록 게임 세계를 지역으로 나눕니다. 각 지역은 별도의 파일에 저장되며 MCR 파일 형식은 좌표계를 사용하여 게임 세계 내에서 각 지역의 위치를 식별합니다. 영역의 좌표는 영역의 왼쪽 아래 모서리의 블록 좌표에 의해 결정됩니다. 예를 들어 좌표가 (-1,0)인 영역은 게임 세계의 원점에서 왼쪽으로 한 영역, 아래로 0 영역에 위치합니다.

## MCR 파일 형식 사양

MCR 파일 형식 사양은 공개적으로 사용할 수 있습니다. MCR 형식의 기반이 되는 NBT 형식의 사양은 Minecraft Forge 웹사이트에서 확인할 수 있습니다. 또한 [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format)에는 구조 및 지원하는 다양한 데이터 유형을 포함하여 MCR 파일 형식에 대한 자세한 정보도 있습니다.

### MCR 파일의 압축 데이터

Minecraft MCR 파일 형식은 압축을 지원합니다. MCR 파일 형식은 데이터를 압축된 형태로 저장할 수 있는 [NBT 형식](https://minecraft.fandom.com/wiki/NBT_format)을 기반으로 합니다. 이렇게 하면 MCR 파일의 크기를 줄이고 보다 효율적으로 전송하고 저장할 수 있습니다. 이는 플레이어가 다른 사람과 대규모 Minecraft World 지형 데이터를 공유할 수 있도록 하는 MCR 파일 형식의 중요한 기능입니다.

## 참조

* [마인크래프트용 월드 에디터](https://www.mcedit.net/)
* [Minecraft 소개](https://www.minecraft.net/en-us)
* [지역 파일 형식](https://minecraft.fandom.com/wiki/Region_file_format)
* [NBT 형식](https://minecraft.fandom.com/wiki/NBT_format)

