{
  "date" : "2021-06-30",
  "keywords" :[ "msi 파일", "MSI 파일 형식", "msi 파일이란", "파일", "msi 예", "msi 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"MSI 파일을 만들고 열 수 있는 MSI 파일 형식 및 API에 대해 알아보세요.",
  "title" :"MSI - Windows Installer 패키지 파일",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## .MSI 파일이란?
Windows 프로그램을 설치하고 실행하는 데 사용되는 MSI 파일. 설치해야 할 필수 파일과 설치 위치에 대한 정보를 포함하여 일반적인 소프트웨어 프로그램에 대한 설치 정보가 포함된 Microsoft Windows용 전체 패키지입니다. MSI 파일에는 소프트웨어 업데이트용 패키지도 포함될 수 있습니다. MSI 파일은 [EXE](/ko/executable/exe/)와 유사하지만 EXE에 설치 프로그램 정보가 포함되지 않을 수 있으며 EXE 파일을 실행할 때 소프트웨어 프로그램이 직접 실행될 수 있습니다.

## MSI 파일 형식
Windows Installer는 실제로 소프트웨어 프로그램의 설치, 제거 및 유지 관리에 사용되는 Microsoft Windows의 API(응용 프로그래밍 인터페이스) 및 소프트웨어 구성 요소입니다. 설치 정보 및 선택적 파일은 COM 구조적 저장소로 구조화된 설치 패키지 및 느슨한 관계형 데이터베이스로 패키지됩니다. .msi 파일 확장자를 갖는 **MSI 파일**으로 잘 알려져 있습니다. 파일 확장자가 **.mst**인 패키지에는 Windows Installer의 **Transformation Scripts**가 포함되어 있고, **.msm** 확장자가 포함된 파일에는 **Merge Modules** 및 파일 확장자 **.pcp**가 포함되어 있습니다. **패치 생성 속성**에 사용됩니다. Windows Installer는 이전 버전인 Setup API에서 크게 변경된 후 더욱 발전되었습니다. GUI 프레임워크와 제거 순서의 자동 생성은 Windows Installer의 새로운 기능입니다. 이제 독립 실행형 실행 가능한 설치 프로그램 프레임워크의 대안으로 간주되었습니다.

### MSI 패키지의 논리적 구조
패키지는 하나 이상의 전체 제품 설치를 지정하며 일반적으로 **GUID**로 식별됩니다. 제품은 하나 이상의 구성 요소로 구성되며 다양한 기능으로 그룹화됩니다. Windows Installer는 다양한 제품 간의 종속성을 동시에 처리하지 않습니다. 패키지의 논리적 구조는 다음 요소로 구성됩니다.

- **제품**: 단일, 설치, 작동 프로그램 또는 함께 결합된 여러 프로그램 세트가 제품입니다. 제품은 고유한 GUID로 식별됩니다.
- **기능**: 구성 요소 및 기타 하위 기능을 원하는 수만큼 포함할 수 있습니다. 더 작은 패키지는 단일 기능으로 구성될 수 있습니다.
- **구성 요소**: 구성 요소는 Windows Installer에서 하나의 단위로 처리됩니다. 프로그램 파일, 폴더, 레지스트리 키, COM 구성 요소 및 바로 가기를 포함할 수 있습니다.
- **키 경로**: 키 경로는 패키지 작성자가 지정된 구성 요소에 대해 중요하다고 지정하는 특정 파일, ODBC 데이터 원본 또는 레지스트리 키입니다.

## 참고문헌

* [Windows Installer - Wikipedia 제공](https://en.wikipedia.org/wiki/Windows_Installer)


