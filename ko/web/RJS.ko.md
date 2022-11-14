{
  "date" : "2021-05-24",
  "keywords" :["rjs", "파일", "확장자", "파일 형식", "파일 확장자", "RJS", "루비 자바스크립트 파일"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - 루비 자바스크립트 파일",
  "description":"RJS 파일 형식과 RJS 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## RJS 파일이란?

확장자가 .rjs인 파일은 Rails 개발자가 Ruby를 사용하여 동적 JavaScript 코드를 생성할 수 있도록 하는 Ruby 코드와 JavsScript의 조합입니다. Ruby 코드는 Java 기능에 포함되며 Ruby 엔진이 서버에서 실행되어야 하는 웹 서버에서 컴파일됩니다. RJS는 [RHTML](/ko/web/rhtml/)과 유사합니다. 유일한 차이점은 측면에는 [HTML](/ko/web/html/)에 Ruby 코드가 포함되어 있고 Javascript 기능에는 Ruby 코드가 포함되어 있다는 것입니다.

## RJS 파일 형식

RJS 파일은 다른 스크립팅 또는 프로그래밍 언어와 마찬가지로 일반 텍스트로 코딩됩니다. 클라이언트에서 이러한 페이지를 요청하면 서버에서 Ruby 코드가 실행되고 클라이언트의 브라우저에는 HTML과 Javascript 코드만 반환됩니다. RJS 파일의 구문은 Ruby와 JavaScript 구문의 조합과 유사하여 Ruby 코드만 JavaScript 기능에 포함됩니다.

### RJS 예

다음 예제는 간단한 Ruby 코드를 독립적으로 보여주고 JavaScript 함수에 포함됩니다.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
다음은 RubyJS입니다.
```Ruby
# here you go!

foo = -> { "bar" }
```
## 참고문헌

* [RJS](https://github.com/makevoid/rjs)

