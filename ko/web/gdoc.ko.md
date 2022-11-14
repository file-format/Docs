{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC 파일 - Google 문서도구 바로가기",
  "description":"GDOC 파일이 무엇이며 GDOC 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## .GDOC 파일이란?

GDOC 파일은 클라우드 기반 문서 저장 서비스인 Google 드라이브에 있는 파일을 가리키는 바로 가기 파일입니다. Google 드라이브 클라이언트가 컴퓨터에 설치되고 그 안에 문서가 생성되면 드라이브는 온라인 클라우드 저장소에 문서를 생성하고 로컬 Google의 GDOC 파일에 이 문서의 [URL](/ko/web/url/)을 씁니다. 드라이브 폴더. 이 바로 가기 파일을 더블 클릭하면 기본 웹 브라우저가 [URL](/ko/web/url/) 위치의 문서를 엽니다. 이 바로 가기 파일을 이 폴더 밖으로 옮기면 온라인 문서에 대한 링크가 끊어집니다.

## GDOC 파일 형식 - 추가 정보

GDOC 파일에는 [JSON](/ko/web/json/) 파일 형식으로 작성된 온라인 문서에 대한 바로 가기가 포함되어 있습니다. GDOC 파일을 여는 브라우저는 URL 정보를 읽고 사용자가 문서가 저장된 이 Google 계정에 로그인한 경우 링크된 문서를 열어 표시합니다. GDOC 파일에는 문서의 내용이 포함되어 있지 않습니다.

### GDOC 파일 예

GDOC 파일은 텍스트 편집기에서 열 수 있으며 그 내용은 다음과 같습니다.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

보시다시피, 내용은 문서의 URL과 관련 문서 ID가 있는 JSON 형식입니다.

## 참고문헌

* [Google 문서도구가 gdoc 또는 docx 파일을 열지 않음](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=ko )

