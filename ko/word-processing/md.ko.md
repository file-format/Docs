{
  "date" : "2019-10-11",
  "keywords" :[ "md 파일", "md 파일 형식", "md 파일이란", "파일", "md 예제", "md 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - MarkDown 언어 파일",
  "description":"MD 파일을 만들고 열 수 있는 MD 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## .MD 파일이란?

Markdown 언어로 생성된 텍스트 파일은 **.md** 또는 **.MARKDOWN** 파일 확장자로 저장됩니다. MD 파일은 인라인 텍스트 기호도 포함하는 Markdown 언어를 사용하는 일반 텍스트 형식으로 저장되며 들여쓰기, 표 형식, 글꼴 및 머리글과 같은 텍스트 형식을 정의하는 방법을 정의합니다. MD 파일은 Markdown이라는 프로그램을 사용하여 HTML로 변환할 수 있습니다. Markdown 언어는 John Gruber가 발표했습니다.

MD 파일은 또한 Markdown에서 주로 사용하는 개발자 파일로 분류할 수 있으며, 사용자가 읽고 쓰기 쉬운 파일을 만들 수 있도록 텍스트 파일을 HTML 버전으로 변환합니다. 다음은 .md 파일을 열 수 있는 응용 프로그램입니다.

* 마이크로소프트 메모장
* 메모장2
* 애플 텍스트에디트
* 마이크로소프트 워드패드

주의할 점은 .md 파일 확장자의 이름을 바꾸지 말라는 것입니다. 그렇다면 파일을 한 유형에서 다른 유형으로 변경하는 데 사용할 수 있는 특수 변환 소프트웨어가 있기 때문에 파일 유형이 변경되지 않습니다. 위에서 논의한 바와 같이 .MD 파일은 Markdown 언어 소프트웨어에서 생성된 파일의 확장자입니다. **Markdown**은 [경량 마크업 언어](https://en.wikipedia.org/wiki/Lightweight_markup_language)로 웹에서 일반 텍스트 서식 구문으로 텍스트 서식을 지정하는 데 사용됩니다. Markdown은 구문이 매우 작고 HTML 태그의 아주 작은 하위 집합을 포함하기 때문에 HTML을 대체하지 않는다는 점을 분명히 하십시오. Markdown을 사용하는 이유는 산문을 쉽게 읽고, 쓰고, 편집할 수 있도록 하기 위함입니다. 즉, HTML은 출판 형식이고 Markdown은 쓰기 형식이라고 말할 수 있습니다.

Markdown은 이제 세계에서 가장 인기 있는 마크업 언어 중 하나입니다. Microsoft Word를 사용하는 동안 버튼을 클릭하여 단어와 구의 서식을 지정하고 변경 사항을 즉시 볼 수 있습니다. 하지만 마크다운은 그렇지 않습니다. Markdown 형식의 파일이 생성되면 Markdown 구문이 텍스트에 추가되어 다르게 보일 수 있는 단어와 구문을 나타냅니다. 예를 들어, 제목을 표시하기 위해 그 앞에 숫자 기호가 추가됩니다(예: # 제목 1). 굵은 문장을 만들기 위해 앞뒤에 두 개의 별표를 추가합니다(예: **이 텍스트는 볼드체입니다**). 마크다운 구문은 텍스트에서 while 이후에 볼 수 있습니다.

## 약력

John Gruber와 Aaron Swartz는 2004년에 "읽기 쉬운 일반 텍스트 형식을 사용하여 작성하고 이를 XHTML 또는 HTML로 변환할 수 있는 옵션으로 작성할 수 있도록 하는" 아이디어로 Markdown 언어를 만들었습니다. 디자인의 목표는 가독성입니다. 언어는 태그와 형식 지정 지침이 분명한 RTF 또는 HTML과 같은 마크업 언어에서 수행되는 것처럼 형식 지정 지침이 추가되거나 태그가 지정된 것처럼 보이지 않고 있는 그대로 읽을 수 있습니다. 기본적인 영감은 이메일에서 일반 텍스트를 마크업하기 위해 기존 규칙을 사용하는 것입니다.

그 이후로 Markdown은 [CPAN](https://en.wikipedia.org/wiki/CPAN) 에서 사용할 수 있는 Perl [모듈](https://en.wikipedia.org/wiki/Modular_programming)과 같이 다른 사람들에 의해 다시 구현되었습니다. 및 다양한 기타 프로그래밍 언어로 제공됩니다. [BSD 스타일 라이선스](https://en.wikipedia.org/wiki/BSD_license)에 따라 배포되며 여러 [콘텐츠 관리 시스템](https://en.wikipedia.org/wiki/Content_management_system).

## 기술 사양

Markdown으로 무언가를 작성할 때 텍스트는 먼저 확장자가 .md 또는 .markdown인 일반 텍스트 파일에 저장되고 Dillinger와 같은 마크다운 응용 프로그램은 Markdown 형식의 텍스트를 웹에 표시하기 위해 HTML로 변환하는 Markdown 파일 처리에 사용됩니다. 브라우저. Markdown 응용 프로그램은 //Markdown 프로세서//(일반적으로 "파서" 또는 "구현"이라고도 함)를 사용하여 Markdown 형식의 텍스트를 가져와 HTML 형식으로 출력합니다. 프로세스의 흐름도는 아래와 같습니다.

간단히 말해서 다음과 같은 4단계 프로세스입니다.

1. 먼저 텍스트 편집기 또는 확장자가 .md 또는 .markdown인 Markdown 응용 프로그램을 사용하여 Markdown 파일을 만듭니다.
1. Markdown 파일이 Markdown 응용 프로그램에서 열립니다.
1. Markdown 응용 프로그램은 Markdown 파일을 HTML 문서로 변환하는 데 사용됩니다.
1. HTML 파일을 웹 브라우저에서 보거나 Markdown 응용 프로그램을 사용하여 PDF와 같은 다른 파일 형식으로 변환합니다.

Markdown은 빠르고 쉽게 메모를 작성하고, 웹사이트에 콘텐츠를 작성하고, 인쇄 준비 문서를 생성하고, 책을 출판하고, 프레젠테이션을 생성하고, 문서를 작성합니다.

마크다운의 일부 버전은 다른 버전에 상당한 영향을 미치므로 다른 버전의 일부로 인용되는 경우가 많습니다. 예를 들어 라이브러리는 CommonMark(GFM)에 대한 지원을 언급합니다. 간단히 살펴보겠습니다.

### GFM
Markdown은 오픈 소스 공유 플랫폼인 Github이 GFM(Github Flavored Markup)이라는 버전으로 언어를 허용하고 확장했기 때문에 개발자들에게 매우 인기가 있습니다.

### 커먼마크
Markdown 개발자들은 최근에 Markdown을 표준화하려고 시도했으며, 더 강력하고 CommonMark라고 하는 언어에 대한 버전, 테스트 및 문서를 만들기 위해 함께 했습니다. 이 형식은 약간 새롭고 많은 기능을 지원하지 않지만 곧 많은 MultiMarkdown 기능이 추가될 것입니다.

### 다중 마크다운
Multi-Markdown은 다른 버전에서 지원하는 다양한 기능을 언어에 추가했습니다. 원래 Perl로 작성되었지만 나중에 C로 옮겨졌습니다. 분리된 코드 블록, 구문 강조 표시, 테이블, 메타데이터, 조각/상호 참조 링크, 각주, 취소선, 정의 목록, 수학을 지원합니다.

## 참고문헌

* [마크다운 마스터하기](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

