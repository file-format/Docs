{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BRD 파일 - EAGLE 회로 기판 파일 - .brd 파일이 무엇이며 어떻게 여나요?",
  "description" : "BRD EAGLE 회로 기판 파일 및 여는 방법에 대해 알아보세요.",
  "linktitle" : "BRD",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-brd-ko",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## .BRD 파일이란?

BRD 파일 형식은 인쇄 회로 기판(PCB) 설계를 위한 전자 설계 자동화(EDA) 소프트웨어에 사용됩니다. Eagle, KiCad, Altium Designer 등과 같은 PCB 설계 소프트웨어는 인쇄 회로 기판의 레이아웃, 연결 및 기타 설계 관련 정보를 저장하기 위해 이 파일 형식을 사용합니다.

BRD 파일은 엔지니어와 디자이너가 디자인을 생성, 수정 및 분석하는 데 사용하는 디지털 파일인 CAD 파일 유형입니다. BRD 파일은 전자 산업에서 인쇄 회로 기판(PCB) 설계에 일반적으로 사용되는 소프트웨어 응용 프로그램인 Autodesk EAGLE과 연결되어 있습니다. Autodesk EAGLE은 회로도 캡처(회로의 시각적 표현 생성)와 PCB 레이아웃(구성요소 및 라우팅 연결 배열)을 위한 도구를 제공합니다.

BRD 파일은 Autodesk EAGLE 소프트웨어 제품군의 구성 요소인 EAGLE Layout Editor를 사용하여 생성됩니다. 이 편집기를 사용하면 구성 요소 배치, 트레이스 라우팅, 설계 규칙 정의 및 제조에 필요한 파일 생성을 포함하여 PCB 레이아웃을 설계할 수 있습니다.

BRD 파일은 PCB의 전자 회로 설계를 위한 템플릿 또는 청사진 역할을 합니다. 설계자는 EAGLE 및 .brd 파일을 사용하여 회로도를 제조 가능한 실제 레이아웃으로 변환합니다.

.BRD 파일은 Gerber 드릴 데이터 형식으로 저장할 수 있습니다. Gerber 파일은 PCB 제조에서 PCB 설계의 패턴, 레이어 및 기능을 설명하는 데 사용되는 표준 형식입니다. .brd 파일을 이 형식으로 저장하면 PCB 제작에 필요한 지침을 생성하는 CAM(컴퓨터 지원 제조) 프로그램에서 해당 파일을 사용할 수 있습니다.

## BRD 파일 뷰어

.brd 파일을 보는 데 사용할 수 있는 여러 소프트웨어 도구가 있으므로 사용자는 Autodesk EAGLE과 같은 소프트웨어로 생성된 PCB 레이아웃을 시각화하고 검사할 수 있습니다.

1.  **Autodesk EAGLE**: Autodesk EAGLE에 액세스할 수 있는 경우 보기 및 편집 목적으로 소프트웨어 내에서 직접 .brd 파일을 열 수 있습니다.
    
2.  **KiCad**: KiCad는 PCB 레이아웃 편집기가 포함된 오픈 소스 EDA 소프트웨어 제품군입니다. Autodesk EAGLE로 생성된 .brd 파일을 가져오고 볼 수 있는 기능이 있습니다.
    
3.  **ViewPlot**: ViewPlot은 .brd를 포함한 다양한 PCB 파일 형식을 지원하는 독립형 Gerber 뷰어입니다. 이를 통해 사용자는 원본 설계 소프트웨어 없이도 PCB 설계를 볼 수 있습니다.
    
4.  **GC-Prevue**: GC-Prevue는 .brd 파일도 처리할 수 있는 또 다른 인기 있는 Gerber 뷰어입니다. PCB 레이아웃 시각화, 거리 측정 및 설계 세부 사항 검사를 위한 기능을 제공합니다.
    
5.  **Gerbv**: Gerbv는 Gerber 형식으로 저장된 .brd 파일을 포함할 수 있는 Gerber 파일 보기를 지원하는 오픈 소스 Gerber 뷰어입니다.
    
6.  **온라인 뷰어 도구**: 웹 브라우저에서 직접 .brd 파일을 업로드하고 볼 수 있는 온라인 도구도 있습니다. 그러한 예 중 하나는 Gerber 및 .brd를 포함한 다양한 PCB 파일 형식 보기를 지원하는 EasyEDA의 Online Gerber Viewer입니다.

## BRD 파일 여는 방법? .

PCB 설계에 사용되는 BRD 파일은 다양한 PCB 설계 응용 프로그램에서 열 수 있습니다.

- **Autodesk EAGLE**: Autodesk에서 개발한 크로스 플랫폼 PCB 설계 소프트웨어입니다. 회로도 작성, PCB 레이아웃 및 전기 연결 라우팅을 지원합니다. 사용자는 Autodesk EAGLE 내에서 직접 .brd 파일을 열어 보고 추가 편집을 할 수 있습니다.
    
- **Altium Designer**: Altium Designer는 주로 Windows 운영 체제를 위한 포괄적인 PCB 설계 소프트웨어입니다. 회로도 캡처, PCB 레이아웃 및 설계 분석을 위한 광범위한 기능을 제공합니다. Altium Designer는 .brd 파일 열기도 지원하므로 사용자는 다른 소프트웨어에서 만든 디자인을 가져와서 작업할 수 있습니다.
    
- **오픈 보드 뷰어**: 오픈 보드 뷰어는 Linux 운영 체제용으로 특별히 설계된 PCB 보기 소프트웨어입니다. 이는 사용자가 PCB 레이아웃을 시각화하고, 구성 요소를 검사하고, 라우팅 세부 정보를 검토할 수 있는 오픈 소스 도구입니다. Open Board Viewer는 .brd 파일 열기를 지원하므로 Linux 플랫폼 사용자는 다른 소프트웨어에서 생성된 설계를 보고 분석할 수 있습니다.

다음은 BRD 파일을 여는 데 사용할 수 있는 프로그램 목록입니다.

- (Windows, Mac, Linux)용 **Autodesk EAGLE**(무료 평가판)
- (Windows, Mac, Linux)용 **Altium Designer**(무료 평가판)
- Linux용 **오픈 보드 뷰어**(무료)

## 참고자료
* [EAGLE 프로그램](https://en.wikipedia.org/wiki/EAGLE_(프로그램))


