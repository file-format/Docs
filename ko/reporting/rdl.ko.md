{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - 보고서 정의 언어 파일",
  "keywords" :[ "rdl", "보고서 정의 언어", "XmlTextWriter", "XSD", "RDL 요소"],
  "description":"SQL Server Reporting Services 보고서 정의의 XML 표현인 RDL 파일 형식에 대해 알아보세요.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## .RDL 파일이란? ##

RDL(Report Definition Language)은 보고서를 정의하기 위해 Microsoft에서 설정한 벤치마크입니다. RDL 파일은 하나 이상의 RDL 요소로 구성됩니다. 반면 RDL 요소는 데이터 유형과 카디널리티로 구성됩니다. 요소는 단순하거나 복잡할 수 있습니다. 단순 요소에는 자식 요소 또는 속성이 없는 반면 복합 요소에는 자식 및 선택적 속성이 있습니다.

## RDL XML 스키마 정의
XSD(XML 스키마 정의) 파일은 RDL 파일의 유효성을 검사합니다. 스키마는 .rdl 파일에서 RDL 요소가 발생할 수 있는 위치에 대한 규칙을 정의합니다. RDL 요소는 단순하거나 복잡할 수 있습니다. 단순 요소에는 하위 요소나 속성이 없고 복합 요소에는 하위 요소와 선택적으로 속성이 있습니다.

## RDL 생성
RDL은 본질적으로 개방적이고 확장 가능하기 때문에 XML 스키마를 기반으로 RDL 파일을 생성하는 많은 애플리케이션과 도구를 구축할 수 있습니다. 응용 프로그램에서 RDL을 만드는 가장 간단한 방법 중 하나는 **System.Xml** 네임스페이스 및 System.Linq 네임스페이스의 Microsoft .NET Framework 클래스를 사용하는 것입니다. 특히 **XmlTextWriter** 클래스는 RDL을 작성하는 데 사용할 수 있습니다. **XmlTextWriter**를 사용하여 모든 .NET Framework 응용 프로그램에서 처음부터 끝까지 완전한 보고서 정의를 생성할 수 있습니다. 개발자는 사용자 지정 속성이 있는 사용자 지정 보고서 항목을 추가하여 RDL을 확장할 수도 있습니다.

## RDL 유형
다음 표에는 RDL 요소에 사용되는 유형 및 속성이 나열되어 있습니다.

|유형|설명|
---|---|
|Binary |base-64로 인코딩된 이진 값이 있는 속성입니다.|
|부울| 객체의 값이 true 또는 false인 속성입니다. 달리 지정하지 않는 한 생략된 선택적 부울 개체의 값은 False입니다.|
|날짜 |완전히 지정된 날짜 또는 날짜/시간 값이 ISO8601 날짜 형식으로 지정된 특성: YYYY-MM-DD[THH:MM[:SS[.S]]].|
|열거형 |지정된 값 목록 중 하나여야 하는 문자열 텍스트 값이 있는 속성.|
|Float |플로트 값이 있는 속성. 마침표(.)는 선택적 소수 구분 기호로 사용됩니다.|
|정수 |정수(int32) 값을 가진 속성입니다.|
|Language |미국 영어의 경우 "en-us"와 같이 언어 및 문화 코드가 포함된 텍스트 값이 있는 속성입니다. 값은 Microsoft .NET Framework에서 기본 언어가 정의된 특정 언어 또는 중립 언어여야 합니다.|
|이름 |문자열 텍스트 값이 있는 속성. 이름은 항목의 네임스페이스 내에서 고유해야 합니다. 지정하지 않으면 항목의 네임스페이스는 이름이 있는 가장 안쪽에 있는 포함 개체입니다.|
|NormalizedString |정규화된 문자열 텍스트 값이 있는 속성입니다.|
|크기 |크기 요소는 숫자를 포함해야 합니다(선택적인 소수 구분 기호로 사용되는 마침표 문자 포함). 숫자 뒤에 cm, mm, in, pt 또는 pc와 같은 CSS 길이 단위 지정자가 와야 합니다. 숫자와 지정자 사이의 공백은 선택 사항입니다. 크기 지정자에 대한 자세한 내용은 CSS 값 및 단위 참조를 참조하세요. RDL에서 크기의 최대값은 160인치입니다. 최소 크기는 0인치입니다.|
|문자열 |문자열 텍스트 값이 있는 속성|
|UnsignedInt |부호 없는 정수(uint32) 값을 가진 속성입니다.|
|변형 |간단한 XML 유형의 속성입니다.|

## RDL 데이터 유형
RDL에서 DataType 열거는 속성, 표현식 또는 매개변수의 데이터 유형을 정의합니다. 다음 표는 CLR 데이터 유형이 RDL 데이터 유형에 어떻게 대응하는지 보여줍니다.

|CLR 유형 |해당 데이터 유형|
---|---|
|부울| 부울|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, 바이트, SByte |정수|
|싱글, 더블 |플로트|
|문자열, 문자, GUID, 시간 범위 |문자열|


## 참조 ##

- [보고서 정의 언어(위키피디아)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [보고서 정의 언어(SSRS)](https://docs.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

