---
date: 2019-10-11
keywords: json, .json, json 파일 형식, json 파일 여는 방법, javascript 객체 표기법, json 데이터 형식, .json 파일 형식
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JSON 파일 형식 - JSON 파일이란?
linktitle: JSON
description: "JSON 파일을 생성하고 열 수 있는 JSON 파일 형식 및 API에 대해 알아봅니다."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## JSON 파일이란?

JSON(JavaScript Object Notation)은 사람이 읽을 수 있는 텍스트를 사용하여 데이터를 저장하고 전송하는 데이터 공유를 위한 개방형 표준 파일 형식입니다. JSON 파일은 .json 확장자로 저장됩니다. JSON은 형식이 덜 필요하며 [XML](/ko/web/xml/)에 대한 좋은 대안입니다. JSON은 JavaScript에서 파생되지만 언어 독립적인 데이터 형식입니다. JSON의 생성 및 구문 분석은 많은 최신 프로그래밍 언어에서 지원됩니다. *application/json*은 JSON에 사용되는 미디어 유형입니다.

## JSON 파일 형식 - 간략한 역사

JSON 생성으로 이어지는 실시간 서버 간 통신이 필요했습니다. JSON 형식은 2001년 3월 Douglas Crockford에 의해 처음 지정되었습니다. JSON은 JavaScript의 하위 집합인 Standard ECMA-262 3rd Edition(1999년 12월)을 기반으로 합니다.

JSON 표준 ECMA-404의 초판은 2013년 10월 Ecma International에서 발행되었습니다. RFC 7159는 2014년 JSON의 인터넷 사용에 대한 주요 참조가 되었습니다. 2017년 11월 ISO/IEC 21778:2017이 국제 표준으로 발행되었습니다. RFC 8259는 2017년 12월 13일 인터넷 표준 STD 90의 최신 버전인 Internet Engineering Task Force에서 게시했습니다.

## JSON 파일 구조

JSON 데이터는 **키/값** 쌍으로 작성됩니다. 키와 값은 중간에 콜론(:)으로 구분되며 왼쪽에는 키, 오른쪽에는 값이 있습니다. 다른 키/값 쌍은 쉼표(,)로 구분됩니다. 키는 "name"과 같이 큰따옴표로 묶인 문자열입니다. 값은 다음 유형일 수 있습니다.

- '번호'
- `String`: 큰따옴표로 묶인 유니코드 문자 시퀀스입니다.
- '부울': 참 또는 거짓.
- `Array`: 예를 들어 대괄호로 묶인 값 목록

```json
[ "사과", "바나나", "오렌지" ]
```

- `Object`: 예를 들어 중괄호로 묶인 키/값 쌍의 모음

```json
{"name": "Jack", "age": 30, "favoriteSport": "Football"}
```

JSON 객체는 데이터 구조를 나타내기 위해 중첩될 수도 있습니다. 아래는 JSON 객체의 예입니다.

### JSON 형식 예

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## JSON 파일의 최대 크기는 얼마입니까?

JSON 파일의 최대 크기에는 사실상 제한이 없습니다. 콘텐츠에 필요한 공간만큼 저장될 수 있습니다.

인터넷을 통해 데이터를 전송하기 위해 JSON 파일 형식을 사용하는 경우 컴퓨터의 사용 가능한 리소스에 주의해야 합니다. 대용량 JSON 데이터가 전송되는 경우 클라이언트 브라우저의 메모리가 제한된 경우 전송에 영향을 미칩니다.


사양에 의해 정의된 엄격한 제한은 없지만 사용자 컴퓨터의 리소스를 소진하지 않도록 주의해야 합니다. 사용자 경험이 빠르게 저하되고 앱을 포기할 가능성이 높기 때문입니다.

## JSON 대 XML

**XML**은 인터넷을 통한 데이터 교환을 위해 널리 사용되는 또 다른 파일 형식입니다. 애플리케이션 간의 데이터 교환과 관련하여 개발자는 XML 및 JSON 파일 형식을 모두 사용할 수 있습니다. 그러나 다음과 같은 이유로 인터넷을 통한 응용 프로그램 간의 데이터 교환에 가장 편리한 방법으로 JSON을 채택하고 있습니다.

1. JSON은 XML 파일 형식에 비해 명확하고 읽기 쉬운 데이터 보기를 제공합니다.
1. JSON은 XML에 비해 동일한 데이터 세트를 정의하는 문자 수가 적기 때문에 인터넷을 통한 데이터 전송 오버헤드를 줄입니다.
1. 최신 프로그래밍 언어는 웹을 통해 JSON 응답을 구문 분석하는 내장 파서를 제공합니다.

## 알고 계셨나요?

FileFormat.com에서 기고자가 되어 파일 형식 커뮤니티를 최신 정보로 유지할 수 있습니다. JSON 또는 웹 파일 형식에 대해 공유해야 하는 내용이 있는 경우 [웹 파일 형식 뉴스](https://news.fileformat.com/t/Web) 섹션에 결과를 게시하여 사람들이 더 자세히 알아볼 수 있도록 할 수 있습니다.

## 참고문헌

- [JSON - 위키백과](https://en.wikipedia.org/wiki/CSS)
- [JSON 소개](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

