{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AVL - ArcView 범례 파일",
  "description":"AVL 파일을 만들고 열 수 있는 AVL 파일 형식 및 API에 대해 알아보십시오.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## .AVL 파일이란?

AVL 파일은 ESRI ArcView GIS(Geographic Information System) 소프트웨어로 생성된 지도의 키가 포함된 범례 파일입니다. 접근을 위해 해당 맵에서 사용되는 참조 심볼 정보를 담고 있습니다. AVL 파일에는 유형에 따라 심볼, 디스플레이 설정(예: 투명도), 배율 종속 디스플레이 속성, 조인된 테이블/관련 테이블 정보, 정의 쿼리, 피처 레이어의 레이블 지정 속성, 주석 레이어의 주석 디스플레이 속성과 같은 추가 정보가 포함될 수 있습니다. 일종의 레이어.

AVL 파일은 ArcView 프로젝트 [.APR](/ko/gis/apr/) 파일에서 참조할 수 있습니다.

## AVL 파일 형식 - 추가 정보

AVL 파일은 일반 텍스트 파일 형식으로 저장됩니다. 즉, 메모장, Notepad++ 및 Apple TextEdit와 같은 모든 텍스트 편집기에서 AVL 파일을 열 수 있습니다. 파일을 열면 파일 내용을 볼 수 있을 뿐만 아니라 수정할 수도 있습니다.

### .LYR 파일과 .AVL 파일의 차이점

* **파일 형식 차이** - .lyr는 바이너리 파일인 반면 .avl은 텍스트 파일입니다.
* **내용 차이** - .lyr 파일은 .avl 파일보다 더 많은 정보를 포함합니다. AVL 파일은 기호 정보만 저장하는 반면 LYR 파일은 ArcMap의 레이어 속성 대화 상자에서 사용할 수 있는 모든 정보를 저장합니다.

## 참조

* [.lyr 파일과 .avl 파일의 차이점](https://support.esri.com/en/technical-article/000005936)

