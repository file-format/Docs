{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "파일", "포맷", "열기", "읽기", "API", "MicroStation", "Intergraph 인터랙티브 그래픽 디자인 시스템" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD 설계 파일 형식",
  "description" :"DGN 파일을 만들고 열 수 있는 DGN 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## .DGN 파일이란?

.dgn(디자인) 확장자를 가진 파일은 MicroStation 및 Intergraph Interactive Graphics Design System과 같은 CAD 응용 프로그램에서 만들고 지원하는 도면 파일입니다. 고속도로, 교량, 건물 등 건설 프로젝트의 설계도 생성 및 저장에 사용됩니다. 형식은 Autodesk의 [DWG](/ko/cad/dwg/) 파일 형식과 유사하며 경쟁자로 간주됩니다. DNG 파일은 Intergraph 표준 파일 형식 또는 V8 DGN으로 저장할 수 있습니다. DGN은 DWG, [BMP](/ko/image/bmp/), [JPEG](/ko/image/jpeg/), [PDF](/ko/pdf/), [GIF](/ko/image/)와 같은 여러 다른 형식으로 변환할 수 있습니다. gif/) 및 기타. Corel PaintShop Photo Pro 및 IMSI TurboCAD Deluxe 버전과 같은 다른 소프트웨어 응용 프로그램 외에도 Autodesk AutoCAD, Bentley View 및 Bentley Systems MicroStation으로 열 수 있습니다.

## V8 DGN 파일 형식

MicroStation V8 DGN 파일은 하나 이상의 모델로 구성됩니다. 모델은 요소의 컨테이너입니다. V8 DGN은 이전 버전의 MicroStation에 있던 모든 파일 형식 기반 제약을 제거합니다. 다음은 DGN 파일 형식의 개선 사항 목록입니다.

* DGN 파일의 레벨 수 제한이 제거되었으며 각 레벨에 이름이 지정되어 요소로 저장됩니다.
* DGN 파일의 최대 물리적 크기는 제한이 없으며 운영 체제에 의해서만 제한됩니다(예: NT 제한은 4GB).
* 단일 요소의 최대 크기는 128KB입니다.
* 셀의 최대 크기에는 제한이 없습니다.
* 셀 이름은 약 500자로 제한됩니다.
* DGN 파일에 첨부할 수 있는 참조 수에는 제한이 없습니다.
* 선 문자열, 모양 또는 점 곡선은 최대 5000개의 정점을 가질 수 있습니다.
* 복잡한 사슬이나 복잡한 모양의 구성 요소 수에는 제한이 없습니다.
* DGN 파일의 그래픽 그룹 수에는 제한이 없습니다.
* 울타리가 배치된 뷰와 평행합니다.
* 한 줄의 텍스트는 65,535자를 포함할 수 있습니다.
* 텍스트 노드의 최대 크기에는 제한이 없습니다.
* DGN 파일의 텍스트 노드 수에는 제한이 없습니다.
* 각 요소에는 요소의 수명 주기 동안 변경되지 않는 고유한 64비트 식별자가 있습니다.
* 각 요소에는 가장 최근에 변경된 시간을 나타내는 타임스탬프가 있습니다.

## 참고문헌

* [DNG - 위키피디아 작성](https://en.wikipedia.org/wiki/DGN)
* [OpenDNG](http://www.bentley.com/opendgn)
* [MicroStation V8 DGN 파일 형식](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

