---
date: 2019-10-11
keywords: sass, .sass, sass 파일 형식, sass 파일을 여는 방법, 구문적으로 멋진 스타일시트, CSS 전처리기, sass
작가:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Sass 파일 형식
linktitle: Sass
description: "Sass 파일을 만들고 열 수 있는 Sass 파일 형식 및 API에 대해 알아봅니다."
menu:
  docs:
    parent: "web"
lastmod: 2021-06-01
---

## .SASS 파일이란? ##

Sass(구문적으로 멋진 스타일 시트)는 전처리기 스크립팅 언어입니다. [CSS](/ko/web/css/)로 컴파일되어 .sass 확장자로 저장됩니다. Sass는 .sass 확장자를 사용하는 들여쓰기를 기반으로 하는 원본과 .scss 확장자를 사용하는 CSS와 같은 블록 형식이 있는 최신 SCSS의 두 가지 구문으로 구성됩니다.

## Sass를 사용하는 이유 ##

Sass는 스타일 작업을 재미있게 만드는 변수 소개, 중첩, 믹스인, 가져오기 및 선택기 상속과 같은 많은 기능을 제공하므로 스타일을 유지하는 데 정말 유용합니다.

## SASS 파일 사용 방법 ##

SASS 파일은 [HTML](/ko/web/html/) 문서에 직접 포함되지 않고 HTML 파일에 포함된 CSS 파일로 변환됩니다. [Sass 공식 사이트](https://sass-lang.com/install)에 제공된 지침에 따라 시스템의 Sass를 설치할 수 있습니다.

Sass는 이미 저장된 SASS 파일을 변환하거나 변경 사항을 관찰하고 파일이 저장될 때 변환하여 CSS로 변환할 수 있습니다. 둘 다에 대한 명령은 아래에 나와 있습니다.

### 한 번 변환 ###

명령의 첫 번째 매개변수는 소스 SASS 파일이고 두 번째 매개변수는 출력 CSS 파일입니다.

```cmd
sass main.sass main.css
```

### 변경 사항 확인 ###

위의 명령은 명령 실행을 유지하는 추가 *watch* 플래그와 함께 실행할 수 있으며 Sass 파일이 저장되자마자 출력 CSS가 생성됩니다.

```cmd
sass --watch main.sass main.css
```

## Sass 구문 ##

Sass는 변수, 중첩, 믹스인, 가져오기, 선택기 상속 등을 지원합니다. 다음은 이러한 기능의 예입니다.

### 변수 ###

변수는 버튼의 기본 색상 또는 패딩과 같은 재사용 가능한 정보를 설정하는 데 사용할 수 있습니다. 이는 나중에 해당 정보를 변경해야 하는 경우 한 위치에서 변경하면 모든 곳에서 업데이트되는 경우 유용할 수 있습니다.

**새스**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

CSS 선택기는 HTML의 계층 구조와 유사하게 중첩될 수 있습니다. 다음 예에서 범위는 h1 블록 내부에 중첩됩니다.

**새스**

```sass
$primary-color: #47dff0
$secondary-color: darken($primary-color, 50%)
$margin: 16px

.highlight
    border-color: $primary-color
    color: $secondary-color

h1
    span
        margin: $margin / 2
    color: $secondary-color
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

믹스인은 여러 위치에서 사용되는 유사한 속성을 함께 그룹화하는 데 사용됩니다. 믹스인은 매개변수도 지원합니다.

**새스**

**mixin 선언**

```sass
// Simple
=error-text
    color: red
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px

// With Parameter
=message-text($color)
    color: $color
    font-size: 25px
    font-weight: bold
    border: 1px solid black
    padding: 10px
```

**믹스인 사용**

```sass
.error
    +error-text()

.success
    +message-text(green)

.info
    +message-text(blue)
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

확장/상속은 한 선택기의 속성을 다른 선택기와 공유해야 하는 경우에 유용할 수 있습니다. 아래 예에서 *.error-notice* 선택기는 *.error-text* 선택기의 모든 속성을 가져오고 테두리 및 패딩 속성을 추가합니다.

**새스**

```sAss
.error-text
    color: red
    font-size: 25px
    font-weight: bold

.error-notice
    @extend .error-text
    border: 1px solid black
    padding: 10px
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

가져오기는 기능 또는 따라야 하는 다른 구조를 기반으로 스타일을 다른 파일로 구조화하는 경우 유용할 수 있습니다. 나중에 CSS로 변환되는 기본 SASS 파일에서 이러한 모든 파일을 가져올 수 있습니다. 가져오는 동안 가져오기 지침에 파일 확장자를 지정할 필요가 없습니다. Sass는 모든 SASS 파일을 직접 컴파일합니다. 가져오기 파일이 직접 컴파일되지 않도록 하려면 이름 시작 부분에 밑줄(_)을 추가하여 파일을 부분 파일로 만들 수 있습니다. 부분은 일반 Sass 파일과 유사하게 가져옵니다.

**새스**

```sass
@import "variables"
@import "header-styles"
@import "footer-styles"
```

출력 CSS에는 가져온 모든 파일의 스타일이 있습니다.

## 참조 ##

- [Sass - Wikipedia](https://en.wikipedia.org/wiki/Sass_(stylesheet_language))
- [사스](https://sass-lang.com/)

