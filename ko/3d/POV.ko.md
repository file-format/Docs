
{
  "date": "2023-01-05",
  "keywords": [
"POV 파일",
"POV 파일 형식",
"POV 파일이 뭐야?",
"파일",
"포 예",
"POV 파일 확장자",
"확대",
"체재"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "POV 파일 형식과 POV 파일을 열고 생성할 수 있는 API에 대해 알아봅니다.",
  "title": "POV - 비전 파일의 지속성",
  "linktitle": "POV",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-po-kov"
}
},
  "lastmod": "2023-01-05"
}

## .POV 파일이란?

POV 파일은 POV-Ray 광선 추적 소프트웨어에 대한 지침이 포함된 일반 텍스트 파일입니다. 이러한 지침은 POV-Ray에 특정한 특수 스크립트 언어로 작성되었습니다. 3D 개체, 재료, 조명 및 장면의 모양을 정의하는 기타 속성을 포함하여 렌더링할 장면을 지정합니다. POV 파일은 POV-Ray에 특화된 특수 스크립팅 언어를 사용하며 복잡하고 상세한 3D 장면을 만드는 데 사용할 수 있습니다. POV 파일의 파일 확장자는 일반적으로 .pov 또는 .povray입니다. POV-Ray에서 POV 파일을 열면 소프트웨어는 파일의 지침을 읽고 이를 사용하여 장면의 렌더링된 이미지를 생성합니다.

.pov 파일은 아티스트와 디자이너가 영화, TV, 비디오 게임, 마케팅 자료 등 다양한 응용 프로그램에 대한 3D 그래픽과 애니메이션을 만드는 데 자주 사용됩니다.

## POV 파일 형식

**.pov 파일**은 일반적으로 장면에서 사용할 수 있는 미리 정의된 색상, 텍스처 및 기타 리소스의 라이브러리를 포함하는 데 사용되는 일련의 **#include** 문으로 시작됩니다. 그런 다음 파일은 일련의 블록을 사용하여 장면의 개체, 재료 및 기타 속성을 정의합니다. .pov 파일에 지정할 수 있는 다양한 유형의 개체, 재료 및 기타 속성이 있으며 루프 및 조건문을 사용하여 더 복잡하고 세부적인 장면을 만들 수 있습니다.

## POV용 소프트웨어 애플리케이션

.pov 파일 형식은 POV-Ray 광선 추적 소프트웨어에서 사용되므로 .pov 파일을 여는 기본 응용 프로그램은 POV-Ray 소프트웨어 자체입니다. POV-Ray의 최신 버전은 공식 웹사이트(https://www.povray.org/)에서 다운로드할 수 있습니다.

POV-Ray 외에도 .pov 파일을 열고 편집할 수 있는 다음과 같은 다양한 애플리케이션이 있습니다.

- BRL-CAD: .pov 파일을 가져오고 내보낼 수 있는 오픈 소스 3D 모델링 소프트웨어
- MeshLab: .pov 파일을 가져오고 내보낼 수 있는 3D 메쉬 처리 소프트웨어
- Blender: .pov 파일을 가져오고 내보낼 수 있는 인기 있는 오픈 소스 3D 그래픽 소프트웨어

.pov 파일을 열 수 있는 다른 소프트웨어 응용 프로그램도 있을 수 있으므로 위 응용 프로그램으로 .pov 파일을 열 수 없는 경우 파일 뷰어나 변환기 도구를 사용해 볼 수 있습니다.

## POV 예

예를 들어, 다음은 단일 파란색 원통이 있는 장면을 정의하는 샘플 .pov 파일입니다.

```
#include "colors.inc" 

// Declare the camera and specify its position and direction
camera {
  location <0, 0, -5>
  look_at <0, 0, 0>
}

// Declare a light source and specify its position and color
light_source {
  <5, 5, -5>
  color White
}

// Declare the cylinder object and specify its endpoints, radius, and material
cylinder {
  <0, 0, 0>, <0, 0, 1>, 0.5
  pigment { color Blue }
  finish { phong 1 }
}

```

이 예에서 카메라 블록은 장면에서 카메라의 위치와 방향을 지정하고, 'light_source' 블록은 광원을 선언하고 위치와 색상을 지정하며, 'cylinder' 블록은 원통 객체를 선언하고 끝점을 지정합니다. 반경 및 재료 특성. POV-Ray 소프트웨어에서 이 .pov 파일을 열면 단일 파란색 원통의 이미지가 렌더링됩니다.

## 참고자료
 * [POV-Ray - 위키피디아](https://en.wikipedia.org/wiki/POV-Ray)
 * [문서 POV-Ray 웹사이트](http://www.povray.org/documentation/)

