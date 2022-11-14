{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - 이메일 메시지",
  "description":"EML 파일을 만들고 열 수 있는 EML 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## .EML 파일이란?

EML 파일 형식은 Outlook 및 기타 관련 응용 프로그램을 사용하여 저장된 전자 메일 메시지를 나타냅니다. 거의 모든 이메일 클라이언트는 RFC-822 인터넷 메시지 형식 표준을 준수하기 위해 이 파일 형식을 지원합니다. Microsoft Outlook은 EML 메시지 유형을 여는 기본 소프트웨어입니다. EML 파일은 디스크에 저장하고 통신 프로토콜을 사용하여 수신자에게 보내는 데 사용할 수 있습니다.

## EML의 간략한 역사

EML 파일 형식 사양은 [RFC 822](http://www.ietf.org/rfc/rfc0822.txt) 표준 형식에 따라 제공됩니다. RFC-822 이전에는 RFC-733이 1982년까지 네트워크 메시지 교환 규칙을 관장했으며, 전자는 ARPA 표준을 수립하여 측면을 개선하기 위해 만들어졌습니다. 동시에 Microsoft는 Outlook Express와 같은 자체 이메일 클라이언트 개발을 위해 자체 COM 모듈을 만들었습니다. RFC-822는 마이크로소프트가 개방형 표준에서 벗어나 고도로 구조화된 데이터베이스 형식으로 이메일을 저장하는 [PST](/ko/email/pst/) 파일 형식을 만들면서 독점 형식으로 확립되는 길을 택했다. 이로 인해 Microsoft Outlook에서 전자 메일을 전달할 때 타사 전자 메일 클라이언트 사용자에게 문제가 발생했습니다.

2001년에 822 표준이 2822로 향상되었습니다. 현재 MIME RFC-822 형식으로 EML 메시지를 만들고 읽고 보내는 데 사용되는 인터넷 메시지 형식입니다.

## EML 파일 형식 사양

EML 파일은 두 개의 구별된 섹션으로 구성됩니다.

* 헤더 - 메시지 헤더에 대한 정보를 포함합니다.
* 메시지 본문 - 메시지 내용, 포함된 이미지 및 첨부 파일을 포함할 수 있는 일련의 정보를 포함합니다.

### 헤더 정보 ###

EML 파일은 헤더 정보와 선택적으로 메시지 본문으로 구성됩니다. EML의 각 헤더 행에는 콜론 ":"으로 구분된 두 부분이 있습니다. 첫 번째 이름은 헤더 이름이고 콜론 다음은 헤더 본문입니다. 예를 들어, 이러한 헤더에는 다음이 포함됩니다.

* 보내는 사람 이메일 주소
* 받는 사람 이메일 주소
* 이메일 제목
* 메시지의 시간 및 날짜 스탬프

**예제 헤더**

에서:<John@bmw.eml.light.com>

에게:<Andy@fileformat.com>

날짜: 2018년 3월 8일 목 10:43:37 +0100

제목: bmw eml 라이트

### 메시지 본문 ###

EML 메시지 본문에는 텍스트, 하이퍼링크 및 첨부 파일 형식의 이메일 기본 정보가 포함됩니다. 이메일 본문에는 읽을 수 있는 일반 텍스트가 포함될 수 있지만 반드시 필요한 것은 아닙니다. 이 경우 메시지 본문은 비어 있거나 인코딩된 첨부 파일 데이터를 포함할 수 있습니다.

메시지 본문의 내용은 읽기 응용 프로그램이 각 형식의 정보를 읽을 수 있도록 하는 Content-Type으로 설명됩니다. 실제로 문서의 성격과 형식을 나타냅니다. MIME 유형 또는 콘텐츠 유형의 구조는 매우 간단합니다. 유형 및 하위 유형, '/'로 구분된 두 개의 문자열로 구성됩니다. 공간이 허용되지 않습니다. '유형'은 범주를 나타내며 이산 또는 다중 파트 유형이 될 수 있습니다. '하위 유형'은 각 유형에 따라 다릅니다. Content-Type 범주에 속하는 유형 목록은 길지만 몇 가지 중요한 콘텐츠 유형은 다음과 같습니다.


|**유형**|**설명**|**하위 유형의 예**
---|---|---|
|text|사람이 읽을 수 있는 형식을 나타냄|text/plain, text/html, text/css, text/javascript
|이미지|동영상을 제외한 모든 유형의 이미지를 나타냄|이미지/bmp, 이미지/png, 이미지/jpg, 이미지/gif
|오디오|모든 오디오 파일 형식을 나타냄|오디오/mdi, 오디오/wav
|application|모든 종류의 바이너리 데이터를 나타냄|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### EML Body의 Attachment 표현 ###

EML 본문에는 포함된 각 콘텐츠 유형에 대한 경계가 포함됩니다. 메시지 본문의 첨부 파일은 다음 예와 같이 Content-Type 및 Content-Disposition으로 식별됩니다.

콘텐츠 유형: 텍스트/일반; charset#"windows-1252"; name#"애플 앱 스토어.txt"
내용-처분: 첨부; 파일명#"애플 앱 스토어.txt"
콘텐츠 전송 인코딩: base64
X-첨부 파일 ID: f_jkhztmd02

알 수 있는 바와 같이 Content-Disposition을 첨부로 설정하면 읽기 애플리케이션이 첨부 파일 이름 및 전송 인코딩과 같은 첨부 정보를 얻을 수 있습니다. 첨부 헤더 정보 뒤에는 읽을 인코딩된 첨부 콘텐츠가 옵니다.

#### 스프레드시트를 첨부로 사용한 예 ####

콘텐츠 유형: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
내용-처분: 첨부; 파일명#"english_spodr.xlsx"
콘텐츠 전송 인코딩: base64
X-첨부 파일 ID: f_jkhztmd43

## 참고문헌

* [RFC 822](http://www.ietf.org/rfc/rfc0822.txt)

