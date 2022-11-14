{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPCACHE 파일 - HTML5 캐시 매니페스트 파일 형식",
  "description" :"APPCACHE 파일이 무엇이며 APPCACHE 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## .APPCACHE 파일이란?

APPCACHE 파일은 웹 응용 프로그램에 오프라인으로 액세스하기 위해 브라우저에서 캐시할 리소스 목록이 포함된 텍스트 파일입니다. 인터넷에 연결되어 있지 않을 때 유용합니다. 이러한 상황에서 브라우저는 오프라인 캐시 리소스를 사용하여 웹 콘텐츠에 대한 액세스를 제공합니다. APPCACHE 파일에는 이미지(예: **[PNG](/ko/image/png/)**, **[WEBP](/ko/image/webp/)** 등), 스타일시트 **([ CSS])(/ko/web/css/)** 및 스크립트 파일(예: Javascript **[JS](/ko/web/js/)** 파일).

**APPCACHE 파일을 열 수 있는** 애플리케이션에는 Google Chrome, Safari 및 Firefox와 같은 웹 브라우저가 있습니다.

## APPCACHE 파일 형식 - 추가 정보

APPCACHE 파일은 인터넷 연결 없이 실행할 수 있는 웹 페이지에 대한 오프라인 액세스를 제공하는 간단한 텍스트 파일입니다. APPCACHE의 존재는 페이지를 오프라인에서 사용 가능한 것으로 지정합니다.

### APPCACHE 파일을 참조하는 방법은 무엇입니까?

HTML 페이지에서 APPCACHE 파일은 다음과 같이 참조됩니다.

```
<html manifest="example.appcache">
  ...
</html>
```

## APPCACHE 매니페스트 파일의 구조

간단한 APPCACHE 매니페스트 파일은 다음과 같습니다.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

이것은 가장 간단한 예이며 더 복잡한 구조도 존재할 수 있습니다.

## APPCACHE 매니페스트의 장점

캐시 인터페이스를 사용하면 웹 애플리케이션에 다음과 같은 이점이 있습니다.

1. 오프라인 브라우징 - 캐시 인터페이스는 최종 사용자가 오프라인일 때 전체 사이트를 탐색할 수 있도록 합니다.
1. 속도 - 캐시를 통해 디스크에서 직접 오프라인 콘텐츠에 고속으로 액세스할 수 있습니다.
1. 항상 액세스 가능 - 사이트가 다운되더라도 사용자는 웹 콘텐츠에 계속 액세스할 수 있으며 오프라인 경험을 얻을 수 있습니다.

## 참고문헌

* [AppCache 매니페스트 초보자 가이드](https://web.dev/appcache-beginner/)

