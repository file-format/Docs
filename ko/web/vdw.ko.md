{
  "date" : "2019-10-11",
  "keywords" :[ "vdw","vdw 파일", "vdw 파일 형식", "vdw 파일 형식", "파일", "유형", "vdw 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Visio 그래픽 서비스 파일 형식",
  "description":"VDW 파일 형식과 VDW 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}
## .VDW 파일이란?
VDW는 웹 드로잉을 렌더링하는 데 필요한 스트림과 저장소를 지정하는 Visio Graphics Service 파일 형식입니다. 웹 드로잉은 벡터 또는 래스터 드로잉으로 렌더링할 수 있는 드로잉 페이지, 모양, 글꼴, 이미지, 데이터 연결 및 다이어그램 업데이트 정보의 모음입니다. VDW 파일은 Microsoft Visio에서도 열 수 있지만 주로 웹에서 사용하기 위해 저장됩니다. Microsoft Visio는 Visio 파일을 [PNG](/ko/Image/PNG/), [BMP](/ko/Image/BMP/), [PDF](/ko/pdf/) 등을 포함한 다양한 파일 형식으로 변환하는 기능을 제공합니다.

## **VDW** 파일 형식 #

VDW 파일 형식의 기술 사양은 [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)에서 온라인으로 제공되며 개발자가 생성을 위해 참조할 수 있습니다. 응용 프로그램. 기술 문서는 저장소와 스트림을 포함하는 복합 파일에 포함된 데이터를 설명합니다. 웹 드로잉의 표현은 ZIP 아카이브를 통해 VisioServerData라는 스트림을 통해 가능합니다. 아카이브의 ShapGraphic XML 파트는 웹 드로잉에 표시되는 그래픽 요소를 설명하고 XAML(Extensible Application Markup Language)로 표현됩니다. ZIP 아카이브의 XML 부분 모음은 웹 드로잉의 데이터 연결, 모양 및 다이어그램 업데이트 논리에 대한 정보를 설명합니다. 이러한 부분은 XML로 표현됩니다. DataGraphic XML 부분은 웹 드로잉의 데이터가 데이터 원본에서 새로 고쳐진 후 평가될 다시 계산된 속성을 설명합니다. ZIP 아카이브의 추가 항목에는 웹 도면에 사용된 글꼴 및 이미지에 대한 정보가 포함되어 있습니다.

|![파일의 가능한 구현](/ko/web/vdw.png "파일의 가능한 구현")

## 참조 ##

* [[MS-VGSFF]: Visio Graphics Service(.vdw) 파일 형식](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

