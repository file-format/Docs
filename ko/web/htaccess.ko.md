{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS 파일 - Apache HTACCESS 파일 형식",
  "description" :"HTACCESS 파일이 무엇인지 알아보기 위한 파일 형식 가이드",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .HTACCESS 파일이란?

HTACCESS 파일은 웹 사이트의 다른 폴더/디렉토리에 대한 구성 변경을 허용하는 메커니즘을 제공하는 Apache 구성 파일입니다. 여기에는 디렉토리 및 하위 디렉토리에 적용할 수 있는 구성 지시문이 포함됩니다.

HTACCESS 파일은 웹 사이트의 인덱스 페이지 정의, 404(페이지를 찾을 수 없음) 오류 페이지 나열, 301 또는 302 페이지 리디렉션 수행, 특정 IP 주소 또는 다른 웹 사이트의 액세스 차단과 같은 여러 검사를 수행합니다. 따라서 .htaccess 파일을 사용하면 Apache [HTTP](/ko/web/http/) 서버의 전체 성능이 저하됩니다.

## HTACCESS 파일 형식

HTACCESS 파일은 일반 텍스트 파일 형식으로 디스크에 저장됩니다. 즉, 모든 텍스트 편집기에서 이러한 파일을 열고 편집할 수 있습니다. "." 앞에 이름이 없습니다. .htaccess 파일에서 폴더 내의 숨겨진 파일임을 보여줍니다.

## HTACCESS 파일의 일반적인 용도

HTACCESS 파일의 다섯 가지 일반적인 용도는 다음과 같습니다.

### Mod_Rewrite

HTACCESS 파일을 사용하여 웹 사이트의 URL 및 웹 페이지가 사용자에게 표시되는 방식을 지정하고 변경할 수 있습니다.

### 인증

.htpasswd라는 암호 파일을 만들어 .htaccess로 인증할 수 있습니다. 이렇게 하면 사이트 방문자가 웹 페이지의 특정 섹션을 방문하려는 경우 암호를 제공할 수 있습니다.

### 사용자 정의 오류 페이지

400 잘못된 요청, 401 승인 필요, 403 금지된 페이지, 404 파일을 찾을 수 없음 및 500 내부 오류와 같은 사용자 정의 오류 페이지를 .htaccess 파일로 생성할 수 있습니다. 그러나 이러한 모든 검사는 페이지에 액세스할 때 실행되므로 서버 성능이 느려집니다.

### MIME 유형

Apache HTACCESS 파일은 MIME(Multipurpose Internet Mail Extensions) 유형을 포함하도록 수정할 수 있습니다. 이렇게 하면 서버가 사이트에서 지원하지 않는 응용 프로그램 파일의 전달을 지원할 수 있습니다.

### SSI

SSI(Server Side Include)는 웹 사이트에서 시간을 크게 절약해 줍니다. SSI는 다음 코드를 .htaccess 파일에 삽입하여 활성화할 수 있습니다.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS 파일 예

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## 참고문헌

* [Apache HTTP 서버 튜토리얼: .htaccess 파일](https://httpd.apache.org/docs/current/howto/htaccess.html)

