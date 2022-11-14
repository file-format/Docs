---
date: 2021-07-05
keywords: ssp, .ssp, ssp 파일 형식, ssp 파일을 여는 방법, Scala 서버 페이지
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - 스칼라 서버 페이지 파일 형식
linktitle: SSP
description: "SSP 파일 형식 및 SSP 파일을 만들고 열 수 있는 API에 대해 알아봅니다."
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## .SSP 파일이란?

확장자가 .ssp인 파일은 일반 HTML 전용이 아닌 표현식용 스칼라 코드로 생성된 웹 페이지입니다. HTML과 Scala의 조합을 사용하여 서버 측 스크립트로 작동합니다. 이 파일은 서버에 상주하며 사용자에게 제공할 정적 웹 페이지를 만드는 데 사용됩니다. Scala 자체는 Velocity, JSP 또는 Erb로 작업한 사용자에게 익숙한 구문을 가진 범용 프로그래밍 언어입니다. SSP 파일은 텍스트 및 마크업 생성을 위한 Scala 기반 템플릿 엔진인 [Scalate](https://scalate.github.io/scalate/)를 사용하여 분석 및 평가할 수 있습니다.

## SSP 파일 형식 - 추가 정보

SSP 파일은 일반 텍스트 파일로 저장되며 Scalate를 사용하여 평가할 수 있습니다. Ssp 템플릿은 HTML 문서인 경우가 더 많은 일반 텍스트로 구성됩니다. 여기에는 렌더링 엔진이 문서의 다른 부분을 동적으로 렌더링하도록 하는 Ssp 태그가 포함되어 있습니다. 태그는 <% ... %> 및 ${ ... } 시퀀스로 시작하고 끝납니다. 이 시퀀스를 벗어나는 모든 것은 리터럴 텍스트로 간주됩니다.

### SSP 예

다음 예제는 렌더링 엔진에서 렌더링할 때 SSP 코드와 그 출력을 보여줍니다.

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
출력은 다음과 같습니다.
```
<p>
  hi there reader!
  yo 7
</p>
```

## 참고문헌

- [SSP 참조](https://scalate.github.io/scalate/documentation/ssp-reference.html)

