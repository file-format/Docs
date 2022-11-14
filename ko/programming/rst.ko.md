{
  "date" : "2022-04-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RST 파일 형식 - 재구성된 텍스트 파일",
  "description":"RST 파일 형식과 RST 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "RST",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-11"
}

## .RST 파일이란?

RST 파일은 주로 Python 프로그래밍 커뮤니티에서 사용되는 기술 문서 파일 형식입니다. 문서 생성을 위해 일반 텍스트 문서에 스타일과 서식을 적용하는 reStructuredText 마크업 언어로 작성된 텍스트 파일입니다. RST 파일은 Python 프로그램 코드의 주석 및 기타 정보를 사용하여 응용 프로그램의 기술 문서를 만듭니다. 그러나 여기에는 간단한 웹페이지와 [eBook](/ko/ebook/)으로 변환할 수 있는 텍스트도 포함될 수 있습니다. Github Atom, GNU Emacs(교차 플랫폼), Microsoft 메모장(Windows), Apple TextEdit(Mac) 및 Vim(Linux)과 같은 텍스트 편집기를 사용하여 RST 파일을 열 수 있습니다.

## RST 파일 형식

RST 파일에는 reStructuredText 마크업 언어로 작성된 코드가 포함되어 있습니다. Java용 Javadoc과 유사한 Python용 도구 세트를 제공하는 Python Doc-SIG(Documentation Special Interest Group)의 Docutils 프로젝트의 일부입니다. RST 파일 형식용 파서는 Docutils에 포함되어 있으며 프로그램 문서로 형식을 지정하기 위해 Python 프로그램에서 정보를 추출할 수 있습니다.

### reStructuredText RST 예제

다음과 같이 RST 파일 형식으로 작성된 텍스트를 예로 들어보겠습니다.

```
================
Document Heading
================

Heading
=======

Sub-heading
-----------

Paragraphs are separated
by a blank line.
```

이 텍스트를 Docutils와 같은 rST 프로세서에 입력하면 다음과 같이 출력됩니다.

```
<h1>Document Heading</h1>

<h2>Heading</h2>

<h3>Sub-heading</h3>

<p>Paragraphs are separated
by a blank line.</p>
```

## 참조 ##

* [reStructuredText - 위키피디아 작성](https://en.wikipedia.org/wiki/ReStructuredText)

