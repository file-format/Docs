{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MBOX - 이메일 사서함 파일",
  "description":"MBOX 파일을 만들고 열 수 있는 MBOX 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "MBOX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .MBOX 파일이란?

MBox 파일 형식은 전자 메일 메시지 모음을 위한 컨테이너를 나타내는 일반적인 용어입니다. 메시지는 첨부 파일과 함께 컨테이너 내부에 저장됩니다. 전체 폴더의 메시지는 단일 데이터베이스 파일에 저장되고 새 메시지는 파일 끝에 추가됩니다. 수많은 응용 프로그램과 API가 Apple Mail 및 Mozilla Thunderbird와 같은 MBox 파일 형식을 지원합니다.

## MBOX 파일 형식 ##

MBox 파일 형식은 application/mbox가 RFC 2822 형식의 [RFC 4155.](https://tools.ietf.org/rfc/rfc4155.txt) 메시지로 표준화된 2005년까지 꽤 오랫동안 표준화되지 않은 상태로 남아 있었습니다. , MBox 파일 형식 내에서 차례로 연결됩니다. 각 메시지는 메시지 발신자를 식별하는 구분선으로 시작하고 최종 수신자(전송 경로의 마지막 홉 시스템 또는 수신자의 역할을 하는 시스템)가 메시지를 수신한 날짜와 시간도 식별합니다. 우편물). 각 메시지는 일반적으로 빈 줄로 종료됩니다. 데이터베이스의 끝은 일반적으로 추가 데이터가 없거나 명시적인 파일 끝 표시가 있는 것으로 인식됩니다.

## MBox 파일에서 메시지 읽기 ##

판독기는 From_ 라인을 찾는 mbox 파일을 스캔합니다. 모든 From_ 행은 메시지의 시작을 표시합니다. 독자는 모든 From_ 라인(파일 시작 부분 이후)이 비어 있다는 사실을 이용하려고 해서는 안 됩니다. 독자가 메시지를 찾으면 From_ 라인에서 (손상되었을 수 있는) 봉투 발신자와 배달 날짜를 추출합니다. 그런 다음 다음 From_ 줄 또는 파일 끝 중 먼저 오는 쪽까지 읽습니다. 마지막 빈 줄을 제거하고 >From_ 줄 및 >>From_ 줄 등의 인용을 삭제합니다. 결과는 RFC 822 메시지입니다.

## 인코딩 고려 사항 ##

수신된 이메일에 Mbox 파일이 첨부되어 있고 다른 Mbox 파일에 저장되면 MBox 파일의 내용이 되돌릴 수 없을 정도로 뒤섞일 수 있습니다. 이를 방지하기 위해 메시징 시스템은 이러한 개체가 메시징 프로토콜을 통해 전송될 때마다 불투명한 전송 인코딩(예: BASE64 또는 Quoted-Printable)으로 mbox 데이터베이스를 인코딩해야 합니다. 또한 구현자는 비준수 데이터가 수신되는 경우 mbox 데이터를 로컬로 인코딩할 준비를 해야 합니다.

## 참조 ##

* [엠박스 - RFC4155](https://tools.ietf.org/rfc/rfc4155.txt)
* [엠박스 - 위키피디아](https://en.wikipedia.org/wiki/Mbox)
