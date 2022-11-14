{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "keywords" :[ "SWF", "파일", "확장자", "형식", "비디오 형식","SWF 파일이란", "swf 파일 형식", "swf 파일 플레이어","swf 파일을 여는 방법"] ,
  "title" :"SWF 파일 - Shockwave Flash 동영상 파일 형식",
  "description":"SWF 파일이란 무엇이며 SWF 파일을 만들고 여는 방법을 보여줄 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SWF",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## .SWF 파일이란?

SWF 파일은 Adobe Flash로 만든 애니메이션 파일입니다. 여기에는 텍스트, 벡터 이미지, 래스터 이미지, 액션 스크립트, 원, 선, 정사각형 및 직사각형과 같은 개체와 같은 다양한 유형의 요소가 포함되어 애니메이션을 생성할 수 있습니다. SWF 파일은 이러한 멀티미디어 항목을 서로 다른 초당 프레임(fps)에서 재생할 수 있는 프레임으로 정렬합니다. SWF는 Short Web File을 의미하지만 Shockwave 형식으로도 알려져 있습니다.

*SWF 파일을 열 수 있는** 응용 프로그램에는 Adobe Flash Player(현재 중단됨) 및 Eltima Elmedia Player가 포함되었습니다.

## SWF 파일 형식 - 추가 정보

SWF 파일은 바이너리 파일로 디스크에 저장하는 데 사용되었습니다. SWF 파일 형식은 웹 사이트에 포함되어 독립적으로 재생할 수 있는 애니메이션과 게임을 개발하는 데 사용되었습니다. 또한 비디오와 사운드를 지원하여 개발자에게 대화형 멀티미디어 응용 프로그램을 만들 수 있는 많은 선택권을 제공했습니다. SWF 파일은 Adobe Shockwave가 설치된 웹 브라우저에서 재생할 수 있습니다. Adobe Flash는 짧은 기능과 보안 문제로 인해 2020년 12월에 중단되었습니다.

## SWF 파일 형식의 간략한 역사

SWF 파일 형식은 원래 FutureWave Software에서 파일 크기를 작게 유지하면서 네트워크 연결이 느린 시스템의 플레이어 소프트웨어에서 실행할 의도로 애니메이션을 표시하도록 설계되었습니다. 1996년 12월 Macromedia는 FutureWave를 소유하고 Macromedia Flash 1.0으로 전환했습니다.

2005년, Macromedia는 2008년에 오픈 소스 프로젝트의 일부로 SWF를 발표한 Adobe에 인수되었습니다. 같은 해에 Adobe는 SWF 파일의 크롤링 및 인덱싱을 허용하는 세계적으로 유명한 웹 엔진에 코드를 출시했습니다. 그러나 SWF 파일이 인터넷에 Flash 콘텐츠를 게시하기 위한 표준 형식이 된 것처럼 SWF는 Small Web 형식을 의미하도록 수정되었습니다.

## SWF 파일 구조

경로는 단순한 선에서 베지어 곡선에 이르는 기본 요소 세그먼트의 시퀀스인 SWF의 기본 그래픽 요소입니다. 이러한 간단한 요소는 큐브, 타원 및 텍스트와 같은 다른 추가 기본 요소를 만드는 데도 도움이 됩니다. SWF의 그래픽 프리미티브는 SVG 및 MPEG-4 BIFS와 같은 다른 형식의 그래픽 요소와 유사합니다.

목록 표시 및 이미 정의된 요소의 재사용/이름 변경도 형식에서 허용됩니다. SWF의 바이너리 스트림 형식은 태그, 크기 및 페이로드 측면에서 유사한 QuickTime 원자와 비교할 수 있습니다. 바이너리 스트림 형식을 사용하면 이전 플레이어가 지원되지 않는 콘텐츠를 건너뛸 수 있습니다. SWF의 원래 버전은 벡터 그래픽과 이미지를 제공하는 것으로 제한되었지만 새 버전에서는 오디오 및 비디오 콘텐츠도 허용합니다.

"Stage3D"라는 Flash Player의 새로운 저수준 3D API가 버전 11에 도입되었습니다. 이 API는 OpenGL 또는 Direct3D에 대응하도록 계획되었습니다. Stage3D는 AGAL(Adobe Graphics Assembly Language)이라는 저급 언어로 색상을 정의합니다. 다음은 SWF 파일 형식의 몇 가지 기본 데이터 유형입니다.

### 좌표

SWF 파일 형식의 XY 좌표는 정수로 저장되며 트윕이라는 단위로 측정됩니다. 트윕은 논리 픽셀의 1/20로 구성됩니다. 논리 픽셀과 화면 픽셀은 100% 스케일 없이 파일을 재생할 때 동일합니다.

### 정수 유형 및 바이트 순서

8, 16, 32 및 64비트의 부호 있는 및 부호 없는 정수 유형은 SWF 파일 형식에서 허용됩니다. 리틀 엔디안 바이트 순서는 정수 값을 저장하는 데 사용됩니다. 바이트 내에서 비트 순서는 빅 엔디안으로 저장됩니다. 모든 정수 값은 바이트 정렬되어야 합니다. 부호 있는 정수는 전통적인 2의 보수 비트 패턴을 사용하여 표현됩니다.

### 고정 소수점 숫자

SWF 파일 형식은 32비트와 16비트의 두 가지 유형의 고정 소수점 수를 지원합니다.

### 부동 소수점 숫자

SWF 8 and later version use three types of floating-point numbers (FLOAT, FLOAT 16, DOUBLE) that are compatible to the IEEE Standard 754 of floating-point types.


### 인코딩된 정수

인코딩된 정수 유형 중 하나는 가변 바이트 수로 SWF 9 이상에서 지원됩니다.

## 참고문헌

* [SWF 파일 형식](https://en.wikipedia.org/wiki/Swf)

