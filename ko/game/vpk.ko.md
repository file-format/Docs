{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"VPK 파일을 만들고 열 수 있는 언리얼 스태틱 메시 VPK 파일 형식 및 API에 대해 알아보세요.",
  "title" :"VPK 파일 - 언리얼 스태틱 메시 파일",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## .VPK 파일이란?

.vpk 파일은 Valve Corporation에서 개발한 게임 엔진인 **Source Engine**에서 사용하는 파일 형식입니다. VPK 파일은 모델, 텍스처 및 사운드와 같은 게임 콘텐츠를 패키징하는 데 사용되며 일반적으로 Team Fortress 2, Left 4 Dead 및 Counter-Strike: Global Offensive와 같은 게임에서 사용됩니다. GCFScape 및 VPK 도구와 같은 다양한 도구를 사용하여 파일을 열고 추출할 수 있습니다.

## VPK 파일 형식 - 추가 정보

VPK 파일은 바이너리 파일로 디스크에 저장됩니다. 단일 vpk 파일은 VPK 패키지의 일부이거나 독립적인 원시 VPK 파일로 작동할 수 있습니다. VPK 파일에 저장할 수 있는 정보에는 지도, 자료, 게임 콘텐츠, 안무 장면 등이 있습니다.

### VPK 파일을 만드는 방법?

사용 가능한 도구에 따라 .vpk 파일을 만드는 방법에는 여러 가지가 있습니다.

1. `VPK 도구 사용:` VPK 파일을 만들고 추출하는 데 사용할 수 있는 명령줄 도구입니다. 다음 명령을 사용하여 VPK 파일을 만들 수 있습니다.
```
"vpk.exe -M <directory> <output_file.vpk>"
```
그러면 지정된 디렉토리에서 VPK 파일이 생성되고 지정된 출력 파일로 저장됩니다.

1. `Hammer Editor 사용:` Hammer Editor는 Source SDK에 포함된 도구로 Source 엔진을 사용하는 게임의 레벨을 만들고 편집하는 데 사용할 수 있습니다. 또한 "파일 시스템" 탭에서 폴더를 마우스 오른쪽 버튼으로 클릭하고 "Create VPK"를 선택하여 VPK 파일을 생성하는 기능도 포함합니다.

1. `Valve의 VPK 크리에이터 사용:` 게임 콘텐츠를 패키징하고 배포하는 데 사용되는 Valve에서 개발한 도구입니다. 이 도구는 VPK 파일을 만드는 데 사용할 수 있으며 VPK 파일을 만드는 공식 도구이기도 합니다.

## 참조

* [밸브 소프트웨어](https://www.valvesoftware.com/en/)
* [VPK 개발자 리소스](https://developer.valvesoftware.com/wiki/GCF)

