{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XFDF 파일 형식 - XFDF 파일이란 무엇입니까?",
  "description":"XFDF 파일을 만들고 열 수 있는 API와 XFDF 파일에 대해 알아보세요.",
  "linktitle" : "XFDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

## .XFDF 파일이란?

확장자가 .xfdf인 파일은 Adobe Acrobat 소프트웨어로 생성된 XML 양식 데이터 형식입니다. [FDF](/ko/pdf/fdf/)와 마찬가지로 XFDF는 XML 형식의 양식 요소 설명과 값을 포함합니다. 여기에는 PDF 양식에 있는 텍스트 필드의 이름과 값이 포함될 수 있습니다. XFDF는 사람이 읽을 수 있는 형식으로 저장되며 C#과 같은 프로그래밍 언어를 사용하여 프로그래밍 방식으로 읽을 수 있습니다.

## XFDF 파일 형식 - 추가 정보

XFDF 파일은 데이터 가져오기 및 내보내기에 사용되는 범용 형식인 XML 파일 형식으로 저장됩니다. XFDF 파일 구조는 아래와 같이 헤더, 필드 값, 요소 데이터로 구성됩니다.

|요소|속성|내용|
---|---|---|
|\<XFDF> ||최상위 요소|
|\<fields> ||이 템플릿의 모든 필드 값|
|<field (T)> |이름 |필드 이름|
|<value (V)> |값 |필드 값|

## 참고문헌

* [Acrobat의 FDF 형식 지원](https://helpx.adobe.com/coldfusion/develping-applications/working-with-documents-charts-and-reports/assembly-pdf-documents/fdf-format-support-for -acroforms.html)
* [Adobe 개발자 리소스](https://opensource.adobe.com/dc-acrobat-sdk-docs/)

