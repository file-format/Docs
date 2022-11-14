{
  "date" : "2019-12-10",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"_XLSX 파일을 만들고 열 수 있는 API와 _XLSX 파일이 무엇인지 알기 위한 파일 형식 가이드",
  "title" :"_XLSX 파일이란?",
  "linktitle" : "_XLSX",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-11-22"
}

## _XLSX 파일이란?

확장자가 .\_xlsx인 파일은 실제로 다른 응용 프로그램에서 이름을 바꾼 [XLSX](/ko/spreadsheet/xlsx/) 파일입니다. 이는 파일 이름에 . 파일 이름 끝에 . \_XLSX 파일은 다시 .xlsx 확장자로 이름을 변경하여 XLSX 파일과 유사한 Microsoft Excel에서 열 수 있습니다.

## _XLSX 파일 형식 - 추가 정보

_XLSX 파일은 XLSX 파일과 다르지 않으며 2000년에 Microsoft에서 채택한 Open XML 표준을 사용합니다. XLSX 이전에는 [XLS](/ko/spreadsheet/xls/)가 Excel 스프레드시트를 사용하여 문서를 저장하는 데 사용되는 기본 파일 형식이었습니다. 바이너리 형식으로. 이 새로운 XML 기반 파일 형식은 작은 파일 크기, 파일 손상 방지 및 올바른 형식의 이미지 표현과 같은 이점이 있습니다. 이 새로운 XML 기반 파일 형식은 Office 2007의 일부가 되었으며 새 버전의 Microsoft에서도 수행됩니다.

## \\XLSX 파일 형식 사양

\_XLSX 파일은 이름이 변경된 XLSX 파일이므로 원본 파일과 동일한 사양을 갖습니다. [ZIP](/ko/compression/zip/) 아카이브 파일 형식을 기반으로 하는 아카이브 파일일 뿐입니다. 이 아카이브의 내용을 보려면 파일 이름을 .zip 확장자로 바꾸고 압축을 풀면 이 Excel 통합 문서의 구성 파일을 볼 수 있습니다. 파일에 압축을 푼 빈 통합 문서에는 다음과 같은 구성 파일과 폴더가 있습니다.

### [콘텐츠 유형].xml

이것은 zip 압축을 풀 때 기본 수준에서 발견되는 유일한 파일입니다. 패키지 내 부품의 콘텐츠 유형을 나열합니다. 패키지에 포함된 XML 파일에 대한 모든 참조는 이 XML 파일에서 참조됩니다.

### \\rels(폴더)

패키지 수준 관계를 저장하는 단일 XML 파일이 포함된 관계 폴더입니다. Xlsx 파일의 주요 부분에 대한 링크는 이 파일에 URI로 포함됩니다. 이러한 URI는 패키지에 대한 각 핵심 부분의 관계 유형을 식별합니다. 여기에는 xl/workbook.xml에 있는 기본 사무실 문서와 핵심 및 확장 속성으로 docProps 내의 다른 부분과의 관계가 포함됩니다.

### docProps

이 폴더에는 전체 문서 속성이 들어 있습니다. 여기에는 핵심 속성 집합, 확장 또는 응용 프로그램별 속성 집합 및 문서의 축소판 미리 보기가 포함됩니다. 빈 통합 문서에는 이 폴더에 app.xml 및 core.xml이라는 두 개의 파일이 있습니다. core.xml에는 작성자, 생성 및 저장 날짜, 수정된 날짜와 같은 정보가 포함되어 있습니다. App.xml에는 파일 내용에 대한 정보가 포함되어 있습니다.

### xl(폴더)

통합 문서 내용에 대한 모든 세부 정보가 포함된 기본 폴더입니다. 기본적으로 다음 폴더가 있습니다.

* \_rels
* 주제
* 워크시트

다음 xml 파일:

* 스타일.xml
* 워크북.xml

## 참고문헌

* [MS-XLSX - .xlsx 파일 형식](https://msdn.microsoft.com/en-us/library/dd922181(v#office.12).aspx)
* [오픈오피스 XML](http://officeopenxml.com/anatomyofOOXML-xlsx.php)

