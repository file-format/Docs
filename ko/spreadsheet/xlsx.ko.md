{
  "date" : "2019-12-10",
  "keywords" :[ "XLSX", "파일", "확장자", "파일 형식", "엑셀", "스프레드시트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"XLSX 파일이 무엇이며 XLSX 파일을 만들고 열 수 있는 API에 대해 알아봅니다.",
  "title" :"XLSX 파일 형식 - XLSX 파일이란 무엇입니까?",
  "linktitle" : "XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## .XLSX 파일이란?

**XLSX**는 Microsoft Office 2007 출시와 함께 Microsoft에서 도입한 잘 알려진 Microsoft Excel 문서 형식입니다. [Part 2](https://www .ecma-international.org/publications/standards/Ecma-376.htm) OOXML 표준 ECMA-376의 새 형식은 여러 XML 파일을 포함하는 zip 패키지입니다. .xlsx 파일의 압축을 풀면 기본 구조와 파일을 검사할 수 있습니다.

## XLSX 파일 형식의 간략한 역사

XLSX 파일 형식은 2007년에 도입되었으며 2000년에 Microsoft에서 채택한 Open XML 표준을 사용합니다. XLSX 이전에 사용된 일반적인 파일 형식은 순수한 바이너리 파일 형식인 [XLS](/ko/spreadsheet/xls/)였습니다. 새로운 파일 형식은 파일 크기가 작고 손상이 적고 이미지 형식이 잘 표현된다는 장점이 있습니다. Microsoft가 **Office Open XML** 표준을 수용하기 위해 변경하기로 결정한 것은 2000년 초였습니다. 2007년에 이 새로운 파일 형식은 Office 2007의 일부가 되었으며 새 버전의 Microsoft Office에서도 계속 사용됩니다.

## XLSX 파일 형식 사양

공식 [XLSX 파일 형식 사양](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)은 Microsoft에서 온라인으로 제공됩니다. XLSX 파일 내부에 있는 내용을 보려면 확장자를 변경하여 [ZIP](/ko/compression/zip/) 파일로 이름을 바꾼 다음 추출하여 이 Excel 통합 문서의 구성 파일을 봅니다. 파일에 압축을 푼 빈 통합 문서에는 다음과 같은 구성 파일과 폴더가 있습니다.

### [콘텐츠 유형].xml ###

이것은 zip 압축을 풀 때 기본 수준에서 발견되는 유일한 파일입니다. 패키지 내 부품의 콘텐츠 유형을 나열합니다. 패키지에 포함된 XML 파일에 대한 모든 참조는 이 XML 파일에서 참조됩니다.

### \\rels(폴더) ###

패키지 수준 관계를 저장하는 단일 XML 파일이 포함된 관계 폴더입니다. Xlsx 파일의 주요 부분에 대한 링크는 이 파일에 URI로 포함됩니다. 이러한 URI는 패키지에 대한 각 핵심 부분의 관계 유형을 식별합니다. 여기에는 xl/workbook.xml에 있는 기본 사무실 문서와 핵심 및 확장 속성으로 docProps 내의 다른 부분과의 관계가 포함됩니다.

### docProps ###

이 폴더에는 전체 문서 속성이 들어 있습니다. 여기에는 핵심 속성 집합, 확장 또는 응용 프로그램별 속성 집합 및 문서의 축소판 미리 보기가 포함됩니다. 빈 통합 문서에는 이 폴더에 app.xml 및 core.xml이라는 두 개의 파일이 있습니다. core.xml에는 작성자, 생성 및 저장 날짜, 수정된 날짜와 같은 정보가 포함되어 있습니다. App.xml에는 파일 내용에 대한 정보가 포함되어 있습니다.

### xl(폴더) ###

통합 문서 내용에 대한 모든 세부 정보가 포함된 기본 폴더입니다. 기본적으로 다음 폴더가 있습니다.

* \_rels
* 주제
* 워크시트

다음 xml 파일:

* 스타일.xml
* 워크북.xml

## XLSX 형식 예 ##


통합 문서에 포함된 각 Excel 워크시트에는 XML 파일이 하나씩 있습니다. 이러한 XML 파일은 xl/worksheets 폴더에서 찾을 수 있습니다. 워크시트에 포함된 모든 정보는 XML 파일의 다른 섹션으로 구성됩니다. 다음 이미지에 표시된 통합 문서의 샘플 워크시트를 살펴보겠습니다.

{{< figure src="../XLSX file format.png" alt="XLSX 파일 형식" >}}

보시다시피 이 워크시트에는 A1~B2 셀의 내용과 이미지가 포함되어 있습니다. 또한 G13 셀은 현재 워크시트의 활성 셀입니다. 이제 xl/worksheets/sheet1.xml 파일을 검사하여 이 정보가 XML 파일에 어떻게 표시되는지 살펴보겠습니다. 이 XML 파일의 내용은 아래와 같습니다.

{{< figure src="../XLSX File Format Details.png" alt="XPS 파일 형식" >}}

1. 탭에 테마 색상이 적용되어 있습니다. 태그가 있는 XML 파일에 언급되어 있습니다.<tabColor> 테마 ID를 따릅니다.
1. tabSelected 값이 1로 설정되어 이것이 선택된 시트임을 나타냅니다.
1. 위의 첫 번째 이미지에서 볼 수 있듯이 워크시트의 G13 셀은 XML 파일에서도 언급된 활성 셀입니다.
1. sheetData 탭은 워크시트에 포함된 데이터를 나타냅니다. 그러나 이 섹션에는 워크시트의 원래 내용이 없음을 알 수 있습니다. 이는 텍스트가 "sharedStrings" XML 시트에서 간접적으로 참조되기 때문입니다. 이 연결을 통해 각 텍스트는 한 번만 저장되고 공간을 절약하기 위해 다시 참조할 수 있습니다.
1. 보이는 이미지는 참조 ID "rId2"로 참조됩니다.

## 기여하다

XLSX 또는 스프레드시트 파일 형식에 대해 공유해야 합니까? [스프레드시트 파일 형식 뉴스](https://news.fileformat.com/t/Spreadsheet) 섹션에 결과를 게시할 수 있습니다.

## 참고문헌

* [[MS-XLSX] - XLSX 파일 형식](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-xlsx/2c5dee00-eff2-4b22-92b6-0738acd4475e)
* [오픈오피스 XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

