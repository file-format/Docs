{
  "date" : "2021-06-28",
  "keywords" :[ "cgi 파일", "cgi 파일이란", "파일", "cgi 예제", "cgi 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"CGI 파일을 만들고 열 수 있는 CGI 파일 형식과 API에 대해 알아보세요.",
  "title" :"CGI - 공통 게이트웨이 인터페이스 스크립트 파일",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## .CGI 파일이란?
CGI 파일은 웹 서버에서 사용자 요청을 처리하기 위해 외부 프로그램을 실행하는 데 사용하는 Common Gateway Interface 스크립트로 알려져 있습니다. 확장자가 .cgi인 파일에 저장되는 스크립트는 일반적으로 C 또는 Perl 프로그래밍 언어로 작성됩니다. 웹 개발자가 데이터베이스를 웹 서버에 연결하기를 원했던 웹 초기부터 도입되었습니다. 웹 서버와 데이터베이스 간의 공통 게이트웨이를 지원하는 서버는 CGI 코드를 실행하는 데 적합했습니다.

## CGI 파일 형식
CGI 스크립트는 웹 서버에서 소유자가 URL을 처리하는 방법을 쉽게 구성하는 데 사용됩니다. 절차는 일반적으로 새 디렉토리(문서가 주로 있는)를 CGI 스크립트를 포함하는 것으로 표시하여 수행됩니다. 일반적으로 알려진 이름은 cgi-bin입니다. 예를 들어, /usr/local/apache/htdocs/cgi-bin은 웹 서버에서 CGI 디렉토리로 선택될 수 있습니다. 웹 브라우저가 CGI 디렉토리 내의 파일을 가리키는 URL을 요청하면 해당 파일(/ko/usr/local/apache/htdocs/cgi-bin/printenv.pl)을 웹 브라우저로 보내는 대신 HTTP 서버는 지정된 스크립트를 실행하고 스크립트의 출력을 웹 브라우저에 반환합니다. 간단히 말해서 CGI 스크립트가 표준 출력으로 전송되는 모든 것은 창의 터미널에 표시되지 않고 웹 클라이언트로 전송됩니다.

### CGI 예

웹 서버에 의해 전달된 모든 환경 변수를 보여주는 Perl로 작성된 다음 CGI 스크립트:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

출력은 다음과 같습니다.
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## CGI 스크립트 사용
CGI 스크립트가 포함된 CGI 파일은 일반적으로 사용자의 입력 데이터를 처리하고 관련 출력 데이터를 생성하는 데 사용됩니다. 위키 구현은 CGI 프로그램의 예 중 하나입니다. 사용자 에이전트가 항목 이름에 대한 요청을 보내면 웹 서버는 CGI 프로그램을 실행합니다. CGI 프로그램은 해당 항목 페이지의 소스를 가져와 HTML로 변환하고 결과를 인쇄합니다. 웹 서버는 CGI 프로그램에서 출력을 받아 사용자 에이전트에 반환합니다. 그런 다음 사용자 에이전트가 "페이지 편집" 버튼을 클릭하여 편집 기능을 호출하면 CGI 프로그램은 페이지 내용과 함께 HTML 텍스트 영역 또는 기타 편집 컨트롤을 표시합니다. 마지막으로 사용자 에이전트가 "페이지 게시" 버튼을 클릭하면 CGI 프로그램은 업데이트된 HTML을 해당 항목 페이지의 소스로 변환하고 저장합니다.



## 참고문헌

* [공통 게이트웨이 인터페이스 - Wikipewdia 제공](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

