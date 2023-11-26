{
  "date" : "2023-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"DTSX 파일을 생성하고 열 수 있는 DXL 파일 형식과 API에 대해 알아보세요.",
  "title" :"DXL 파일 형식 - Domino XML 언어 파일 형식",
  "linktitle" : "DXL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-16"
}

## .DXL 파일이란?

DXL 파일은 엔터프라이즈 수준의 비즈니스 협업 소프트웨어인 Lotus Domino용으로 생성된 XML 기반 데이터 저장 파일입니다. 여기에는 스키마, 디자인 요소, 보기, 양식, 문서 및 데이터베이스 데이터 자체와 같은 Lotus Domino 데이터베이스와 관련된 데이터가 포함됩니다. [XML](/ko/web/xml/)은 모든 프로그래밍 언어로 작성된 소프트웨어 응용 프로그램에서 읽을 수 있는 범용 파일 형식입니다. 또한 사람이 읽을 수 있으며 텍스트 편집기로 열 수 있습니다. 이것이 DXL 파일이 상호 교환 가능한 파일 형식으로 데이터를 내보내는 기능을 제공하는 이유입니다.

## DXL 파일 형식

DXL 파일은 XML 파일 형식으로 저장되며 모든 프로그래밍 언어로 작성된 응용 프로그램에서 쉽게 읽을 수 있습니다. 이러한 파일은 데이터를 분류하고 적절한 순서로 정렬하는 XML 태그에 데이터와 설정을 저장합니다.

### DXL 출력 예

다음은 Notes 문서에 대한 출력 텍스트 발췌 출력입니다.

```
<document form="Customers">
	<noteinfo noteid="942" unid="431A199A6FCC9C0985256A54005041A1" sequence="1">
		<created>
			<datetime dst="true">20010522T103636,81-04</datetime>
		</created>
		<modified>
			<datetime dst="true">20010522T103709,78-04</datetime>
		</modified>
		<revised>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</revised>
		<lastaccessed>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</lastaccessed>
		<addedtofile>
			<datetime dst="true">20010522T103709,77-04</datetime>
		</addedtofile>
	</noteinfo>
	<updatedby>
		<name>CN=Michelle Lally/OU=CAM/O=Acme</name>
	</updatedby>
	<item name="date">
		<datetime>20010601</datetime>
	</item>
	<item name="name">
		<text>Harry Hill</text>
	</item>
	</document>
```

## 참고자료

* [DXL 형식 - Microsoft](https://help.hcltechsw.com/dom_designer/9.0.1/appdev/H_EXAMPLE_DOCUMENT_NOTEINFO_AND_ITEM_ELEMENTS_XML.html)

