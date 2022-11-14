{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7C - PKCS 7 인증서 파일",
  "description":"P7C 파일을 만들고 열 수 있는 P7C 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "P7C",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## .P7C 파일이란?

P7C 파일은 다른 보안 인증서 파일과 마찬가지로 네트워크를 통해 ID를 인증하는 데 사용되는 디지털 인증서입니다. 인증서를 사용하는 응용 프로그램은 이러한 인증서 파일에 포함된 공개 키를 사용하여 ID를 인증합니다. 공개 키 암호화 또는 비대칭 암호화는 하나는 공개 키이고 다른 하나는 개인 키라고 하는 키 쌍을 사용합니다. 개인 키는 효과적인 보안을 위해 안전하게 보관되며 공개 키는 다른 사람과 공유할 수 있습니다. 다른 일반적인 인증서 파일 형식에는 [CRT](/ko/web/crt/), DER 및 PEM이 있습니다.

## P7C 파일 형식 - 추가 정보

P7C 파일은 바이너리 파일로 디스크에 저장되며 수학적 문제에 기반한 암호화 알고리즘을 사용하여 생성된 공개 키 정보를 포함합니다. 이들은 모든 텍스트 편집기에서 열 수 있지만 그 내용은 사람이 읽을 수 있는 형식이 아닙니다. P7C 파일을 열 수 있는 일부 응용 프로그램에는 Apple Keychain Access, Adobe Acrobat Reader DC, Microsoft 인증서 관리자 및 Microsoft Windows 연락처가 있습니다.

### P7C 파일 형식 예

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 참조 ##

* [공개 키 암호화](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C 파일 생성은 어떻게 하나요?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

