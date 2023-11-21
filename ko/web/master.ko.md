{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MASTER 파일 - ASP.NET 마스터 페이지 파일 형식",
  "description" :"MASTER 파일 형식과 MASTER 파일을 만들고 여는 API에 대해 알아보세요.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## MASTER 파일이란 무엇입니까?

MASTER 파일은 ASP.NET으로 만든 마스터 웹 페이지 템플릿 파일입니다. MASTER 파일과 동일한 레이아웃 및 설정을 가진 여러 페이지를 생성하기 위한 시작점으로 사용됩니다. 템플릿 MASTER 파일에는 머리글, 탐색 메뉴, 바닥글, 글꼴 및 스타일 정보에 대한 설정이 포함되어 있습니다. MASTER 파일을 사용하면 여러 웹페이지를 빠르게 만들 수 있습니다.

Microsoft Visual Studio 2022 이상을 사용하여 MASTER 파일을 열 수 있습니다.

## MASTER 파일 형식 - 추가 정보

MASTER 파일은 HTML 파일 형식으로 생성 및 저장되며 다른 웹페이지 파일과 유사합니다. 편집 가능한 섹션과 편집 불가능한 섹션으로 나누어져 있습니다. 편집 가능한 섹션은 사용자의 요구 사항에 맞게 수정할 수 있는 섹션입니다. Microsoft Visual Studio에서 MASTER 파일을 열면 편집할 수 없는 섹션이 회색으로 표시됩니다.

마스터 페이지는 마스터 페이지 자체와 하나 이상의 콘텐츠 페이지 등 두 부분으로 구성됩니다.

### 마스터 페이지

마스터 페이지는 .master 확장자를 가지며 ASP.NET으로 만들어집니다. 정적 텍스트, HTML 태그 및 서버 측 컨트롤로 구성된 미리 정의된 레이아웃이 있습니다. 일반 .aspx 페이지에서는 @ Page 지시문이 사용됩니다. .master 파일의 경우 @Master 지시문으로 대체됩니다.

### 콘텐츠 페이지

콘텐츠 페이지는 마스터 페이지의 자리 표시자 컨트롤에 대한 콘텐츠를 나타냅니다. 이는 실제로 마스터 페이지의 코드 숨김인 .aspx 페이지입니다. 콘텐츠 페이지는 아래와 같이 사용할 마스터 페이지를 가리키는 MasterPageFile 특성을 포함하여 @ Page 지시문을 사용하여 바인딩됩니다.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## 참고자료

* [ASP.NET 마스터 페이지 개요](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

