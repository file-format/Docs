{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "파일", "확장자", "파일 형식", "Mathematica", "스프레드시트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"NB 파일을 만들고 열 수 있는 NB 파일 API가 무엇인지 알아보세요.",
  "title" :"NB - Mathematica 노트북 파일 형식",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## .NB 파일이란?

확장자가 .nb인 파일은 수학적 지침에 대한 지침을 텍스트 파일로 저장하는 Wolfram 노트북 파일 형식입니다. 여기에는 라이브 계산, 임의의 동적 인터페이스, 전체 조판 입력, 이미지 입력, 자동 코드 주석, 완전한 고급 프로그래밍 인터페이스, 신중하게 구성된 수천 개의 기능 및 옵션과 같은 다양한 유형의 데이터가 포함될 수 있습니다. 텍스트 지침은 입력 문이 파일에 놓일 때 생성되고 업데이트되는 Mathematica 입력 및 출력입니다.

## Wolfram 노트북 NB 파일 형식 - 추가 정보

Wolfram Notebook NB 파일은 사람이 읽을 수 있는 파일 형식인 일반 텍스트 형식으로 저장됩니다. 전자 필기장의 내용은 스프레드시트와 유사하게 각 섹션이 셀 그룹으로 표시되는 일반 텍스트로 섹션으로 정렬됩니다. 이러한 그룹의 범위는 각 셀의 끝에 있는 대괄호로 정의됩니다. 셀에 할당된 스타일은 아래에 자세히 설명된 대로 노트북 내에서의 역할을 결정합니다.

### Wolfram 언어로서의 노트북

Wolfram Language Kernal에서 실행하기 위한 수학적 명령으로 구성된 노트북을 저장하려는 경우 문서의 셀에 자동으로 '입력' 텍스트 스타일이 할당됩니다. 이것은 커널이 이것을 사용자가 'Shift+Return' 키 조합을 발행할 때 실행되는 명령으로 간주하도록 지시합니다. Mathematica Notebook은 다음 예와 같습니다.

{{< figure src="../Wolfram Notebook.jpeg" alt="Wolfram 노트북 파일 형식" >}}

### 문서로서의 노트북

Mathematica Notebooks는 문서 형식으로 되어 있어 보고 있는 것이 무엇인지(WYSIWYG) 확인할 수 있습니다. 이러한 문서는 화면이나 인쇄된 종이에서 보는 것과 동일하며 대화형입니다. 이를 위해 'Text Style'을 셀에 할당하여 Kernel에서 문장을 실행하지 않고 내용을 표시합니다.

## Mathematica 노트북 내보내기

Mathematica Notebook은 PDF, 그래픽, GIS, 압축 및 스프레드시트와 같은 다양한 파일 형식으로 내보낼 수 있습니다.

## 참고문헌

* [Mathematica Notebook 기초](https://reference.wolfram.com/language/guide/NotebookBasics.html)

