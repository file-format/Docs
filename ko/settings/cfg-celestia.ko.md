{
"날짜": "2023-09-27",
  "keywords": [
"cfg",
"cfg 파일",
"cfg celestia 구성 파일",
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
"title": "CFG 파일 형식 - Celestia 구성 파일",
  "description":"CFG Celestia 구성 파일 형식과 CFG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
"linktitle": "CFG 셀레스티아",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
"parent": "설정"
}
},
"lastmod": "2023-09-27"
}

## .CFG 파일이란?

Celestia 구성 파일은 3D 우주 시뮬레이션 프로그램인 Celestia에서 사용하는 일반 텍스트 파일입니다. 이러한 파일은 Celestia의 작동 방식, 표시되는 천체 및 프로그램 표시 방식을 사용자 정의하는 데 중요합니다. 그러나 부적절한 변경으로 인해 Celestia의 로딩 프로세스가 중단되어 올바르게 실행되지 않을 수 있으므로 이러한 파일을 편집할 때는 세심한 주의가 필요합니다.

## 셀레스티아

Celestia는 사용자가 매우 현실적이고 대화형 방식으로 우주를 탐색하고 시각화할 수 있는 무료 오픈 소스 3D 천문학 시뮬레이션 소프트웨어입니다. Chris Laurel이 개발했으며 2000년대 초반에 처음 출시되었습니다. Celestia는 Windows, macOS 및 Linux 운영 체제에서 사용할 수 있습니다.

Celestia의 주요 기능과 측면은 다음과 같습니다.

- **현실적인 3D 시각화:** Celestia는 태양계는 물론 별, 은하 및 기타 천체를 상세하고 정확하게 표현합니다. 고품질 3D 모델과 텍스처를 사용하여 시각적으로 몰입감 있는 경험을 선사합니다.

- **광범위한 천체 데이터베이스:** 이 소프트웨어에는 별, 행성, 달, 소행성, 혜성 및 우주선을 포함하여 알려진 천체에 대한 방대한 내장 데이터베이스가 함께 제공됩니다. 사용자는 이러한 개체를 쉽게 찾고 탐색할 수 있습니다.

- **과학적 정확성:** Celestia는 시각화 도구이지만 사용 가능한 과학적 데이터를 기반으로 천체 물체와 현상을 최대한 정확하게 표현하는 것을 목표로 합니다.

## Celestia에서 사용하는 파일 형식

Celestia는 3D 천문학 시뮬레이션의 다양한 측면에 다양한 파일 형식을 활용합니다. Celestia에서 사용하는 주요 파일 형식은 다음과 같습니다.

1. **구성 파일(.cel)**
- *설명*: 사용자가 Celestia의 동작, 모양 및 콘텐츠를 사용자 정의할 수 있는 일반 텍스트 파일입니다.
- *목적*: 설정 사용자 정의, 위치 정의, 천체 지정.

2. **3D 모델 및 메시**
- *형식*: [.3ds](/ko/3d/3ds/), [.obj](/ko/3d/obj/), [.dae](/ko/3d/dae/), .ac
- *설명*: 천체 및 우주선 렌더링에 사용되는 지원되는 3D 모델 파일 형식입니다.
- *목적*: Celestia 내에서 3D 개체를 표시합니다.

3. **텍스처 파일**
- *형식*: [.jpg](/ko/image/jpeg/), [.png](/ko/image/png/), [.dds](/ko/image/dds/)
- *설명*: 이 파일은 천체의 표면 질감을 제공합니다.
- *목적*: 사실적인 외관을 위해 텍스처를 3D 모델에 매핑합니다.

4. **별 카탈로그 및 데이터 파일**
- *형식*: 사용자 정의 형식, [.csv](/ko/spreadsheet/csv/), [.tsv](/ko/spreadsheet/tsv/)
- *설명*: 정확한 시뮬레이션을 보장하기 위해 별과 기타 천체를 나타내는 데 사용되는 데이터 파일입니다.
- *목적*: 천체 물체를 정확하게 표현합니다.

5. **텍스처 큐브 맵**
- *설명*: 큐브 맵은 은하와 같이 멀리 떨어져 있는 천체의 모습을 시뮬레이션하는 데 사용됩니다.
- *목적*: 사실적인 질감으로 멀리 있는 물체를 렌더링합니다.

6. **스크립트 파일**
- *설명*: 이 파일에는 Celestia의 스크립팅 언어로 작성된 사용자 정의 스크립트가 포함되어 있습니다.
- *목적*: 사용자가 Celestia의 세계 내에서 동적 이벤트와 애니메이션을 만들 수 있도록 합니다.

## Celestia 구성 파일

Celestia 구성 파일로 수행할 수 있는 작업에 대한 기본 개요는 다음과 같습니다.

1. **위치 설정**: 위도, 경도 및 고도 매개변수를 사용하여 지구상의 위치를 지정할 수 있습니다. 이를 통해 Celestia는 사용자 위치에서 밤하늘을 정확하게 표시할 수 있습니다.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **보기 옵션 사용자 정의:** 시야각, 시간 설정, 렌더링 기본 설정 등 다양한 보기 옵션을 조정할 수 있습니다.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **천체 개체 로드:** 별, 행성, 소행성, 우주선 등과 같은 천체 개체를 시뮬레이션에 추가할 수 있습니다. 각 개체는 해당 속성과 함께 구성 파일에 정의됩니다.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
}
}
```

4. **우주선 정의:** 위치, 방향, 3D 모델과 같은 매개변수를 지정하여 자신만의 가상 우주선을 만들거나 실제 우주선을 사용할 수 있습니다.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
}
}
```

5. **스크립트 생성:** Celestia의 사용자 정의 스크립팅 언어로 스크립트를 작성하여 동적 이벤트와 애니메이션을 생성할 수 있습니다.

## CFG 파일을 여는 방법?

CFG 파일을 열거나 참조하는 프로그램

- (Windows, Mac, Linux)용 Celestia(무료)

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
* [셀레스티아](https://en.wikipedia.org/wiki/Celestia)

