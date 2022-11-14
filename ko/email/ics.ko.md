{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar 파일 형식",
  "description":"ICS 파일을 만들고 열 수 있는 ICS 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .ICS 파일이란?

iCalendar(Internet Calendaring and Scheduling Core Object Specification)는 일정 이벤트와 일정을 교환하고 배포하기 위한 인터넷 표준(RFC 2445)입니다. iCalendar 형식은 상호 운용 가능하므로 다른 이메일 응용 프로그램을 사용하는 사용자 간에 일정 정보를 교환할 수 있습니다. iCalendar는 입력 데이터를 MIME(Multipurpose Internet Mail Extensions) 형식으로 지정하고 다른 전송 프로토콜을 통해 교환되는 개체를 용이하게 합니다. 이러한 전송 프로토콜은 SMTP, HTTP, 지점간 비동기 통신 및 물리적 미디어 기반 네트워크 전송이 될 수 있습니다.

iCalendar를 사용하면 사용자가 이메일을 통해 이벤트, 날짜/시간 종속 작업 및 약속 있음/없음 정보를 회신할 수 있는 다른 사용자와 공유할 수 있습니다. iCalendar 파일은 "텍스트/캘린더"의 MIME 유형과 함께 ".ics" ".iCalendar" 또는 ".ifb" 접미사를 사용하여 저장합니다. iCalendar는 전송 프로토콜 종속성 없이 자체적으로 유지됩니다. 웹 서버(HTTP 프로토콜 포함)는 iCalendar 정보를 전송할 수 있으며 웹 페이지는 iCalendar를 사용하여 내장된 형태로 iCalendar 데이터를 포함할 수 있습니다.

## ICS 파일 형식의 간략한 역사

1998년 IETF(Internet Engineering Task Force)는 iCalendar를 표준(RFC 2445)으로 정의했습니다. 이 표준은 Frank Dawson(Lotus Notes Corporation)과 Derik Stenerson(Microsoft)에 의해 문서화되었습니다. 2009년에 표준은 Bernard Desruisseaux(Oracle)에 의해 RFC 5545로 다시 수정되었습니다. 이번에는 몇 가지 새로운 기능이 추가되었고 일부 오래된 기능은 더 이상 사용되지 않습니다. 2016년에 RFC 7986이 릴리스되어 원래 iCalendar RFC로 확장되었습니다. RFC 7986은 주요 VCALENDAR 개체에 새로운 특성을 추가했으며 회의 시스템을 위한 새로운 지원 기능도 도입되었습니다.

## ICS 파일 형식 ##

iCalendar의 데이터가 사용하는 MIME 타입은 “text/calendar”입니다. iCalendar의 기본 문자 집합은 UTF-8이지만 MIME에 매개변수를 제공하여 다른 문자 집합을 사용할 수 있습니다. iCalendar 파일에는 이러한 섹션 중 "VCALENDAR"가 포함되어 있으며 다른 모든 섹션을 캡슐화하는 전역 섹션입니다. VEVENT 섹션은 이벤트를 정의하고, VTODO는 모든 할일 항목을 나열하고, VJOURNAL은 저널 항목을 포함하고, VTIMEZONE은 시간대 정보를 지정합니다. 유사한 카테고리의 여러 섹션이 허용됩니다. 여러 이벤트의 경우 iCalendar 파일에 여러 VEVENT 섹션이 있을 수 있습니다.

### 콘텐츠 라인 ###

iCalendar 개체는 "콘텐츠 줄"이라는 고유한 텍스트 줄로 정렬됩니다. 이 파일 형식에서 CRLF 시퀀스는 줄을 종료하는 반면 줄 길이는 줄 바꿈을 제외하고 75옥텟으로 제한됩니다. 긴 데이터 항목은 여러 줄에 걸쳐 있을 수 있습니다.

### 목록 및 필드 구분 기호 ###

속성 및 매개변수는 쉼표 문자로 구분된 값 목록을 지정합니다. 인용된 문자열은 URI 기반 매개변수 값에 사용됩니다. 매개변수 목록은 속성 값으로 구성할 수 있습니다. 이 목록의 각 속성 매개변수는 SEMICOLON으로 구분해야 합니다.

값 목록에서 SEMICOLON은 특성 매개변수를 분리하고 쉼표는 특성 값을 분리합니다. 예는 아래와 같습니다.

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### 여러 값

일부 속성은 여러 값을 가질 수 있습니다. 속성 이름으로 새 콘텐츠 줄을 생성하기만 하면 다중 값 속성의 기본 규칙입니다. 그러나 여러 언어 변형이 있는 단일 값의 경우 다중 값 속성을 사용해서는 안 됩니다.

### 바이너리 콘텐츠

iCalendar 개체 내에서 속성 값은 URI를 사용하여 외부 MIME 엔터티에 배치된 이진 콘텐츠 데이터를 참조할 수 있습니다. 인라인 이진 콘텐츠는 "ENCODING" 매개변수가 있는 특별한 상황에서 사용할 수 있습니다. 여기서 응용 프로그램은 iCalendar 개체를 단독 엔터티로 표현해야 합니다. 다음 예에서는 URI 참조가 있는 "ATTACH" 속성을 설명합니다.

첨부: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### 문자 집합

iCalendar의 기본 문자 집합 체계는 UTF-8이지만 속성 값의 문자 집합을 정의하기 위해 속성 매개 변수가 지정되지 않았습니다. MIME 전송에서 "charset" 매개변수는 기존 charset에 사용해야 합니다(MUST).

## 참고문헌

* [Internet Calendaring and Scheduling Core Object Specification](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar(RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

