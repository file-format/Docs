{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAML 파일 형식 - Haml 소스 코드 파일",
  "description":"HAML 파일을 생성하고 열 수 있는 HAML 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## HAML 파일이란?

HAML 파일은 [Haml](https://haml.info/) 언어로 작성된 소스 코드를 포함하는 HTML 추상화 마크업 언어 파일입니다. ERB(Ruby 템플릿 스크립트)의 대체품으로 사용할 수 있습니다. HAML 파일에는 웹 문서의 HTML을 생성하기 위한 템플릿 소스 코드가 포함되어 있습니다. ERB 파일은 파일 확장자를 변경하여 app/views 폴더에 있는 이러한 파일을 Haml로 교체하기만 하면 교체할 수 있습니다. HAML 파일은 Microsoft 메모장, 메모장++, Apple TextEdit,

## HAML 파일 형식

HAML 파일은 디스크에 일반 텍스트 파일로 저장된 소스 파일입니다. 여기에는 HAML 구문으로 작성된 코드가 포함되어 있습니다. HAML은 **<>** 태그를 **%** 기호로 대체하여 코드를 더 간단하고 쉽게 만듭니다. ERB 파일은 다음의 간단한 예와 같이 HAML로 교체할 수 있습니다.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### HAML 예

다음은 HAML의 Hello World 예제입니다.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
다음 HTML 출력으로 렌더링됩니다.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## 참고문헌

* [HAML - Github](https://github.com/haml/haml)

