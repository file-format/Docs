{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTX 파일 - HTML 확장 파일 형식",
  "description" :"HTX 파일을 만들고 열 수 있는 API와 HTX 파일이 무엇인지 알아보기 위한 파일 형식 가이드",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .HTX 파일이란?

HTX 파일은 실제로 데이터베이스 쿼리 결과를 웹 페이지로 표시하기 위한 데이터 변수를 포함하는 HTML 파일입니다. 대부분 Microsoft FrontPage 웹 개발 소프트웨어로 생성되는 HTX 파일은 해당 인터넷 데이터베이스 커넥터(.IDC) 파일과 동일한 폴더에 저장되도록 저장됩니다.

HTX 파일은 Microsoft FrontPage와 같은 응용 프로그램과 메모장, TextEdit 또는 Atom과 같은 텍스트 편집기로 열 수 있습니다.

## HTX 파일 형식

HTX 파일은 데이터베이스에서 데이터를 검색하고 표시를 위해 변수에 저장하기 위한 코드와 함께 일반 텍스트 파일로 저장됩니다.


### HTX 파일 예

HTX 파일의 예는 쿼리 제한을 표시하기 위한 페이지 헤더와 사용자에게 표시하기 위해 페이지에 표시되는 문서를 정의하는 다음과 같습니다.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

이 샘플 코드의 출력은 다음과 같습니다.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

보시다시피 HTX 파일은 결과가 최종 사용자에게 반환되고 표시되는 방식을 형식화하는 템플릿입니다. 일부 IIS 확장 및 인덱싱 서비스를 사용하여 HTML 형식으로 작성되었습니다. 이러한 확장에는 결과 처리를 위한 변수 이름 및 기타 코드가 포함됩니다.

## 참고문헌

* [.Htx 파일에서 결과 서식 지정](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

