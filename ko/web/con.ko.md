{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CON 파일 - 개념 응용 소스 파일 형식",
  "description" :"CON 파일이 무엇이며 CON 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## .CON 파일이란?

CON 파일은 **Concept Application Server**용으로 개발된 애플리케이션의 소스 코드 파일입니다. 서버와 사용자 간의 데이터 교환을 위한 응용 프로그램을 작성하는 데 사용됩니다. 서버에서 호스팅되는 CON 파일은 사용자 측에서 Concept Client가 설치된 경우 웹 브라우저를 통해 액세스할 수 있습니다. 개념 응용 프로그램 서버는 [SQL](/ko/database/sql/) 하위 집합 데이터베이스 엔진(TinDB)을 가질 수 있는 소규모 프로그래밍 언어를 사용하는 웹 서버입니다.

CON 파일은 RadGs Concept Application Server로 열거나 실행할 수 있습니다.

## CON 파일 형식 - 추가 정보

CON 파일은 서버에서 호스팅되며 사용자 컴퓨터에서 웹 브라우저를 사용하여 액세스합니다. 개념 [URL](/ko/web/url/)은 일반 HTTP URL과 다르며 **concept://**로 시작합니다.

### CON 파일 URL 예

Concept Application Server에서 호스팅되는 CON 파일은 다음과 같은 URL을 사용하여 웹 브라우저를 통해 액세스할 수 있습니다.

```
concept://domain.server.com/web_application/main.con.
```
## 참고문헌

* [컨셉 애플리케이션 서버](https://github.com/Devronium/ConceptApplicationServer)

