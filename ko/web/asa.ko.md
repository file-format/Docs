{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "파일 형식", "파일 형식", ".asa 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - ASP 구성 파일",
  "description" :"ASA 파일이 무엇이며 ASA 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## .ASA 파일이란?

ASA 파일은 [ASP](/ko/web/asp/)/ASP.NET 프로젝트용으로 생성된 구성 파일입니다. 여기에는 응용 프로그램의 전역 수준에서 액세스할 수 있는 변수, 포함 및 기능의 선언이 포함됩니다. 프로젝트의 모든 페이지는 이러한 변수와 함수에 액세스할 수 있으므로 다시 작성할 필요가 없습니다. 이러한 예 중 하나는 다른 ASP 웹 사이트 페이지에서 액세스할 수 있도록 루트 디렉터리에 저장된 Global.asa 페이지입니다. Global.asa 파일은 선택 사항이지만 사용하는 경우 각 응용 프로그램에는 Global.asa 파일이 하나만 있을 수 있습니다.

## ASA 파일 형식 - 추가 정보

ASA 파일은 다음 정보가 포함된 일반 텍스트 파일입니다.

* 응모 이벤트
* 세션 이벤트
* \<object> 선언
* TypeLibrary 선언
* #include 지시문

## ASA 파일 예

Global.asa 파일은 다음과 같습니다.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## 참고문헌

* [ASP Global.asa 파일 - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

