{
  "date" : "2021-08-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"휴대용 장치 마크업 언어 파일",
  "description":"HDML 파일을 만들고 열 수 있는 HDML 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "HDML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-21"
}

## .HDML 파일이란?

.hdml(휴대용 장치 마크업 언어) 확장자를 가진 파일은 휴대용 컴퓨터, 스마트폰 및 정보 표시 장치와 같은 휴대용 전자 장치용 웹 페이지를 만들기 위한 마크업 언어입니다. HDML은 [SGML](https://en.wikipedia.org/wiki/Standard_Generalized_Markup_Language) 언어의 확장이라고 합니다. HDML은 HTML과 유사하지만 PDA, 휴대폰 등과 같이 작은 디스플레이가 있는 무선 및 핸드헬드 장치에 사용됩니다. 중요한 영향을 미치는 WML로 대체되었습니다.

## HDML 파일 형식 - 추가 정보

HDML은 HTML과 유사한 마크업 태그를 기반으로 하는 휴대용 장치용 마크업 언어입니다. HDML은 표준화를 위해 W3C에 제출되었지만 표준이 되지는 못했습니다. 그러나 파일 형식 사양은 [W3 웹사이트](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)에서 참조용으로 제공됩니다. [HDML 언어 구문](https://www.w3.org/TR/hdml20-5.html#HEADING5-0)은 개발자 참조용으로 제공되며 샘플 애플리케이션 개발에 사용할 수 있습니다.

## HDML 요소

다음은 HDML을 위한 런타임 환경을 제공하는 몇 가지 요소이며 사용자 에이전트라고 합니다.

|요소|설명|
---|---|
|카드|이것은 HDML의 기본 빌딩 블록이며 사용자가 정보 카드를 표시하고 상호 작용할 수 있도록 합니다. |
|덱|HDML 카드는 함께 덱으로 그룹화됩니다. HDML 데크는 URL [RFC1738]로 식별되고 서버에서 요청하고 사용자 에이전트가 캐시하는 콘텐츠 단위라는 점에서 HTML 페이지와 유사합니다.|
|액션|액션은 PREV, SOFT1-SOFT8 및 HELP 유형일 수 있습니다. 이들은 추상적이며 사용자 에이전트 특정 방식으로 사용자 인터페이스에서 지원됩니다.|
|활동|활동은 하나의 논리적 기능을 수행하는 관련 카드 그룹과 같습니다. 이들은 하나 이상의 데크에 걸쳐 있을 수 있습니다. HDML 탐색 및 상태 모델은 활동을 중심으로 구성됩니다.|
|이력 기반 탐색|사용자 에이전트는 사용자에게 표시되는 카드의 이력을 유지 관리합니다. 액세스한 각 카드는 카드 내역에 추가됩니다. 사용자 에이전트를 사용하면 사용자가 기록의 이전 카드로 쉽게 돌아갈 수 있습니다.|

## 참고문헌

* [HDML - Wikipedia](https://en.wikipedia.org/wiki/Handheld_Device_Markup_Language)
* [HDML 사양 - W3 학교](https://www.w3.org/TR/NOTE-Submission-HDML-spec.html)

