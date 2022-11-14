{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","cd 파일이란","cd 파일을 여는 방법", "확장자", "파일", "cd 파일","cd 파일 형식", "cd 파일 확장자" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio 클래스 다이어그램 파일",
  "description":"CD 파일 형식과 CD 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## .CD 파일이란?

확장자가 .cd인 파일은 현재 솔루션의 모든 클래스 간의 구조 및 관계에 대한 정보를 제공하는 Visual Studio 클래스 다이어그램 파일입니다. Visual Studio 솔루션([.sln](/ko/programming/sln/)으로 표시)에는 각각 여러 클래스가 있는 하나 이상의 프로젝트가 포함될 수 있습니다. 클래스 다이어그램 파일은 프로젝트를 마우스 오른쪽 버튼으로 클릭하고 클래스 다이어그램 옵션을 선택하여 생성할 수 있습니다.

## 클래스 다이어그램(.cd) 파일 형식 - 추가 정보

클래스 다이어그램 파일은 프로젝트의 클래스를 XML 노드로 나타내는 표준 XML 파일 형식으로 저장됩니다. Visual Studio를 사용할 수 없는 경우 이러한 클래스 다이어그램 파일은 XML 파일 열기를 지원하는 모든 응용 프로그램에서 열 수 있습니다.

### Visual Studio 프로젝트에 클래스 다이어그램을 추가하는 방법

Visual Studio에서 클래스 다이어그램을 추가할 솔루션/프로젝트를 엽니다. 그런 다음 프로젝트 노드를 마우스 오른쪽 버튼으로 클릭하고 추가 > 새 항목을 선택합니다. 또는 Ctrl+Shift+A를 누릅니다.

* 새 항목 추가 대화 상자가 열립니다.

* Common Items > General을 확장한 다음 템플릿 목록에서 Class Diagram을 선택합니다. Visual C++ 프로젝트의 경우 유틸리티 범주에서 클래스 다이어그램 템플릿을 찾습니다.

### 클래스 다이어그램(CD)을 이미지로 내보내기

Visual Studio를 사용하면 클래스 다이어그램을 [PNG](/ko/image/png/), [JPEG](/ko/image/jpeg/) 및 [BMP](/ko/image/bmp/)와 같은 이미지로 변환/내보내기가 가능합니다. 이러한 내보낸 클래스 다이어그램 파일은 문서화 및 TDP(기술 데이터 팩) 기록 유지 목적으로 사용할 수 있습니다. 클래스 다이어그램을 이미지로 변환하려면 Microsoft Visual Studio 내에서 다음 단계를 사용할 수 있습니다.

1. 클래스 다이어그램(.cd) 파일을 엽니다.
1. 클래스 다이어그램 메뉴 또는 다이어그램 표면 바로 가기 메뉴에서 다이어그램을 이미지로 내보내기를 선택합니다.
1. 다이어그램을 선택합니다.
1. 원하는 형식을 선택합니다.
1. 내보내기를 선택하여 내보내기를 마칩니다.

## 참고문헌

* [Visual Studio의 디자인 클래스](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

