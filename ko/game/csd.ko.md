{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"CSD Steam 게임 데이터 백업 파일 형식 및 API에 대해 알아보세요.",
  "title" :"CSD 파일 형식 - Steam 게임 데이터 백업 파일",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## .CSD 파일이란?

CSD 파일은 **Valve** 게임을 다운로드하고 관리할 수 있는 게임 서비스 **Steam**에서 생성한 게임 백업 파일입니다. 삭제된 게임을 복원하는 데 사용할 수 있는 게임과 관련된 백업 데이터가 포함되어 있습니다. Steam은 게임이 Steam을 통해 다운로드, 설치 및 패치된 경우에만 CSD 파일에서 게임을 복원할 수 있습니다. CSD 파일에서 게임을 복원하려면 Steam → Gamesteam 백업 및 복원 옵션을 사용하여 파일을 선택하십시오.

## CSD 파일 형식 - 추가 정보

CSD 파일 형식의 내부 구조는 공개적으로 사용할 수 없으며 해당 파일 형식 사양은 개발자 참조용으로 사용할 수 없습니다. CSD 파일은 Steam 게임 파일 형식이기도 한 CSM 및 ISS 파일과 함께 제공됩니다.

### Steam 백업 파일은 어디에서 찾을 수 있나요?

전체 Steam 백업 파일은 다음 위치에서 찾을 수 있습니다.

* C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
* \cfg\ - 사용자 정의 구성 및 구성 스크립트
* \downloads\ - 멀티플레이어 게임을 위한 맞춤형 콘텐츠
* \maps\ - 멀티플레이어 게임 중에 설치되거나 다운로드된 사용자 지정 지도
* \materials\ - 사용자 정의 텍스처 및 스킨
* \SAVE\ - 싱글 플레이어 저장된 게임

단, 제3자 제작 게임의 위치는 다를 수 있으며 게임 개발자가 결정합니다.

### CSD 백업 파일에서 복원

Steam을 설치하고 올바른 Steam 계정에 로그인합니다(자세한 지침은 Steam 설치 참조).
* 스팀 실행
* Steam 애플리케이션의 왼쪽 상단 모서리에 있는 "Steam"을 클릭하십시오.
* "게임 백업 및 복원..." 선택
* "이전 백업 복원" 선택
* 게임의 백업 파일 위치로 이동
* 필요한 게임을 설치하려면 Steam 창을 계속 진행하세요.

## 참고문헌

* [Steam 백업 기능 사용하기](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

