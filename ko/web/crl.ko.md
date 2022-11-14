{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRL 파일 - 인증서 해지 목록",
  "description":"CRL 파일 형식과 CRL 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## .CRL 파일이란?

CRL(인증서 해지 목록) 파일은 할당된 해지 날짜 이전에 인증 기관(CA)이 해지하는 X.509 디지털 인증서의 블랙리스트입니다. 여기에는 보안 관리자가 영향을 받는 디지털 인증서를 차단할 수 있도록 하는 해지 날짜 및 문제에 대한 정보가 포함되어 있습니다. CRL은 주요 목적이 신뢰할 수 없고 유효하지 않은 인증서에 대해 알리는 것이기 때문에 만료된 인증서를 포함하지 않습니다.

**CRL 파일을 열 수 있는** 응용 프로그램에는 OpenSSL, Microsoft IIS Server 및 Citrix NetScaler가 있습니다.

## CRL 파일 형식 - 추가 정보

CRL 파일에는 공개 키 정보를 공유하기 위한 의미 체계도 정의하는 X.509 표준의 정보가 포함되어 있습니다. CRL 파일에 포함된 기타 정보에는 인증서가 해지된 시간 제한, 해지 이유, 해지된 인증서의 일련 번호 및 타임스탬프가 포함될 수 있습니다.


### 인증서가 CRL에 추가되는 주요 이유

웹사이트의 인증서를 취소하고 CRL에 추가하는 데에는 여러 가지 이유가 있을 수 있습니다. 그들 중 일부는 될 수 있습니다.

1. 인증서의 개인 키가 손상되었습니다.
1. 인증서가 유효하지 않거나 CA에서 잘못 발급한 경우
1. 인증서와 관련된 조직 세부 정보가 변경되고 CA가 새 인증서를 발급합니다.
1. 그 밖에 부득이한 사유로 인증서가 취소된 경우

## 참고문헌

* [국립표준기술원(NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [IETF(Internet Engineering Task Force) RFC 5280](https://tools.ietf.org/html/rfc5280)
* [인증취소 목록](https://en.wikipedia.org/wiki/Certificate_revocation_list)

