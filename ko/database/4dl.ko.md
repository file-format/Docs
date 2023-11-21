{
  "date" : "2023-06-14",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"4DL 파일 형식과 4DL 파일을 생성하고 열 수 있는 API에 대해 알아보세요.",
  "title" :"4DL - 4차원 데이터베이스 로그 파일",
  "linktitle" : "4DL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-06-14"
}

## .4DL 파일이란?

4DL 로그 파일은 4D 데이터베이스(.4DD) 파일에 대한 수정 사항을 기록하는 데 사용됩니다. 이 파일은 데이터베이스 파일과 함께 저장되며 유사한 파일 이름을 공유합니다. 그 목적은 데이터베이스 내에 구현된 업데이트의 포괄적인 기록을 정확하게 추적하고 유지하는 것입니다. 4DL 파일에 비해 [4DD 파일](/ko/database/4dd/)은 주로 4D Inc.의 4차원과 관련되어 있습니다.

## 4DL 파일 형식 - 추가 정보

일반적으로 여러 4DL 파일은 4DD 파일과 함께 저장됩니다. 따라서 로그 파일의 첫 번째 버전은 0001.4dl로 이름이 지정될 수 있지만 로그 파일의 측면 버전은 0002.4dl, 0003.4dl 등으로 저장됩니다. 이제 로그 파일 자체가 3번 연속 저장되면 "db1[0005-0003].4dl"이라는 레이블이 붙습니다.

## 참고자료

* [4DD - Wikipedia](https://en.m.wikipedia.org/wiki/4th_Dimension_(software))
