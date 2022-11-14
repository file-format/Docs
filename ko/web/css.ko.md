---
date: 2019-10-11
keywords: CSS, .css, CSS 파일 형식, CSS 파일을 여는 방법, CSS 스타일 시트
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: CSS 파일 형식
linktitle: CSS
description: "CSS 파일 형식과 CSS 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## CSS 파일이란? ##

CSS(Cascading Style Sheets)는 HTML 요소가 화면, 종이 등에 표시되는 방식을 설명하는 파일입니다. HTML을 사용하면 내장된 스타일을 가질 수 있거나 외부 스타일시트에 스타일을 정의할 수 있습니다. 스타일을 포함하려면 \ <style>\</style> 태그가 사용됩니다. 외부 스타일시트는 확장자가 .css인 파일에 저장됩니다. 외부 CSS를 사용하면 여러 HTML 페이지에 CSS를 포함하여 해당 페이지의 스타일을 업데이트할 수 있습니다. 단일 CSS 파일로도 전체 웹사이트의 스타일을 지정할 수 있습니다.

## 간략한 역사 ##

CSS1은 Bert Bos가 공동 저자로 1996년에 발표되었습니다. CSS Working Group은 CSS1에서 다루지 않은 문제에 대한 작업을 시작했습니다. 그 결과 1998년 5월 12일 W3C 권장 사항으로 게시된 1997년 11월 CSS2가 생성되었습니다. 이 버전에는 프린터, 다운로드 가능한 글꼴, 표 및 요소 위치 지정과 같은 미디어 관련 장치에 대한 지원이 추가되었습니다. 1999년 6월 CSS3는 W3C의 권장 사항이 되었습니다. 이것은 각 모듈에 CSS2에 정의된 확장 기능이 있는 모듈로 문서를 나눴습니다.

## CSS 파일 사용 방법 ##

CSS 파일을 사용하려면 HTML 문서의 헤드 섹션에 포함합니다. 링크 태그를 사용하여 아래와 같이 파일을 포함합니다.

```html
<link rel="stylesheet" type="text/css" href="main.css"/>
```

링크 태그의 *href* 속성에는 CSS 파일의 경로가 포함됩니다. 이렇게 하면 포함된 CSS 파일에 포함된 해당 스타일이 HTML 문서에 적용됩니다.

## CSS 구문 ##

CSS 규칙은 선택자와 선언이라는 두 가지 구성 요소로 구성됩니다. 선택자는 HTML 문서의 요소를 가리킵니다. 요소 태그, 클래스 이름, ID 이름, 계층을 보여주는 여러 태그 등이 될 수 있습니다. 선언에는 속성과 값으로 구성된 스타일 정의가 포함됩니다. 속성은 변경하려는 요소의 속성을 식별하고 값은 새 값을 정의합니다. 각 CSS 규칙에는 여러 선언이 있을 수 있습니다. 다음은 CSS 규칙의 예입니다.

```css
h1{
    font-weight: 700;
    color: forestgreen;
}
```

위의 예에서 HTML 문서의 모든 h1 태그를 선택하는 선택기로 **h1**이 있습니다. 규칙에는 두 가지 선언이 있습니다. 하나는 글꼴 두께에 대한 선언이고 다른 하나는 색상에 대한 선언입니다. *font-weight* 및 *color*는 속성이고 *700* 및 *forestgreen*은 각각 값입니다.

## CSS 사용 예 ##

다음은 예제 HTML 문서와 스타일시트를 스타일 지정하는 데 사용되는 스타일시트를 보여줍니다. 스타일이 지정된 HTML 문서와 일반 HTML 문서를 비교하기 위해 비교 이미지도 추가되었습니다.

### HTML 문서 ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="main.css" type="text/css">
    <title>CSS Test</title>
</head>

<body>
    <div class="content-wrapper">
        <h1>Test document to test <span class="highlight">CSS</span></h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

        <h2>List of items</h2>
        <ul>
            <li>Item 1</li>
            <li>Item 2</li>
            <li>Item 3</li>
            <li>Item 4</li>
            <li>Item 5</li>
        </ul>
    </div>
</body>

</html>
```

### CSS 스타일시트 ###

```css
body{
    background-color: lightblue;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
.content-wrapper{
    padding: 10px 30px;
}
p{
    text-align: justify;
}
h1{
    text-align: center;
}
.highlight{
    font-weight: 700;
    color: forestgreen;
}
h1, h2{
    font-weight: 400;
}

ul li{
    list-style-type: square;
    margin-bottom: 10px;
    margin-left: 50px;
}
```

### 출력 비교 ###

이미지의 왼쪽에는 스타일이 적용되지 않은 HTML 문서가 표시되고 오른쪽에는 스타일이 적용된 HTML 문서가 표시됩니다.

{{< figure src="../CssExample.jpg" alt="예시 이미지" >}}

## 참조 ##

- [CSS - 위키백과](https://en.wikipedia.org/wiki/CSS)

