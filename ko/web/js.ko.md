---
date: 2019-10-11
keywords: js, .js, js 파일 형식, js 파일 여는 방법, javascript 파일
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: JS 파일 형식
linktitle: JS
description: "JS 파일 형식과 JS 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "web"
lastmod: 2020-02-12
---

## .JS 파일이란? ##

JS(JavaScript)는 웹 페이지에서 실행하기 위한 JavaScript 코드를 포함하는 파일입니다. JavaScript 파일은 .js 확장자로 저장됩니다. [HTML](/ko/web/html/) 문서 내에서 \ <script>\</script> 태그를 추가하거나 JS 파일을 포함합니다. [CSS](/ko/web/css/) 파일과 유사하게 JS 파일은 코드 재사용성을 위해 여러 HTML 문서에 포함될 수 있습니다. JavaScript는 HTML DOM을 조작하는 데 사용할 수 있습니다.

## 간략한 역사 ##

JavaScript는 Netscape에서 LiveScript라는 이름으로 1995년 9월에 Navigator Browser의 일부로 처음 출시되었습니다. 3개월 후 자바스크립트로 이름이 바뀌었습니다. 1996년에 Microsoft는 JScript를 만들기 위해 Navigator의 인터프리터를 역설계했습니다. JScript는 Internet Explorer와 함께 출시되었으며 JavaScript와 매우 다릅니다.

Netscape는 JavaScript를 ECMA International에 제출하여 1997년 첫 번째 ECMAScript 사양의 공식 릴리스로 이어졌습니다. ECMAScript 2는 1998년에, ECMAScript 3은 1999년에 릴리스되었으며 ECMAScript 4에 대한 작업은 2000년에 시작되었지만 결실을 맺지 못했습니다.

2005년 Jesse James Garrett은 *Ajax*라는 용어를 만든 백서를 발표했습니다. 이것은 JavaScript를 백본으로 사용하여 백그라운드에서 데이터를 로드하고 전체 페이지 다시 로드를 방지하는 웹 응용 프로그램을 만들었습니다. 그 결과 JQuery, Prototype, Dojo 등과 같은 라이브러리가 생성되었습니다.

Google은 2008년에 V8 JavaScript 엔진이 있는 Chrome 브라우저를 출시했습니다. 2009년 초에 모든 관련 작업을 결합하고 JavaScript를 발전시키기로 합의했습니다. 그 결과 2009년 12월 ECMAScript 5 Standard가 출시되었습니다.

## JS 파일 사용법 ##

JS 파일을 사용하려면 HTML 문서에 포함해야 합니다. 링크 태그를 사용하여 아래와 같이 파일을 포함합니다.

```html
<script src="site.js"></script>
```

*script* 태그의 *src* 속성에는 JS 파일의 경로가 포함됩니다. 이렇게 하면 JS 기능이 HTML 문서에 추가됩니다.

## JS 구문 ##

JavaScript 파일에는 변수, 연산자, 함수, 조건, 루프, 배열, 객체 등이 포함될 수 있습니다. 다음은 JavaScript 구문에 대한 간략한 개요입니다.

- 각 명령은 세미콜론(;)으로 끝납니다.
- *var* 키워드를 사용하여 변수를 선언합니다.
- 산술 연산자( + - * / )를 지원하여 값을 계산합니다.
- 한 줄 주석은 //로 추가되고 여러 줄 주석은 /* 및 */로 둘러싸여 있습니다.
- 모든 식별자는 대소문자를 구분합니다. 즉 *modelNo*와 *modelno*는 서로 다른 두 변수입니다.
- 함수는 *function* 키워드를 사용하여 정의됩니다.
- 배열은 대괄호 []를 사용하여 정의할 수 있습니다.
- JS는 ==, !=, >=, !== 등과 같은 비교 연산자를 지원합니다.
- 클래스는 *class* 키워드를 사용하여 정의할 수 있습니다.

## JS 사용 예 ##

다음은 간단한 사용 예제 JavaScript 파일을 보여줍니다.

### HTML 문서 ###

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>JS Test</title>
    <script src="main.js"></script>
</head>

<body>
    <div class="content-wrapper">
        <h1 id="heading">Test document for JS testing</h1>
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Accusantium officia similique illum magni explicabo,
            tempore neque nulla laborum voluptas sint molestias libero et corporis omnis asperiores incidunt,
            perferendis
            sed aut!</p>

            <button type="button" onclick="showAlert()">Show Alert</button>
            <button type="button" onclick="updateHeading()">Update Heading</button>
    </div>
</body>

</html>
```

### JS 코드 ###

```js
function showAlert() {
    alert("Alert from JS file");
}

function updateHeading() {
    document.getElementById('heading').innerHTML = 'Heading changed with JS';
}
```

## 참조 ##

- [JS - 위키백과](https://en.wikipedia.org/wiki/JavaScript)

