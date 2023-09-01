{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"테네프",
  "description":"TNEF 파일을 만들고 열 수 있는 TNEF 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "TNEF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .TNEF 파일이란?

TNEF(Transport Neutral Encapsulation Format)는 메시징 응용 프로그래밍 인터페이스(**MAPI**)를 기반으로 전자 메일 첨부 파일을 캡슐화하기 위한 Microsoft 독점입니다. Microsoft Outlook 및 Microsoft Exchange Server는 TNEF를 완전히 지원하지만 나중에 TNEF를 MAPI로 디코딩하고 형식이 지정된 메일을 표시합니다. TNEF 인코딩이 포함된 전자 메일 첨부 파일에는 MIME 유형이 MS-TNEF이며 winmail/win.dat로 저장됩니다. winmail .dat의 첨부 파일은 다음 정보를 캡슐화합니다.


|메시지|OLE 개체|Outlook 기능
---|---|---|
|<ul><li> 원본 메시지 첨부 파일</li><li> 형식이 지정된 원본 버전</li><li> 글꼴, 텍스트 크기 및 텍스트 색상</li></ul> |<ul><li> 포함된 사진</li><li> 포함된 Office 문서</li></ul> |<ul><li> 사용자 정의 양식</li><li> 투표 버튼</li><li> 회의 요청</li></ul>


TNEF를 지원하지 않는 다른 이메일 서비스는 TNEF 형식의 메시지에 대해 일반 텍스트를 제공합니다. Outlook은 TNEF 파일(OLE) 또는 특정 Outlook 기능(양식, 폴링 단추 및 회의 요청)에 다양한 형식의 메시지를 포함합니다. Outlook 전자 메일 클라이언트 내에서 명시적 TNEF 인코딩을 승인하는 것은 불가능하지만 전자 메일 발송을 위해 RTF 형식을 선택하면 TNEF 인코딩이 암시적으로 용이합니다.

## TNEF 파일 형식

TNEF 데이터 알고리즘은 풍부한 계층적 메시지 속성에서 평면 구조를 설정합니다. 이러한 평면 구조는 특정 속성으로 구성된 직렬 데이터 스트림을 나타내는 데 사용됩니다.

속성이 그룹으로 발생하거나 여러 값이 있는 일부 상황에서 스트림에는 특정 데이터 정렬을 적용하기 위해 개수와 패딩이 포함될 수 있습니다. 이 알고리즘의 사용이 유리한 독특한 상황은 지원되지 않는 메시징 환경입니다. 이러한 환경에서 풍부한 메시지 속성은 TNEF 작성기에 의해 직렬 데이터 스트림으로 인코딩됩니다. 또한 기본 TNEF에 속하지 않는 속성은 전송 중에 캡슐화될 수 있습니다. 이러한 캡슐화된 속성은 클라이언트 응용 프로그램에 대한 원본 메시지의 모든 속성 가용성을 보장하기 위해 TNEF를 통해 디코딩하여 사용할 수 있습니다.

TNEF에서 모든 숫자 데이터 유형은 리틀 엔디안이며 크기는 1바이트보다 큽니다. 리틀 엔디안이 아닌 플랫폼에서 이러한 숫자 값을 처리하려면 올바른 값을 얻기 위해 적절한 변환을 수행해야 합니다. 문자열 값은 [RFC5234] 사양에 따라 ABNF(Augmented Backus-Naur Form) 형식으로 표시됩니다. 문자열이 null 문자로 끝나는 경우 해당 문자열도 포함됩니다. 예: `"worker@specimen.com" %x00`.

{{< figure src="../TNEF.png" alt="TNEF 파일 형식" >}}

## TNEF 속성 및 처리 규칙 ##

TNEF의 데이터 스트림은 레거시 버전 번호, 서명, 기본 키 값 및 코드 페이지를 나타내는 속성으로 시작합니다. 이 코드 페이지는 인코더가 ANSI 특성 및 속성을 기록할 때 생성됩니다. 그 후 스트림은 메시지 속성이 먼저 정렬된 다음 첨부 속성이 뒤따르는 일련의 속성이 되었습니다. attMsgProps, attAttachment 및 attRecipTable과 같은 특수 속성에는 다양한 메시지 및 첨부 파일 특성이 포함되어 있습니다. TNEF 스트림에 나타나는 속성에는 구조, 메시지 속성 및 메시지 속성과 연결하는 데 필요한 변환이 포함됩니다. 각 속성은 해당 속성의 ID, 크기 및 데이터, 체크섬 및 적용에 따른 수준으로 구성됩니다.

## 프로토콜 및 기타 알고리즘과의 관계 ##

풍부한 메시지 형식을 표시하는 메커니즘이 좋지 않은 시스템에는 기본적으로 전송을 위한 TNEF 데이터 알고리즘이 필요합니다. ms-TNEF 미디어 유형을 사용하여 알고리즘의 출력은 첨부 파일(winmail.dat)과 [RFC2045]에 지정된 MIME의 본문 부분으로 구성됩니다. 일반 텍스트 메시지 본문은 [MSDN-UAF] 사양에 따라 UUENCODE를 사용하여 전송되며 이 메시지 본문 또는 이와 동등한 방법은 수신자 측에서 디코딩됩니다. 또한 TNEF는 SMTP, POP3, IMAP4와 같은 다양한 인터넷 프로토콜을 사용하여 메시지 데이터를 전송할 수 있으며 RFC2045 표준에 따라 MIME를 통합합니다.

## 적용 가능성 진술 ##

간단한 메시지 전송 외에도 TNEF의 원래 응용 프로그램은 메시지 클래스를 사용하고 전송 프로토콜에서 원래 지원하지 않는 추가 기능을 지원하기 위해 만들어졌습니다. 이 응용 프로그램은 오늘날 현대 메시징 클라이언트가 사용하는 풍부한 메시지 속성 및 명명된 속성의 전송을 위해 더욱 개선되었습니다. 원래 구현을 준수하기 위해 원래 속성 구문이 유지되고 특수 속성은 새 메시지 속성을 별도로 보유합니다.

## 참고문헌

* [전송 중립 캡슐화 형식](https://en.wikipedia.org/wiki/Transport_Neutral_Encapsulation_Format)
* [Exchange Server의 이메일 주소 및 주소록](https://learn.microsoft.com/en-us/exchange/email-addresses-and-address-books/email-addresses-and-address-books?view# exchserver-2019)
* [[MS-OXTNEF]: TNEF(Transport Neutral Encapsulation Format) 데이터 알고리즘](https://msdn.microsoft.com/en-us/library/cc425498(v#exchg.80).aspx)

