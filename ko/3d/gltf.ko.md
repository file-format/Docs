{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "파일", "확장자", "형식", "3D", "크로노스 그룹 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"GLTF 파일을 만들고 열 수 있는 GLTF 파일 및 API에 대해 알아보세요.",
  "title" :"GLTF - GL 전송 파일 형식",
  "linktitle" : "GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## .GLTF 파일이란?

glTF(GL 전송 형식)는 3D 모델 정보를 JSON 형식으로 저장하는 3D 파일 형식입니다. JSON을 사용하면 3D 자산의 크기와 이러한 자산의 압축을 풀고 사용하는 데 필요한 런타임 처리가 최소화됩니다. 애플리케이션별 3D 장면 및 모델의 효율적인 전송 및 로드를 위해 채택되었습니다. glTF는 Khronos Group 3D Formats Working Group에서 개발했으며 제작자는 3D의 [JPEG](/ko/image/jpeg/)라고도 설명합니다.

GLTF 파일 형식은 3D 콘텐츠 도구 및 서비스를 위한 확장 가능하고 공통된 게시 형식을 정의하여 제작 워크플로를 간소화하고 업계 전반에서 콘텐츠를 상호 운용할 수 있도록 합니다. glTF 파일 형식을 만든 뒤에 숨겨진 의도는 3D 콘텐츠 도구 및 서비스에 대해 확장 가능하고 공통된 게시 형식을 정의하여 제작 워크플로를 간소화하고 업계 전반에 걸쳐 콘텐츠를 상호 운용할 수 있도록 하는 것이었습니다. WebGL 및 기타 API를 사용하는 응용 프로그램의 런타임 처리를 최소화합니다.

## GLTF 파일의 간략한 역사

glTF 파일 형식 1.0의 첫 번째 사양은 2015년 10월에 발표되었습니다. 이것은 Khronos가 2012년 3월에 시작한 일련의 노력으로 이루어졌습니다. 이러한 노력의 목적은 WebGL 견인력 주변의 기회를 평가하는 것이었습니다. 결과적으로 2012년 WebGl 밋업에서 JSON 형식을 기반으로 한 glTF 형식의 첫 번째 데모가 발표되었습니다. 이 형식은 Cesium, 3D Tiles, Oculus, Microsoft, Archilogic 등을 비롯한 여러 회사에서 수시로 채택했습니다.

glTF 2.0은 2017년 6월 5일 Web3D 2017 Conference에서 발표되었습니다. 그 이후에 glTF 파일 형식을 채택한 회사 목록이 많이 있습니다.

## GLTF 파일 형식

glTF 2.0에 대한 파일 형식 사양은 참조용으로 [온라인](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0)에서 사용할 수 있으며 지원을 위해 읽기/쓰기와 관련된 모든 구현에서 참조해야 합니다. .glTF 파일 형식

glTF는 자산을 외부 데이터를 지원하는 JSON 파일로 정의합니다. 다음을 통해 3D 모델을 나타냅니다.

* 노드 계층, 재료, 카메라에 대한 정보는 물론 메시, 애니메이션 및 기타 구성에 대한 설명자 정보를 포함하는 JSON 형식의 .glTF 파일에 포함된 전체 장면 설명
* 지오메트리 및 애니메이션 데이터, 기타 버퍼 기반 데이터를 포함하는 바이너리 파일(.bin)
* 텍스처용 이미지 파일([.jpg](/ko/image/jpeg/), [.png](/ko/image/png/))

이미지와 같은 외부 자산은 URI를 통해 참조되는 외부 파일에 저장됩니다. 이러한 URI는 GLB 컨테이너와 함께 저장되거나 데이터 URI를 사용하여 JSON에 직접 포함됩니다. 유효한 각 glTF는 해당 버전을 지정해야 합니다.

glTF는 작은 파일 크기, 빠른 로딩, 완전한 3D 장면 표현 및 확장성을 달성하도록 설계되었습니다. 이러한 고유한 설계 목표는 3D 도메인에서 glTF 파일 형식이 인기 있는 주된 이유입니다. 다음은 다양한 파일 형식에 대해 glTF 파일 형식에서 지원하는 MIME 형식입니다.

* .gltf 파일은 model/gltf+json을 사용합니다.
* .bin 파일은 application/octet-stream을 사용합니다.
* 텍스처 파일은 특정 이미지 형식에 따라 공식 이미지/* 유형을 사용합니다. 최신 웹 브라우저와의 호환성을 위해 image/jpeg, image/png와 같은 이미지 형식이 지원됩니다.

### JSON 인코딩

glTF는 JSON 파일 형식에 대해 다음과 같은 추가 제한을 부과합니다.

클라이언트 측 구현을 단순화하기 위해 glTF에는 JSON 형식 및 인코딩에 대한 추가 제한이 있습니다.

1. JSON은 BOM 없이 UTF-8 인코딩을 사용해야 합니다.
1. 이 사양에 정의된 모든 문자열(속성 이름, 열거형)은 ASCII 문자 집합만 사용하며 일반 텍스트로 작성해야 합니다(예: `"\u0062\u0075\u0066\u0066\u0065\u0072"` 대신 "버퍼").
1. JSON 객체 내의 이름(키)은 고유해야 합니다. 즉, 중복 키가 허용되지 않습니다.

### URI

버퍼 및 이미지 리소스는 URI를 통해 참조됩니다. 클라이언트는 다음 두 가지 URI 유형을 지원해야 합니다.

**데이터 URI:** 데이터 URI는 RFC 2397에 정의된 대로이며 glTF에서 JSON에 리소스를 포함하는 데 사용합니다.

**상대 URI 경로:** 또는 RFC 3986, [섹션 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2)에 정의된 경로-noscheme — 체계, 권한 또는 매개변수가 없습니다. 예약된 문자는 RFC 3986, [섹션 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2)에 따라 퍼센트로 인코딩되어야 합니다.

## 참조 ##

* [glTF 2.0 사양 - Khronos](https://github.com/KhronosGroup/glTF)
* [glTF 파일 형식 - 위키피디아 작성](https://en.wikipedia.org/wiki/GlTF)

