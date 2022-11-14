{
  "date" : "2021-01-21",
  "keywords" :[ "ai 파일", "ai 파일 형식", "ai 파일이란", "파일", "ai 예제", "ai 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - 어도비 일러스트레이터 아트워크 파일",
  "description":"AI 파일을 생성하고 열 수 있는 AI 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## .AI 파일이란?

확장자가 .ai인 파일은 단일 페이지에 벡터 그래픽이 포함된 Adobe Illustrator 아트워크 파일입니다. 포인트를 사용하여 이미지 데이터를 표시하기 위한 경로를 생성하므로 확대해도 이미지 품질이 저하되는 것을 방지합니다. AI 파일 형식은 AI 파일과 유사한 PGF 파일 형식을 기반으로 합니다. AI 형식은 로고 및 인쇄 매체에 주로 사용되며 초기 버전은 [EPS](/ko/image/eps/) 파일과 유사한 것으로 간주되었습니다. AI 파일은 Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro 및 CorelDraw Graphics 도구로 열 수 있습니다.

## AI 파일 형식

AI는 Adobe Illustrator의 독점 파일 형식이며 EPS 호환 파일을 저장하기 위해 PGF와 유사한 이중 경로 접근 방식을 사용합니다. [Adobe Illustrator 파일 형식 사양](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)에서 자세한 이 파일 형식의 내부 세부 정보는 개발자 참조를 참조하세요. 모두 Adobe Illustrator에서 만든 문서(파일)는 PostScript 언어 문서이며 문서 구조화 규칙을 준수하는 '프롤로그'와 '스크립트'의 두 가지 주요 부분으로 구성됩니다.

### 프롤로그

프롤로그 섹션은 파일 해석에 필요한 정보를 캡슐화합니다. 페이지의 모든 마크를 포함하는 경계 상자가 한 예입니다. 여기에는 글꼴 및 절차 정의와 같은 리소스 정보도 포함됩니다. 이러한 리소스는 procsets라고 하는 집합으로 논리적으로 그룹화되며 해당 절차를 초기화하고 종료하기 위한 명시적 메서드를 포함합니다.

### 스크립트

페이지의 그래픽 요소는 스크립트로 설명됩니다. 스크립트에는 피연산자 및 데이터와 함께 프롤로그의 연산자 및 프로시저에 대한 참조가 포함됩니다. 스크립트의 세 가지 논리적 섹션에는 다음이 포함됩니다.

* 설정 순서 - 프롤로그에 정의된 리소스를 초기화하고 활성화합니다.
* 설명 연산자의 순서
* 자원을 비활성화하는 예고편

스크립트의 연산자는 프롤로그의 procsets에 의해 정의된 언어로 작성된 일련의 그래픽 요소입니다. 이러한 시퀀스는 데이터 요소 모음, 그래픽 속성 정의 및 프로시저에 정의된 프로시저 호출로 구성됩니다.

### 개체 태그

개체 태그는 Adobe Illustrator 아트 개체에 사용자 정의 정보를 첨부하는 데 사용됩니다. 태그는 다음으로 구성됩니다.

* 태그 식별자
* 태그 유형
* 데이터

## 참고문헌
* [Adobe Illustrator 파일 형식 사양](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [PaintShopPro의 AI 파일 형식](https://www.paintshoppro.com/en/pages/ai-file/)

