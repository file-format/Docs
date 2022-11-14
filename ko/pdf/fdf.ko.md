{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FDF 파일 형식 - FDF 파일이란?",
  "description":"FDF 파일 형식과 FDF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "FDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## .FDF 파일이란?

FDF(**Forms Data Format**) 파일은 [PDF](/ko/pdf/) 파일의 양식 필드에서 데이터를 내보내 생성되는 텍스트 문서입니다. 여기에는 PDF 파일에서 사용할 수 있는 양식 필드에서 추출된 텍스트 필드 데이터만 포함됩니다. 내보낸 데이터에 양식 자체가 포함되어 있지 않기 때문에 비교적 작은 데이터 파일이 생성됩니다. Adobe Acrobat은 응용 프로그램 메뉴의 '양식 데이터 내보내기' 옵션을 사용하여 양식 필드 데이터를 내보내는 기능을 제공합니다.

## FDF 파일 형식 - 추가 정보

FDF는 일반 텍스트 형식이며 Portable Document Format에 대한 [ISO 32000 표준](https://www.iso.org/standard/51502.html)의 일부로 포함되어 있습니다. Acrobat Forms 또는 AcroForms에서 데이터를 가져오고 내보낼 수 있도록 Adobe에서 개발했습니다.

FDF 파일에는 두 가지 유형이 있습니다.

• '클래식 FDF' – 기존의 정적 양식을 채우기 위한 데이터를 제공합니다.

• '템플릿 FDF' – 지정된 PDF 파일 내부의 템플릿을 기반으로 새 PDF를 구성합니다. 새 문서 내의 양식은 데이터를 제공하여 채워집니다.

## Adobe Acrobat을 사용하여 FDF 만들기

Adobe의 [FDF 툴킷](https://opensource.adobe.com/dc-acrobat-sdk-docs/)을 사용하면 텍스트 데이터에서 FDF 파일을 만들 수 있습니다.

## 참조 ##

* [Acrobat의 FDF 형식 지원](https://helpx.adobe.com/coldfusion/develping-applications/working-with-documents-charts-and-reports/assembly-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe 개발자 리소스](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

