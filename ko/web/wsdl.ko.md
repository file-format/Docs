{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WSDL 파일 형식 - 웹 서비스 설명 언어 파일",
  "description":"WSDL 파일이 무엇이며 WSDL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## .WSDL 파일이란?

WSDL 파일은 웹 서비스를 설명하기 위해 XML 언어로 작성된 웹 서비스 설명 언어 파일입니다. 여기에는 보편적으로 허용되는 형식으로 외부 세계에 연결하기 위한 끝점 또는 인터페이스에 대한 정보가 포함됩니다. [WSDL 파일 형식 사양](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (W3C.org에서 유지) 포트 및 엔드포인트를 통한 원격 애플리케이션 액세스.

## WSDL 파일 형식 - 추가 정보

WSDL 파일은 사람이 읽을 수 있는 XML 파일로 저장되며 모든 텍스트 편집기에서 열어 내용을 볼 수 있습니다.

## WSDL 서비스 설명

WSDL 2.0 파일 형식 사양은 WSDL 서비스가 다음 두 단계로 구성된 것으로 설명합니다.

- 추상 단계
- 콘크리트 스테이지

설명 및 독립적인 관심사 디자인의 재사용성은 웹 서비스에 의해 관리됩니다. 이는 유형(데이터 유형 정의), 메시지(통신된 데이터), 작업(작업) 및 서비스에서 사용하는 프로토콜을 비롯한 여러 유형의 요소를 사용하여 달성됩니다. 이들은 모두 추상적 수준에서 관리됩니다. 전송 및 연결 형식 세부 정보의 바인딩은 공통 인터페이스를 구현하기 위해 끝점을 함께 그룹화하는 바인딩에 의해 지정됩니다.

### WSDL 서비스와 인터페이스하는 데 사용할 수 있는 기술은 무엇입니까?

ASP.NET, C/C++ 및 Java 응용 프로그램을 포함하여 WSDL 서비스와 인터페이스하는 데 여러 다른 기술을 사용할 수 있습니다.

## WSDL 예제

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

이 예에서 portType "glossaryTerms"는 "setTerm"이라는 단방향 작업을 정의합니다.

## 참고문헌

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [WSDL 파일 형식 사양](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

