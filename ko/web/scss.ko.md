---
date: 2019-10-11
keywords: scss, .scss, scss 파일 형식, scss 파일을 여는 방법, 구문적으로 멋진 스타일시트, CSS 전처리기, sass
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: SCSS 파일 형식 - Sass 캐스케이딩 스타일 시트
linktitle: SCSS
description: "SCSS 파일 형식 및 SCSS 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    parent: "web"
lastmod: 2020-26-11
---

## .SCSS 파일이란? ##

SCSS는 들여쓰기 대신 대괄호를 사용하는 Sass(Syntactically Awesome Stylesheet)의 두 번째 구문입니다. SCSS는 유효한 CSS3 파일도 유효한 SCSS 파일이 되도록 설계되었습니다. SCSS 파일은 .scss 확장자로 저장됩니다.

## SCSS를 사용하는 이유 ##

웹 사이트의 디자인이 복잡해짐에 따라 대용량 [CSS](/ko/web/css/) 파일이 생성됩니다. 이러한 파일은 유지 관리하기가 더 어렵습니다. 이것이 SCSS가 들어오는 곳입니다. SCSS는 CSS 개발에서 변수, 중첩, 믹스인, 가져오기 및 선택기 상속을 도입합니다. 이러한 추가 기능은 디자인 작업을 훨씬 더 재미있게 만듭니다.

## SCSS 파일 사용 방법 ##

SCSS 파일은 CSS와 같이 [HTML](/ko/web/html/) 문서에 직접 포함되지 않습니다. 대신 SCSS 파일은 HTML 파일에 포함된 CSS 파일로 변환됩니다. 시스템에 SCSS를 설치하려면 [Sass 공식 사이트](https://sass-lang.com/install)의 지침을 따르십시오.
SCSS를 CSS로 변환하려면 이미 저장된 SCSS 파일을 변환하거나 변경 사항을 관찰하고 파일이 저장될 때 변환할 수 있습니다. 둘 다에 대한 명령은 아래에 나와 있습니다.

### 한 번 변환 ###

첫 번째 매개변수는 소스 SCSS 파일이고 두 번째 매개변수는 출력 CSS 파일입니다.

```cmd
sass main.scss main.css
```

### 변경 사항 확인 ###

이 명령에는 명령 실행을 유지하는 추가 *watch** 플래그가 있으며 SCSS 파일이 저장되자마자 출력 CSS가 생성됩니다.

```cmd
sass --watch main.scss main.css
```

## SCSS 구문 ##

SCSS는 변수, 중첩, 믹스인, 가져오기, 선택기 상속 등을 지원합니다. 다음은 이러한 기능의 예입니다.

### 변수 ###

변수를 사용하여 저장 버튼의 기본 색상이나 배경 색상과 같은 재사용 가능한 정보를 설정할 수 있습니다. 이는 해당 정보를 변경해야 하는 경우 유용합니다. 한 위치에서 변경하기만 하면 사용되는 모든 위치에서 업데이트됩니다.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**생성된 CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### 중첩 ###

HTML의 계층 구조와 유사한 CSS 선택기를 중첩할 수 있습니다. 아래 주어진 예에서 범위는 h1 블록 내부에 중첩됩니다.

**SCSS**

```scss
$primary-color: #47dff0;
$secondary-color: darken($primary-color, 50%);
$margin: 16px;

.highlight {
    border-color: $primary-color;
    color: $secondary-color;
}

h1 {
    span {
        margin: $margin / 2;
    }

    color: $secondary-color;
}
```

**생성된 CSS**

```css
.highlight {
  border-color: #47dff0;
  color: #042f34;
}

h1 {
  color: #042f34;
}
h1 span {
  margin: 8px;
}
```

### 믹스인 ###

믹스인은 여러 장소에서 함께 사용되는 유사한 속성을 함께 그룹화하는 데 사용할 수 있습니다. 믹스인에 매개변수를 전달할 수도 있습니다.

**SCSS**

**mixin 선언**

```scss
// Simple
@mixin error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}

// With Parameter
@mixin message-text($color) {
    color: $color;
    font-size: 25px;
    font-weight: bold;
    border: 1px solid black;
    padding: 10px;
}
```

**믹스인 사용**

```scss
.error {
    @include error-text();
}

.success {
    @include message-text(green);
}

.info {
    @include message-text(blue);
}
```

**생성된 CSS**

```css
.error {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.success {
  color: green;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}

.info {
  color: blue;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid black;
  padding: 10px;
}
```

### 연장하다 ###

확장/상속은 한 선택기의 속성을 다른 선택기와 공유해야 하는 경우에 유용합니다. 아래 예에서 *.error-notice* 선택기는 *.error-text* 선택기의 모든 속성을 가져오고 테두리 및 패딩 속성을 추가합니다.

**SCSS**

```scss
.error-text {
    color: red;
    font-size: 25px;
    font-weight: bold;
}

.error-notice {
    @extend .error-text;
    border: 1px solid black;
    padding: 10px;
}
```

**생성된 CSS**

```css
.error-text, .error-notice {
  color: red;
  font-size: 25px;
  font-weight: bold;
}

.error-notice {
  border: 1px solid black;
  padding: 10px;
}
```

### 가져오기 ###

가져오기는 관심사를 분리하는 데 유용할 수 있습니다. 머리글 스타일이 별도의 파일에 있고, 바닥글 스타일이 별도의 파일에 있고, 스타일에 사용된 모든 색상 변수가 별도의 파일에 있는 등의 방식으로 스타일을 나눌 수 있습니다. 이 기술을 사용하면 스타일이 체계적으로 유지됩니다. 아래 예와 같이 기본 SCSS 파일의 파일을 가져오기만 하면 됩니다. 가져오기 명령에 파일 확장자를 지정할 필요가 없습니다. Sass는 모든 SCSS 파일을 직접 컴파일합니다. 가져오기 파일이 직접 컴파일되지 않도록 하려면 파일 이름 앞에 밑줄(_)을 추가하여 부분 파일로 만들 수 있습니다. 밑줄 없이 일반 SCSS 파일과 유사한 부분을 가져올 수 있습니다.

**SCSS**

```scss
@import "variables";
@import "header-styles";
@import "footer-styles";
```

출력 CSS에는 가져온 모든 파일의 스타일이 있습니다.

## 참조 ##

- [SCSS - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [사스](https://sass-lang.com/)

