{
  "date" : "2020-03-16",
  "keywords" :[ "DWG", "파일 형식", "CAD", "열기", "만들기" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DWG 파일을 만들고 열 수 있는 DWG 파일 형식과 API에 대해 알아보세요.",
  "title" :"DWG 파일 형식",
  "linktitle" : "DWG",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2019-09-10"
}

## .DWG 파일이란?

DWG 확장자를 가진 파일은 2D 및 3D 설계 데이터를 포함하는 데 사용되는 독점 바이너리 파일을 나타냅니다. ASCII 파일인 DXF와 마찬가지로 DWG는 CAD(Computer Aided Design) 도면의 바이너리 파일 형식을 나타냅니다. CAD 파일의 내용을 표현하기 위한 벡터 이미지와 메타데이터를 포함하고 있습니다. Autodesk의 무료 DWG TrueView와 같이 Windows 운영 체제에서 DWG 파일을 볼 수 있는 무료 뷰어가 있습니다. DWG 파일에 도달하는 것을 지원하는 다른 타사 응용 프로그램도 있습니다. DWG 파일에는 사용자 생성 정보가 포함되며 다음이 포함됩니다.

* 디자인
* 기하학적 데이터
* 지도 및 사진

이 형식은 다양한 설계 목적으로 건축가, 엔지니어 및 디자이너가 널리 사용합니다.

## 간략한 역사 ##

DWG 파일 형식은 1982년 공식적으로 도입된 이후 시간이 지남에 따라 발전해 왔습니다. 과거 사건을 역사 관점에서 간략히 살펴보면 다음과 같습니다.

**1982:** Autodesk는 1970년 Mike Riddle이 개발한 DWG 파일 형식을 AutoCAD의 기반으로 사용하도록 허가했습니다.

**1998:** AutoCAD R14.01 릴리스와 함께 Autodesk는 암호화된 체크섬과 Autodesk의 WaterMark라고 하는 제품 코드를 프로그램에서 생성된 DWG 파일에 포함하는 DWGCHECK라는 기능을 통해 파일 확인 기능을 추가했습니다.

**2006:** Autodesk는 "TrustedDWG 기술"을 포함하도록 AutoCAD 2007을 수정하여 "Autodesk DWG. 이 파일은 Autodesk 응용 프로그램 또는 Autodesk 라이센스 응용 프로그램에서 마지막으로 저장한 신뢰할 수 있는 DWG입니다."를 DWG 파일에 포함합니다. 이 작업의 목적은 Autodesk 소프트웨어 사용자가 이러한 파일이 Autodesk 또는 RealDWG 응용 프로그램에서 생성되었음을 확인하는 데 도움이 되므로 비호환성 위험을 줄이는 데 확실히 도움이 됩니다.

## 파일 구조 ##

DWG는 다양한 응용 프로그램에서 널리 사용되는 파일 형식 중 하나였으며 강력한 파일 구조를 가지고 있습니다. DWG는 이진 파일 형식이므로 일반 ASCII [DXF](/ko/cad/dxf/) 파일 형식처럼 사람이 읽을 수 없습니다. DWG 파일에는 일반적으로 이미지 좌표 및 관련 메타데이터에 대한 정보가 포함됩니다. OpenDesign에서 DWG 파일 형식의 전체 [사양](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)을 다운로드할 수 있습니다. DWG 파일 형식의 파일 구조는 다음과 같이 요약됩니다.

**Header**: 파일 헤더는 DWG Header 변수와 오류 감지에 사용되는 CRC(Cyclic Redundancy Check)에 대한 정보로 구성됩니다. 각 하위 섹션은 서로 다른 레이블을 나타내는 데 서로 다른 길이의 비트가 사용되는 특수 벡터입니다. 예를 들어, DWG 헤더 변수의 처음 6비트는 버전 문자열을 나타냅니다.

**클래스 정의:** DWG 파일에는 특정 .dwg 파일 용도에 따라 여러 클래스가 포함될 수 있습니다. 기타 클래스 데이터 영역의 클래스 메타데이터 크기, 클래스 번호 및 체크섬과 같은 정보.

**템플릿**: 이것은 선택 사항이며 R15 및 R15 버전의 경우 이 섹션은 Object Free Space 섹션 아래에 있습니다.

**패딩**: 메타데이터는 특정 바이트 수로 접미사와 접미사를 붙여 이전 AutoCAD 소프트웨어 버전이 새 DWG 파일 형식과 호환되도록 합니다.

**이미지 데이터**: 이 섹션의 메타데이터는 특정 .dwg 유형에 따라 다릅니다. R14 및 R15 사용자의 경우 이 섹션은 선택 사항입니다.

**객체 데이터**: 객체 데이터는 기존 객체 목록에 해당하는 테이블 엔터티, 사전 항목 등의 전체 목록으로 구성됩니다.

**객체 맵**: 파일의 각 객체 위치는 파일의 이 섹션에 지정됩니다. 이 섹션에 있는 대부분의 메타데이터는 개체를 식별하고 다시 렌더링하는 역할을 하는 파일 핸들입니다.

**객체 여유 공간**: 이 섹션은 모든 사용자에게 선택 사항입니다.

**두 번째 헤더**: DWG 파일 끝에 있는 파일 헤더 섹션의 복제본

## 참조 ##

* [DWG 파일 형식 사양](https://www.opendesign.com/files/guestdownloads/OpenDesign_Specification_for_.dwg_files.pdf)
* [DWG 파일 사양](https://www.scan2cad.com/dwg/file-spec/)
* [DWG - 위키피디아 작성](https://en.wikipedia.org/wiki/.dwg)

