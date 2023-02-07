{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"GCF 파일을 만들고 열 수 있는 GCF 파일 형식 및 API에 대해 알아보세요.",
  "title" :"GCF 파일 - 나데오 게임 GCF 형식",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## .GCF 파일이란?

.gcf 파일은 Steam 게임 플랫폼에서 사용하는 게임 캐시 파일입니다. 여기에는 텍스처, 모델 및 게임에서 사용하는 기타 파일과 같은 게임 데이터가 포함됩니다. 이러한 파일은 사용자의 컴퓨터에 저장되며 게임을 업데이트하거나 설치할 때 다운로드해야 하는 데이터의 양을 줄이는 데 사용됩니다. .gcf 파일은 게임 설치의 백업을 만들거나 컴퓨터 간에 게임을 전송하는 데에도 사용할 수 있습니다.

GCF 파일은 오픈 소스 C++ 프로그래밍 라이브러리인 [HLLib]((https://developer.valvesoftware.com/wiki/HLLib))에서 읽고 쓸 수 있습니다.

## GCF 파일 형식

GCF 파일은 바이너리 파일로 디스크에 저장됩니다. GCF는 원래 Grid Cache File(Steam의 초기 코드명은 Grid)의 약어로 사용되었지만 나중에는 Game Cache File로 사용되었습니다. GCF 파일은 Steam 게임을 저장하는 아카이브 파일입니다. 모든 공식 콘텐츠는 GCF 파일로 다운로드됩니다. GCF 파일은 게임 간에 공유할 수도 있습니다.

참고: GCF는 [VPK 파일 형식](/ko/game/vpk/)의 전신입니다.
## 참조

* [밸브 소프트웨어](https://www.valvesoftware.com/en/)
* [GCF 파일 형식](https://developer.valvesoftware.com/wiki/GCF)
* [HLLib - GCF 파일 읽기를 위한 오픈 소스 C++ 프로그래밍 라이브러리](https://developer.valvesoftware.com/wiki/HLLib)

