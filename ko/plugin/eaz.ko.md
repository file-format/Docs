{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ 파일 - EAZ 파일이란 무엇이며 어떻게 여나요?",
  "description":"EAZ 파일 형식과 EAZ 파일을 생성하고 열 수 있는 API에 대해 알아봅니다.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-koz"
}
},
  "lastmod" : "2023-12-23"
}

## .EAZ 파일이란?

EAZ 파일은 지도 탐색, 시각화 및 공유를 위해 ESRI에서 개발한 무료 애플리케이션인 ArcGIS Explorer에서 사용하는 추가 기능 파일입니다. 여기에는 [XML file](/web/xml/), 컴파일된 코드 및 추가 기능에 필요한 지원 파일이 포함된 압축 파일 아카이브가 포함되어 있습니다. 이러한 파일은 새로운 버튼, 도킹 가능한 창 및 기타 확장 기능을 통합하여 소프트웨어의 기본 기능을 확장하는 데 사용됩니다.

## EAZ 파일 형식 - 추가 정보

EAZ 파일은 ArcGIS Explorer 내에서 사용자 정의 기능을 생성하도록 설계된 개발 키트인 ArcGIS Explorer SDK를 활용하여 생성됩니다. 이러한 파일은 [ZIP](/compression/zip/) 압축을 활용하여 콘텐츠를 효율적으로 패키지합니다. 아카이브의 핵심인 **Addins.xml** 파일은 루트 디렉토리에 위치하며 EAZ 파일에 포함된 다양한 사용자 정의를 간략하게 설명하고 자세히 설명하는 중요한 구성 요소 역할을 합니다.

Addins.xml 파일은 본질적으로 로드맵 역할을 하며 EAZ 파일이 ArcGIS Explorer에 도입하는 특정 개선 사항, 수정 사항, 확장에 대한 통찰력을 제공합니다. 이 포괄적인 구조를 통해 개발자는 새로운 기능, 버튼, 도킹 가능한 창을 캡슐화하고 원활하게 통합하여 ArcGIS Explorer 응용프로그램의 전반적인 기능과 사용자 경험을 향상시킬 수 있습니다.

## 참고자료

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
