{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7B - PKCS 7 인증서 파일",
  "description":"P7C 파일 형식과 P7C 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "P7B",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .P7B 파일이란?

P7B 파일은 사람 또는 장치를 인증하기 위한 보안 디지털 인증서가 포함된 보안 인증서 파일입니다. [.cer](/ko/web/cer/) 인증서 파일과 유사하게, P7B 파일은 파일에서 오른쪽 클릭 옵션을 사용하여 "인증서 설치" 옵션을 사용하여 설치할 수 있습니다. P7B는 CER 파일 형식과 다른 형식 옵션을 사용합니다. 여기에는 base64(ASCII) 인코딩을 사용하는 하나 이상의 X.509 디지털 인증서 파일이 포함되어 있습니다. P7B 파일은 [ZIP](/ko/compression/zip/) 파일로 받거나 인증 기관에서 받습니다.

## P7B 파일 형식

P7B 파일은 모든 텍스트 편집기에서 열 수 있는 일반 ASCII 파일로 저장됩니다. 그것은 가독성 관점에서 의미가 없는 인코딩된 문자열인 공개 키를 포함합니다.

### P7B 파일 형식 예

```
---- BEGIN CERTIFICATE----

XjlakuoieulalxkjflaiuEggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYQDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 참조 ##

* [공개 키 암호화](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C 파일 생성은 어떻게 하나요?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

