{
  "date" : "2019-10-11",
  "keywords" :[ "mhtml","mhtml 파일", "mhtml 파일 형식", "mhtml 파일 형식", "파일", "유형", "mhtml 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHTML - MIME HTML 파일",
  "description":"MHTML 파일 형식과 MHTML 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .MHTML 파일이란?

MHTML 확장자를 가진 파일은 다양한 응용 프로그램에서 만들 수 있는 웹 페이지 아카이브 형식을 나타냅니다. 이 형식은 웹 **[HTML](/ko/web/html/)** 코드 및 관련 리소스를 단일 파일에 저장하기 때문에 아카이브 형식으로 알려져 있습니다. 이러한 리소스에는 이미지, 애플릿, 애니메이션, 오디오 파일 등과 같이 웹페이지에 연결된 모든 것이 포함됩니다. MHTML 파일은 Internet Explorer 및 Microsoft Word와 같은 다양한 응용 프로그램에서 열 수 있습니다. Microsoft Windows는 Windows에서 문제를 일으키는 응용 프로그램을 사용하는 동안 관찰된 문제 시나리오를 기록하기 위해 MHTML 파일 형식을 사용합니다. MHTML 파일 형식은 일반 텍스트 이메일 관련 사양인 message/rfc822에 정의된 사양과 유사한 페이지 내용을 인코딩합니다. 형식의 실제 사양은 [RFC 2557](https://tools.ietf.org/html/rfc2557)에 자세히 나와 있습니다.

## MHTML 파일 형식

MHTML은 HTML 웹 페이지와 해당 리소스를 단일 웹 아카이브로 인코딩하는 기능으로 인해 HTML 문서 집계의 MIME 캡슐화라고도 합니다. RFC 2557 사양에 따라 집계 문서는 루트 리소스(객체)와 URI를 통해 이에 연결된 기타 리소스를 포함하는 MIME 인코딩 메시지입니다. 이러한 다른 리소스는 인라인 그림, 스타일 시트, 애플릿 등의 표현일 수 있습니다. 또한 이들은 다른 멀티미디어 문서의 루트가 될 수 있습니다. MHTML 파일 형식에 대한 전체 문서 사양은 [RFC 2557](https://tools.ietf.org/html/rfc2557)에 자세히 설명되어 있으며 이 파일 형식의 읽기/쓰기를 위한 모든 종류의 응용 프로그램 개발에 참조되어야 합니다. 이 표준은 참조할 본문 부분이 Content-ID 또는 Content-Location으로 식별될 수 있다고 지정합니다.

### MIME 콘텐츠 헤더

MIME 콘텐츠 헤더인 Content-Location은 다른 본문 부분의 리소스에 대한 URI 참조를 확인하기 위해 정의됩니다. 이 헤더는 모든 메시지 또는 콘텐츠 제목에 나타날 수 있습니다.

### 콘텐츠 위치 헤더

Content-Location은 그것이 배치되는 본문 부분의 내용에 레이블을 지정하는 URI의 표현입니다. 그 값은 절대 또는 상대 URI일 수 있습니다. 메시지의 일부 또는 전체 수신자가 검색할 수 없는 리소스에 레이블을 지정하는 데 사용할 수 있습니다. 단일 메시지에는 단일 Content-Location 헤더만 있을 수 있습니다. Content-Location 및 Content-ID 레이블이 모두 있는 본문 부분을 포함하는 다중 부분/관련 구조의 예:

```
Content-Type: multipart/related; boundary#"boundary-example";
                    type#"text/html"

      --boundary-example

      Content-Type: text/html; charset#"US-ASCII"

      ... ... <IMG SRC#"fiction1/fiction2"> ... ...
      ... ... <IMG SRC#"cid:97116092811xyz@foo.bar.net"> ... ...

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092511xyz@foo.bar.net>
      Content-Location: fiction1/fiction2

      --boundary-example
      Content-Type: image/gif
      Content-ID: <97116092811xyz@foo.bar.net>
      Content-Location: fiction1/fiction3

      --boundary-example--
```

### MHTML 집계의 URI

MHTML 집계의 URI는 루트 URI의 URI와 다릅니다. Content-Location 헤더 필드는 멀티파트/관련 제목의 제목에 사용되는 경우 전체 집계에 적용되어야 합니다. 유사하게, 검색된 리소스 세트는 MHTML 집계를 참조하는 URI가 이 집계를 검색하는 데 사용될 때 해당 부분의 Content-Locations를 사용하여 검색된 리소스 세트와 다를 수 있습니다. 예를 들어, MHTML 집계를 검색하면 이전 버전이 반환될 수 있는 반면 루트 URI 및 인라인 연결된 개체를 검색하면 최신 버전이 반환될 수 있습니다.

## 참고문헌

* [집계 문서의 MIME 캡슐화 - RFC 2557](https://tools.ietf.org/html/rfc2557)
* [MHTML 파일 형식 - 위키피디아 작성](https://en.wikipedia.org/wiki/MHTML)

