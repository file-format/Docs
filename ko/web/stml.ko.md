{
  "date" : "2021-05-20",
  "keywords" :[ "stml","stml 파일", "stml 파일 형식", "stml 파일 형식", "파일", "유형", "stml 파일이란"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - SSI HTML 파일",
  "description":"STML 파일 형식과 STML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## .STML 파일이란?

확장자가 .stml인 파일은 사용자가 웹 브라우저에서 페이지를 로드할 때 실행되는 서버 측 지침이 있는 웹 페이지입니다. STML 페이지에는 일반 HTML로 달성할 수 없는 작업을 수행하기 위한 서버 측 포함이 포함된 서버 측 코드가 포함되어 있습니다. [HTML](/ko/web/html/)과 유사하지만 STML은 SSI(Server Side Include)라고도 하는 서버에서 명령을 실행하여 더 많은 기능을 제공합니다. PHP와 같은 서버 측 스크립팅과 함께 새로운 프로그래밍 언어가 도입되면서 모든 서버 측 기술에서 여전히 지원되지만 STML의 사용이 감소합니다. STML 파일은 모든 텍스트 편집기에서 열 수 있으며 명령 업데이트를 위해 편집할 수 있습니다.

## STML 파일 형식

STML은 사람이 읽을 수 있는 일반 ASCII 텍스트 파일 형식을 기반으로 합니다. 그러나 서버 측에서 실행되는 [SSI 명령](https://www.w3.org/Jigsaw/Doc/User/SSI.html)을 사용하여 정의되고 실행된 구문을 따릅니다. 다른 서버 측 스크립팅 언어와 마찬가지로 STML은 서버 측 명령을 사용하여 페이지 방문자 카운터, 웹 페이지 달력, 데이터베이스에서 레코드 검색 등과 같은 작업을 수행할 수 있습니다.

## STML 예

서버 측 지침은 페이지 방문자 카운터 또는 웹 페이지 캘린더와 같은 애플리케이션에서 사용됩니다. 다음 예에서는 사용자 데이터베이스의 처음 세 줄의 처음 네 열을 표시합니다.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## 참고문헌

* [서버 측 포함](https://en.wikipedia.org/wiki/Server_Side_Includes)

