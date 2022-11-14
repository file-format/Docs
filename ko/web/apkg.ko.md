{
  "date" : "2019-10-11",
   "keywords" :[ "apkg","apkg 파일", "apkg 파일 형식", "apkg 파일 형식", "파일", "유형", "APKG 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKG - Anki Flashcard 데크 파일 형식",
  "description" :"APG 파일이 무엇이며 이를 생성하고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "APKG",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-16"
}

## .APKG 파일이란?

확장자가 .apkg인 파일은 플래시 카드 기반 학습 프로그램인 [Anki](https://ankiweb.net/about) 소프트웨어 응용 프로그램에서 사용하기 위해 생성된 플래시 카드 데크입니다. Anki 애플리케이션에 로드 및 표시할 [HTML](/ko/web/html/) 텍스트가 포함되어 있으며 시각적 및 청각적 학습을 위한 이미지와 사운드를 추가로 포함할 수 있습니다. Anki를 사용하면 사용자가 자신의 Anki 플래시 카드 데크를 만들고 다른 사용자의 플래시 카드 데크를 가져올 수 있습니다.

## APK 파일 형식

Anki 카드 데크는 웹 페이지를 만들기 위한 유명하고 일반적인 언어인 HTML로 작성된 템플릿으로 만들어집니다. 데크 카드의 스타일 지정은 웹 페이지 스타일 지정에 사용되는 언어인 CSS를 사용하여 수행됩니다. 스타일링에는 다음과 같은 수정 사항이 포함됩니다.

* font-family - 카드에 사용할 글꼴의 이름입니다.
* font-size - 픽셀 단위의 글꼴 크기입니다.
* text-align - 텍스트를 가운데, 왼쪽 또는 오른쪽에 정렬할지 여부를 정의합니다.
* color - "blue", "red" 등과 같은 단순한 색상 이름이나 HTML 색상 코드가 될 수 있는 텍스트 색상을 정의합니다.
* background-color - 카드의 배경색을 정의합니다.

스타일 정보는 모든 카드 간에 공유되며 변경 시 모든 카드에 영향을 줍니다. 다음 예에서는 첫 번째 카드를 제외한 모든 카드에 노란색 배경을 사용합니다.

```CSS
.card {
  background-color: yellow;
}
.card1 {
  background-color: blue;
}
```

Anki 카드에서 이미지 크기 조정은 다음과 같이 제어할 수 있습니다.

```CS
img {
  max-width: none;
  max-height: none;
}
```

## Anki 카드에 자바스크립트 포함

카드 템플릿을 사용하여 Anki 카드에 [Javascript](/ko/web/js/)를 포함할 수 있습니다. 그러나 Javascript의 고급 수준으로 인해 지원이 제공되지 않습니다. 또한 렌더링 장치는 카드에서 Javascript의 구현 영향을 다르게 표시할 수 있으므로 모든 장치에서 구현을 테스트해야 합니다. window.alert와 같은 특정 Javascript 기능으로 인해 작성한 Javascript 코드를 디버그하기 어렵습니다.

## 참조 ##

* [안키 문서](https://docs.ankiweb.net/intro.html)

