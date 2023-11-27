{
"날짜": "2023-09-27",
  "keywords": [
"cfg",
"cfg 파일",
"cfg wesnoth 마크업 언어 파일",
"cfg 파일이 무엇인가요?",
"cfg 파일을 여는 방법",
"파일",
"cfg 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "CFG 파일 형식 - Wesnoth 마크업 언어 파일",
  "description":"CFG Wesnoth 마크업 언어 파일 형식과 CFG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent" : "game"
}
},
"lastmod": "2023-09-27"
}

## .CFG 파일이란?

CFG 파일은 **"Wesnoth Markup Language"(WML)**라고도 알려져 있습니다. 턴제 전략 게임인 "Battle for Wesnoth" 게임에서 주로 사용되는 커스텀 마크업 언어입니다. WML은 시나리오, 캠페인, 유닛 등을 포함하여 게임의 다양한 측면을 정의하고 사용자 정의하는 데 사용됩니다. 이는 모더와 개발자가 게임용 콘텐츠를 만드는 방법입니다.

XML과 간단한 스크립팅의 조합과 유사한 형식으로 작성됩니다. 다음은 WML 파일에서 찾을 수 있는 몇 가지 공통 요소 및 구조에 대한 개요입니다.

1. **태그:** WML은 태그를 사용하여 게임의 다양한 요소를 정의합니다. 태그는 꺾쇠괄호로 묶여 있습니다. 예를 들어:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **속성:** 태그 내에서 속성을 정의하여 요소와 관련된 속성이나 값을 지정할 수 있습니다. 위의 예에서 "type"과 "hitpoints"는 속성입니다.
    










3. **배열 및 배열의 배열:** 데이터 배열은 물론 배열 배열을 만들어 유닛 목록, 지형 유형 또는 기타 게임 요소를 정의할 수 있습니다.
    










4. **조건문:** WML은 게임 흐름을 제어하기 위한 조건문을 지원합니다. 예를 들어:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **루프:** 루프를 사용하여 항목 목록을 반복하거나 작업을 반복적으로 수행할 수 있습니다.
    










6. **포함:** 콘텐츠를 구성하고 모듈화하기 위해 기본 WML 파일 내에 다른 WML 파일을 포함할 수 있습니다.
    










7. **이벤트 핸들러:** 게임에서 특정 이벤트가 발생할 때 작업을 트리거하는 이벤트 핸들러를 정의할 수 있습니다.
    











다음은 사용자 정의 단위를 정의하는 WML 파일의 간단한 예입니다.

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## 웨스노스 전투

"The Battle for Wesnoth"는 인기 있는 오픈 소스 턴제 전략 게임입니다. Mac, Windows, Linux 등을 포함한 다양한 플랫폼에서 사용할 수 있습니다. 헌신적인 자원봉사자 커뮤니티에 의해 개발된 이 게임은 깊고 매력적인 게임 플레이는 물론 풍부한 판타지 세계로 유명합니다.

"The Battle for Wesnoth"의 주요 특징은 다음과 같습니다.

1. **판타지 설정:** 게임은 인간, 엘프, 드워프, 오크 등 다양한 종족이 존재하는 판타지 세계를 배경으로 합니다. 게임의 지식과 스토리텔링은 게임 매력의 필수적인 부분입니다.
    










2. **턴 기반 전략:** 게임 플레이는 턴 기반으로, 플레이어는 육각형 격자에서 자신의 움직임을 계획하고 실행하는 데 시간을 투자합니다. 이는 전술적 전투와 전략적 의사결정을 결합합니다.
    










3. **캠페인:** 이 게임은 다양한 싱글 플레이어 캠페인을 제공하며 각 캠페인에는 고유한 스토리라인, 캐릭터, 도전 과제가 있습니다. 플레이어는 다양한 내러티브와 시나리오를 탐색할 수 있습니다.
    










4. **멀티플레이어:** "Wesnoth"는 온라인 멀티플레이어를 지원하여 플레이어가 전략적 전투에서 서로 경쟁할 수 있도록 합니다. 멀티플레이어 모드에는 협동 플레이와 경쟁 매치가 포함됩니다.

## CFG 파일을 여는 방법?

일반적으로 "The Battle for Wesnoth" 게임에 사용되는 WML(Wesnoth Markup Language)과 관련된 CFG 파일은 표준 텍스트 편집기를 사용하여 쉽게 편집할 수 있습니다. 이러한 파일에는 시나리오, 유닛, 캠페인 등 게임의 다양한 측면을 정의하는 WML로 작성된 사람이 읽을 수 있는 코드가 포함되어 있습니다.

모든 텍스트 편집기를 사용하여 CFG 파일을 수정할 수 있지만 Emacs 및 Vi와 같은 일부 고급 텍스트 편집기에는 WML 구문 강조 플러그인을 사용할 수 있습니다. 이러한 플러그인은 사용자가 WML 코드 내에서 다양한 요소와 구조를 쉽게 구별할 수 있도록 유용한 색상 구분 및 서식을 제공합니다.

CFG 파일을 열거나 참조하는 프로그램은 다음과 같습니다.

- The Battle for Wesnoth(무료) for (Windows, MAC, Linux)
- 마이크로소프트 메모장

## 기타 CFG 파일

**.cfg** 파일 확장자를 사용하는 다른 파일 형식은 다음과 같습니다.

**설정**
- [CFG - Celestia 구성 파일](/ko/settings/cfg-celestia/)
- [CFG - Citrix 서버 연결 파일](/ko/settings/cfg-citrix/)
- [CFG - MAME 구성 파일](/ko/settings/cfg-mame/)
- [CFG - LightWave 구성 파일](/ko/settings/cfg-lightwave/)

**게임**
- [CFG - Wesnoth 마크업 언어 파일](/ko/game/cfg-wesnoth/)
- [CFG - MUGEN 구성 파일](/ko/game/cfg-mugen/)
- [CFG - 소스 엔진 구성 파일](/ko/game/cfg-sourceengine/)

**시스템 및 기타**
- [CFG - CFG 파일](/ko/system/cfg/)
- [CFG - Cal3D 모델 구성 파일](/ko/misc/cfg-cal3d/)

## 참고자료
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
