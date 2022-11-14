{
  "date" : "2021-05-20",
  "keywords" :[ "shtml","shtml 파일", "shtml 파일 형식", "shtml 파일 형식", "파일", "유형", "shtml 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - 서버 측 HTML 파일 포함",
  "description":"SHTML 파일 형식과 SHTML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## .SHTML 파일이란?

확장자가 .shtml인 파일은 [HTML](/ko/web/html/)로 작성된 웹 페이지이며 서버 지침이 포함되어 있습니다. 또한 더 빠른 로딩을 위해 ASP 파일과 유사한 서버 측 포함을 포함할 수 있습니다. 서버 측 파일에는 서버를 평소보다 느리게 로드할 수 있는 실행 코드가 포함될 수도 있습니다. SHTML 파일은 HTML과 유사하지만 간단한 서버 명령도 사용할 수 있습니다. 이러한 서버 명령은 SSI(Server Side Include)라는 간단한 컴퓨터 프로그래밍 언어로 수행됩니다. SHTML은 [PHP](/ko/programming/php/) 포함과 같은 다른 서버 측 프로그래밍 언어로 대체되었습니다.

## SHTML 파일 형식

SHTML 파일은 일반 텍스트로 작성되며 서버 측에서 실행되는 [SSI 명령](https://www.w3.org/Jigsaw/Doc/User/SSI.html)을 사용합니다. 이러한 서버 측 명령을 사용하여 데이터베이스 드라이버를 사용하여 데이터베이스에 연결하고 테이블에서 사용자 데이터를 가져올 수도 있습니다.

## SHTML 예제

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

