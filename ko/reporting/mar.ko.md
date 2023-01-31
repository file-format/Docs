{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Microsoft Access 보고서 파일",
  "keywords" :[ "mar", "mar 파일", "mar 파일 형식", "액세스 보고서란", "액세스 보고서", "Microsoft 액세스 보고서"],
  "description":"Microsoft Access 소프트웨어에서 Microsoft Access 보고서에 대한 바로 가기 또는 링크를 만드는 데 사용하는 MAR(Acess 보고서) 파일 형식에 대해 알아보세요.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## 액세스 보고서(MAR 파일)란 무엇입니까? ##
Microsoft Access에서 보고서 바로 가기로 만든 파일은 .mar 파일 확장명으로 저장됩니다. **Microsoft Access 보고서**는 Microsoft Access 데이터베이스의 정보를 포맷하고, 보고, 요약하는 방법을 제공합니다. 이 보고서를 사용하면 화면에서 보거나 인쇄할 수 있도록 정확하고 유익한 레이아웃으로 데이터 형식을 지정할 수 있습니다. 보고서는 고정 데이터만 표시하므로 Access 보고서를 볼 때 테이블의 데이터를 변경할 수 없습니다. 보고서를 열 때 가장 최근 데이터가 표시됩니다.

## MAR(Microsoft Access 보고서) 파일 형식

MAR 파일 형식은 Microsoft Access 소프트웨어에서 다음 용도로 데이터베이스에 정보를 표시해야 할 때 유용하게 되는 데이터베이스 개체인 Microsoft Access 보고서에 대한 바로 가기 또는 링크를 만드는 데 사용됩니다.

- 데이터 요약을 표시합니다.
- 데이터의 아카이브 스냅샷.
- 개별 기록에 대한 세부 정보를 표시합니다.
- 레이블을 만듭니다.

## 액세스 보고서의 일부
Access 보고서의 디자인은 디자인 보기에서 볼 수 있는 여러 섹션으로 나뉩니다. 다음 표는 각 섹션의 작동 방식과 보고서 작성에 도움이 될 수 있는 방법을 설명합니다.
| 섹션 | 인쇄 시 섹션이 표시되는 방식 | 섹션을 사용할 수 있는 위치 |
---------|----|------|
| 보고서 헤더 | 보고서 시작 부분. | 로고, 제목 또는 날짜와 같이 일반적으로 표지에 나타날 수 있는 정보에 대해 보고서 머리글을 사용합니다. 보고서 머리글에 합계 집계 함수를 사용하는 계산된 컨트롤을 배치하면 전체 보고서에 대한 합계가 계산됩니다. 보고서 머리글은 페이지 머리글보다 먼저 인쇄됩니다. |
| 페이지 머리글 | 모든 페이지의 상단에 있습니다. | 페이지 머리글을 사용하여 모든 페이지에서 보고서 제목을 반복합니다. |
| 그룹 헤더 | 각 새 레코드 그룹의 시작 부분. | 그룹 머리글을 사용하여 그룹 이름을 인쇄합니다. 예를 들어, 제품별로 그룹화된 보고서에서 그룹 머리글을 사용하여 제품 이름을 인쇄합니다. 그룹 헤더에 합계 집계 함수를 사용하는 계산된 컨트롤을 배치하면 합계는 현재 그룹에 대한 것입니다. 추가한 그룹화 수준 수에 따라 보고서에 여러 그룹 머리글 섹션이 있을 수 있습니다. 그룹 머리글 및 바닥글 만들기에 대한 자세한 내용은 그룹화, 정렬 또는 합계 추가 섹션을 참조하세요. |
| 상세 | 레코드 소스의 모든 행에 대해 한 번씩 나타납니다. | 여기에서 보고서의 본문을 구성하는 컨트롤을 배치합니다. |
| 그룹 바닥글 | 각 레코드 그룹의 끝. | 그룹 바닥글을 사용하여 그룹에 대한 요약 정보를 인쇄합니다. 추가한 그룹화 수준 수에 따라 보고서에 여러 그룹 바닥글 섹션이 있을 수 있습니다. |
| 페이지 바닥글 | 모든 페이지의 끝에서. | 페이지 바닥글을 사용하여 페이지 번호 또는 페이지당 정보를 인쇄합니다. |
| 보고서 바닥글 | 보고서 끝. 참고: 디자인 보기에서 보고서 바닥글은 페이지 바닥글 아래에 나타납니다. 그러나 다른 모든 보기(예: 레이아웃 보기 또는 보고서를 인쇄하거나 미리 볼 때)에서 보고서 바닥글은 페이지 바닥글 위, 마지막 페이지의 마지막 그룹 바닥글 또는 세부 정보 줄 바로 뒤에 나타납니다. | 보고서 바닥글을 사용하여 전체 보고서에 대한 보고서 합계 또는 기타 요약 정보를 인쇄합니다. |






## 참조 ##

- [Access 보고서 소개](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Access에서 보고서 디자인하기](https://www.uis.edu/informationtechnologyservices/wp-content/uploads/sites/106/2013/04/DesigningReportsinAccess2010.pdf)
