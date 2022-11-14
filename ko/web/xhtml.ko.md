{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "파일", "확장자", "파일 형식", "파일 확장자", "확장 가능한 html"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - 확장 가능한 하이퍼텍스트 마크업 언어 파일 형식",
  "description":"XHTML 파일 형식과 XHTML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## XHTML 파일이란?

XHTML은 HTML 4.0의 재구성을 사용하여 XML에 마크업이 있는 텍스트 기반 파일 형식입니다. 이러한 파일은 웹 브라우저에서 열거나 보는 데 적합합니다. XHTML은 보다 구조화되고 덜 스크립팅되며 일반적으로 설계되었습니다. XML의 모든 기존 기능을 사용하고 더 많은 장치에 독립적입니다. XHTML은 스타일 시트와 결합된 확장 옵션과 함께 일반적으로 가치 있는 요소 및 속성 세트를 제공합니다. 속성은 메타데이터 속성 컬렉션에서 사용됩니다. XHTML은 모든 **[HTML](/ko/web/html/)** 프레젠테이션 요소를 스타일 시트에 종속시킴으로써 유연성과 접근성을 제공합니다. 스타일 시트는 이러한 프리젠테이션 요소보다 더 다양합니다. HTML 4.01, HTML5 및 XHTML에 대한 사양은 W3C(World Wide Web Consortium)에서 동적으로 개발되고 있습니다.

## XHTML 파일 형식의 간략한 역사

XHTML의 역사는 World Wide Web Consortium에서 1998년 12월에 발표한 초안 문서로 시작됩니다. 이 문서는 XHTML 1.0이라는 사양인 "Reformulating HTML in XML"을 참조합니다. 이 새로운 사양은 기존 요소 또는 속성을 사용하여 XML로 HTML을 다시 작성합니다. 1999년 5월 W3 컨소시엄은 HTML 4.0이 XML 응용 프로그램으로 재편성되었다고 선언했습니다. 즉, XHTML. 2000년 1월 26일, XHTML 1.0을 정의하는 첫 번째 사양이 W3C에 의해 발표되었습니다. 더 나아가 2001년 5월 31일 W3C는 XHTML을 독립 언어로 발표하고 HTML 5.0 개발 작업을 시작했습니다. 그러나 2005년에 XHTML과 독립적인 일반 HTML을 개선하기 위한 작업 그룹(WHATWG)이 구성되었습니다. WHATWG는 결국 XHTML 2와 병행하여 HTML5 작업을 시작했습니다.

## XHTML 파일 형식

XHTML은 HTML 4를 모방, 분류 및 확장하는 다양한 문서 유형 및 모듈의 모음인 형식입니다. XHTML의 파일은 XML 기반이며 XML 기반의 사용자 에이전트와 작업하는 것을 목표로 합니다. XHTML 파일은 XML을 준수합니다. 표준 XML 도구는 XHTML 파일을 보고, 편집하고, 검증하는 데 사용됩니다. HTML 문서 개체 모델 또는 XML DOM(문서 개체 모델) 종속 응용 프로그램은 XHTML 문서를 통해 작동할 수 있습니다. 오늘날 XHTML을 선택하면 콘텐츠 개발자는 콘텐츠의 순방향 또는 역방향 호환성에 대해 걱정하지 않고 XML의 모든 관련 이점을 누릴 수 있습니다.

관련 요소 집합은 XHTML에서 모듈을 빌드합니다. 양식 또는 테이블 모듈에는 웹 페이지에 표시할 수 있는 다양한 양식 또는 테이블 요소가 포함될 수 있습니다. 모듈화는 HTML 요소를 수많은 연결된 요소 세트로 분리하는 것을 목표로 했습니다. 따라서 콘텐츠 개발자는 다양한 유형의 장치에 대한 모듈 선택을 활용할 수 있습니다. 또한 모듈을 통해 사용자 에이전트는 XHTML 표준과의 일관성을 잃지 않고 요소를 선택할 수 있습니다. XHTML의 구문 분석 요구 사항은 XML과 동일하지만 HTML은 자체적으로 실행합니다.

### 문서 적합성

XHTML2는 XML 및 XHTML 1.0의 네임스페이스 요소와 속성을 사용하는 XHTML 1.0 문서를 준수하는 사양을 제공합니다. 문서 적합성에는 두 가지 유형이 있습니다.

Strictly Conforming Document는 이 사양에 정의된 필수 서비스만 필요한 XML 기반입니다. XHTML 파일에 대해 다음 기준을 충족해야 합니다.

* 파일은 DTD 및 부록 B에 정의된 제약 조건을 준수해야 합니다.
* 파일의 기본 요소는 html이어야 합니다.
* 파일의 기본 요소는 XHTML 네임스페이스에 대한 선언을 포함해야 하며 다음과 같이 정의되어야 합니다.

```
http://www.w3.org/1999/xhtml.
```

* 기본 요소는 다음과 같이 작성할 수 있습니다.

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

기본 요소보다 먼저 DOCTYPE을 선언해야 하며, 공개 식별자는 세 가지 DTD(문서 유형 정의) 중 하나를 참조해야 합니다. 시스템 식별자는 현재 시스템 규칙을 준수하도록 수정될 수 있습니다.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

XML 문서에서는 모든 문서에 XML 선언을 지정할 필요가 없습니다. 그러나 콘텐츠 개발자는 모든 XHTML 문서에서 XML 선언을 사용하도록 유도됩니다. 이러한 선언은 문서의 문자 인코딩이 UTF-8/16과 다르거나 관리 프로토콜에서 인코딩이 지정되지 않은 경우 필수입니다. 다음 XHTML 문서의 예는 XML 선언을 정의합니다.

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

준수하는 사용자 에이전트는 다음 규칙을 충족해야 합니다.

* XHTML 문서의 구문 분석 및 평가는 XML 1.0 권장 사항과의 일관성을 보장하는 사용자 에이전트에 의해 수행됩니다.
* 사용자 에이전트를 검증하는 경우 XML에 따라 참조된 DTD에 대한 문서 유효성을 확인해야 합니다. XHTML 파일이 사용자 에이전트에 의해 일반 XML로 처리될 때 유형 ID의 기능은 조각 식별자로 인식됩니다.

사용자 에이전트가 인식할 수 없는 요소와 충돌하는 경우 달성해야 하는 필수 기준은 다음과 같습니다.

* 알 수 없는 요소의 내용 처리
* 속성과 그 값을 무시
* 기본값으로 제공되는 속성 값을 사용합니다.

사용자 에이전트가 엔티티 참조 선언이 이전에 처리되지 않은 것을 발견하면 문자로 처리되어야 합니다("&" 기호로 시작하여 세미콜론으로 끝남). 콘텐츠 처리 중에 사용자 에이전트가 예측할 수 있지만 렌더링할 수 없는 캐릭터 또는 캐릭터 엔터티 참조는 유사한 의미를 생성하는 대체 렌더링을 사용할 수 있습니다. 이 경우 문서는 렌더링 과정이 정상적이지 않았다는 사실을 사용자가 명확하게 알 수 있는 방식으로 표시되어야 합니다. 공백 처리를 위해 사용자 에이전트는 CSS 문자[CSS2]에서 정의를 찾아야 합니다.

## XHTML 이전 버전과의 호환성

XHTML 1. 문서의 하위 호환성은 적절한 규칙을 따른다면 HTML 4 사용자 에이전트에 정통합니다. XHTML 1.1은 일반적으로 HTML 4 브라우저에서 무시되지만 Ruby 주석을 제외하고는 완전히 호환됩니다. XHTML 2.0은 비교적 덜 호환되지만, 그럼에도 불구하고 문제는 스크립팅 사용을 통해 어느 정도 해결되었습니다.

## 참고문헌

* [XHTML의 역사: 1990년대부터 오늘날까지](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

