{
  "date" : "2022-10-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDM 파일 - 휴대용 장치 마크업 언어 파일",
  "description":"HDM 파일을 만들고 열 수 있는 HDM 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "HDM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-10-12"
}

## .HDM 파일이란?

HDM 파일은 HDML(Handheld Device Markup Language)로 생성되는 마크업 언어 웹페이지 파일입니다. [HTML](/ko/web/html/) 언어와 유사한 마크업 태그가 포함되어 있지만 스마트폰 및 PDA와 같은 휴대용 전자 장치용으로 설계되었습니다. [HDML 파일 형식 사양](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)이 표준화를 위해 W3C에 제출되었지만 표준이 되지 못했습니다. HDM은 W3 웹사이트에서 제공되는 [HDML](/ko/web/hdml/) 파일 형식 사양을 기반으로 합니다.

## HDM 파일 형식 - 추가 정보

HDM 파일은 휴대용 장치에서 시각적으로 디자인된 웹 사이트에 렌더링되는 마크업 태그로 구성됩니다. HDM 파일은 HTML 페이지에 사용되는 HTTP 프로토콜 대신 HDTP(휴대용 장치 전송 프로토콜) 프로토콜을 사용하여 장치에 복사됩니다.

## HDML 파일 요소

다음은 HDML을 위한 런타임 환경을 제공하는 몇 가지 요소이며 사용자 에이전트라고 합니다.

|요소|설명|
---|---|
|카드|이것은 HDML의 기본 빌딩 블록이며 사용자가 정보 카드를 표시하고 상호 작용할 수 있도록 합니다. |
|덱|HDML 카드는 덱으로 함께 그룹화됩니다. HDML 데크는 URL [RFC1738]로 식별되고 서버에서 요청하고 사용자 에이전트가 캐시하는 콘텐츠 단위라는 점에서 HTML 페이지와 유사합니다.|
|액션|액션은 PREV, SOFT1-SOFT8 및 HELP 유형일 수 있습니다. 이들은 추상적이며 사용자 에이전트 특정 방식으로 사용자 인터페이스에서 지원됩니다.|
|활동|활동은 하나의 논리적 기능을 수행하는 관련 카드 그룹과 같습니다. 이들은 하나 이상의 데크에 걸쳐 있을 수 있습니다. HDML 탐색 및 상태 모델은 활동을 중심으로 구성됩니다.|
|이력 기반 탐색|사용자 에이전트는 사용자에게 표시되는 카드의 이력을 유지 관리합니다. 액세스한 각 카드는 카드 내역에 추가됩니다. 사용자 에이전트를 사용하면 사용자가 기록의 이전 카드로 쉽게 돌아갈 수 있습니다.|

## 참고문헌

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML 사양 - W3 학교](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

