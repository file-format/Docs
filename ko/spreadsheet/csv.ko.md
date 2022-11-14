{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "파일", "확장자", "파일 형식", "쉼표로 구분된 값", "스프레드시트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"CSV 파일 형식과 CSV 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"CSV 파일 형식",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## CSV 파일이란?

.csv(쉼표로 구분된 값) 확장자를 가진 파일은 쉼표로 구분된 값을 가진 데이터 레코드를 포함하는 일반 텍스트 파일을 나타냅니다. CSV 파일의 각 줄은 파일에 포함된 레코드 집합의 새 레코드입니다. 이러한 파일은 한 스토리지 시스템에서 다른 스토리지 시스템으로 데이터를 전송할 때 생성됩니다. 모든 응용 프로그램은 쉼표로 구분된 레코드를 인식할 수 있으므로 이러한 데이터 파일을 데이터베이스로 가져오는 것이 매우 편리합니다. Microsoft Excel 또는 OpenOffice Calc와 같은 거의 모든 스프레드시트 응용 프로그램은 큰 노력 없이 CSV를 가져올 수 있습니다. 이러한 파일에서 가져온 데이터는 사용자에게 표시할 수 있도록 스프레드시트의 셀에 정렬됩니다.

## 간략한 역사 ##

다음은 CSV 파일 형식의 기원과 역사에 대한 몇 가지 간단한 사실입니다.

* 1972 - IBM Fortran(레벨 H 확장) 컴파일러가 OS/360에서 지원

* 1978 - 구분 기호에 쉼표와 공백을 사용하는 FORTRAN 77에서 목록 지정 입력/출력이 지원되었습니다.

* 2005 - CSV는 MIME 콘텐츠 유형으로 [RFC4180](https://tools.ietf.org/html/rfc4180)으로 표준화되었습니다.

* 2013 - RFC4180의 결함은 W3C 권장 사항에 의해 처리되었습니다.

* 2015 - W3C는 2015년 12월 권고로 시작된 CSV-메타데이터 표준에 대한 권고의 첫 번째 초안을 작성했습니다.

## CSV 파일 변환 ##

CSV 파일은 이러한 파일을 열 수 있는 응용 프로그램을 사용하여 여러 다른 파일 형식으로 변환할 수 있습니다. 예를 들어 Microsoft Excel은 CSV 파일 형식에서 데이터를 가져와 XLS, [XLSX](/ko/spreadsheet/xlsx/), [PDF](/ko/pdf/), [TXT](/ko/word-processing/txt/)에 저장할 수 있습니다. , XML 및 [HTML](/ko/web/html/) 파일 형식. 마찬가지로 다른 데스크톱 및 온라인 서비스는 CSV 파일을 HTML, ODS 및 [RTF](/ko/word-processing/rtf/)로 내보내는 기능을 제공합니다.

## CSV 파일 형식 ##

CSV 파일 형식은 [RFC4180](https://tools.ietf.org/html/rfc4180)에 지정되어 있는 것으로 알려져 있습니다. 다음과 같은 경우 CSV를 준수하도록 모든 파일을 정의합니다.

* 각 레코드는 줄 바꿈(CRLF)으로 구분된 별도의 줄에 있습니다. 예를 들어:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* 파일의 마지막 레코드에는 끝 줄 바꿈이 있을 수도 있고 없을 수도 있습니다. 예를 들어:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* 일반 레코드 라인과 동일한 형식으로 파일의 첫 번째 라인으로 나타나는 선택적 헤더 라인이 있을 수 있습니다. 이 헤더는 파일의 필드에 해당하는 이름을 포함하고 파일의 나머지 부분에 있는 레코드와 동일한 수의 필드를 포함해야 합니다(헤더 행의 존재 여부는 이 파일의 선택적 "헤더" 매개변수를 통해 표시되어야 합니다. MIME 유형). 예를 들어:
* field_name,field_name,field_name CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿헤더와 각 레코드 내에는 쉼표로 구분된 하나 이상의 필드가 있을 수 있습니다. 각 줄은 파일 전체에서 동일한 수의 필드를 포함해야 합니다. 공백은 필드의 일부로 간주되며 무시하면 안 됩니다. 레코드의 마지막 필드 뒤에 쉼표가 오면 안 됩니다. 예를 들어:
* aaa,bbb,ccc
* 각 필드는 큰따옴표로 묶거나 묶지 않을 수 있습니다(단, Microsoft Excel과 같은 일부 프로그램에서는 큰따옴표를 전혀 사용하지 않음). 필드가 큰따옴표로 묶이지 않으면 큰따옴표가 필드 안에 나타나지 않을 수 있습니다. 예를 들어:\
* "aaa", "bbb","ccc" CRLF
* zzz,yyy,xxx
* 줄 바꿈(CRLF), 큰따옴표 및 쉼표가 포함된 필드는 큰따옴표로 묶어야 합니다. 예를 들어:
* "아아아","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* 큰따옴표를 사용하여 필드를 묶는 경우 필드 내부에 나타나는 큰따옴표를 다른 큰따옴표 앞에 붙여 이스케이프 처리해야 합니다. 예를 들어:
* "aaa","b""bb","ccc"

그러나 현대의 사용에 비추어 구분자는 쉼표에만 국한되지 않고 세미콜론, 탭 또는 공백도 될 수 있습니다. Microsoft Excel과 같은 응용 프로그램은 CSV 파일에서 레코드를 가져오기 위한 구분 문자를 지정하는 옵션을 제공합니다.

## 참고문헌

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

