{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S 파일 - 디지털 서명된 이메일 메시지",
  "description":"P7S 파일 형식과 P7S 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## .P7S 파일이란?

P7S 파일은 디지털 서명된 이메일과 함께 수신되는 디지털 서명입니다. 이 파일이 전자 메일과 함께 첨부 파일로 존재하면 전자 메일이 원본에서 보낸 것임을 확인합니다. 이렇게 하면 보낸 사람의 컴퓨터에 전자 메일 서명 인증서가 설치되어 있는지 확인할 수 있습니다. 이러한 서명된 이메일이 사용자의 컴퓨터에서 전송되면 보낸 사람의 이름이 포함된 P7S 파일이 첨부됩니다. 서명된 이메일을 지원하는 이메일 클라이언트는 보낸 사람의 정보를 볼 수 있습니다.

## P7S 파일 형식 - 추가 정보

S/MIME(Secure/Multipurpose Internet Mail Extensions) P7S 파일에는 사람이 읽을 수 있는 일반 텍스트 형식의 정보가 포함되어 있습니다. Microsoft Outlook, Apple Mail 및 Mozilla Thunderbird와 같은 이메일 클라이언트는 S/MIME 이메일에서 디지털 서명된 정보를 읽을 수 있도록 지원합니다. 이메일에 서명하면 발신자의 신원이 확인되고 수신자에게 메시지가 진짜임을 알립니다. 이메일 클라이언트([EML](/ko/email/eml/) 또는 [MSG](/ko/email/msg/))에서 이메일을 다운로드하면 이러한 P7S 파일이 이러한 이메일에 첨부되어 있습니다.

P7S 파일에는 다음 정보가 포함됩니다.

* 이메일 출처
* 보낸 날짜와 시간,
* 전송 중 수정 여부

이 정보는 전자 메일에 암호화된 서명을 디지털 방식으로 첨부하기 위한 PKCS7(공개 키 암호화 표준 #7) 기술을 사용하여 포함됩니다.

## 참조 ##

* [Microsoft 서명 도구](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

