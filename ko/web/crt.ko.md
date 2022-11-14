{
  "date" : "2019-10-11",
  "keywords" :[ "crt","crt 파일", "crt 파일 형식", "crt 파일 형식", "파일", "유형", "crt 파일이란" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRT - 보안 인증서 파일 형식",
  "description":"CRT 파일 형식과 CRT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CRT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .CRT 파일이란?

확장자가 .crt인 파일은 웹 서버에서 브라우저로 보안 연결을 설정하기 위해 보안 웹 사이트에서 사용하는 보안 인증서 파일입니다. 보안 웹사이트를 통해 데이터 전송, 로그인, 지불 카드 거래를 보호하고 사이트에 대한 보호된 브라우징을 제공할 수 있습니다. 보안 웹사이트를 열면 주소 표시줄에 "잠금" 아이콘이 표시됩니다. 클릭하시면 설치된 인증서의 상세내역을 보실 수 있습니다. Verisign 및 Thawte와 같은 국제 회사에서 이러한 SSL 인증서를 배포합니다.

## CRT 파일 형식

CRT 파일은 ASCII 형식이며 모든 텍스트 편집기에서 열어 인증서 파일의 내용을 볼 수 있습니다. 인증서의 구조를 정의하는 X.509 인증 표준을 따릅니다. SSL 인증서에 포함되어야 하는 데이터 필드를 정의합니다. CRT는 Base64 ASCII 인코딩 파일인 인증서의 PEM 형식에 속합니다.

### PEM 파일 구조

PEM 파일에는 여러 인증서가 있을 수 있습니다. 이 경우 PEM 파일의 각 인증서는 다음 구조를 따릅니다.

```
---- BEGIN CERTIFICATE----
...
...
...
Encoded string for encryption of data
...
...
...
----END CERTIFICATE----
```

### CRT 파일 형식 예

```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 참조 ##

* [공개 키, 개인 키 및 인증서](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

