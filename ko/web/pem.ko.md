{
  "date" : "2022-09-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEM 파일 - 개인 정보 보호 강화 메일 인증서 파일 형식",
  "description":"PEM 파일 형식과 PEM 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "PEM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-14"
}

## .PEM 파일이란?

PEM 파일은 웹 서버와 브라우저 간의 보안 통신 채널을 설정하는 데 사용되는 보안 인증서 파일입니다. Base64로 인코딩되며 개인 키, 서버 인증서 및/또는 다른 인증서의 조합을 포함할 수 있습니다. PEM 파일은 사용 면에서 .der 인증서 파일과 유사하지만 바이너리 데이터가 아닌 Base64로 인코딩된 텍스트로 저장됩니다. 다른 유사한 인증서 파일 형식에는 [.cer](/ko/web/cer/) 및 [.crt](/ko/web/crt/) 파일이 있습니다.

**PEM 파일을 열 수 있는** 응용 프로그램에는 Microsoft 메모장 및 Apple TextEdit와 같은 텍스트 편집기가 포함됩니다.

## PEM 파일 형식

PEM은 데이터를 저장하는 데 사용되는 파일의 구조와 인코딩 유형을 정의하는 컨테이너 파일 형식입니다. PEM 파일은 사람이 읽을 수 없는 Base64 인코딩 파일 형식으로 디스크에 저장됩니다. 표준은 PEM 파일이 다음으로 시작한다고 정의합니다.

```
-----BEGIN <type>-----
```
다음으로 끝납니다.
```
-----END <type>-----
```

이 안에 있는 다른 모든 콘텐츠는 base64로 인코딩됩니다(대소문자, 숫자, + 및 /). 단일 PEM 파일은 다른 프로그램에서 사용할 수 있는 여러 블록으로 구성될 수 있습니다. PEM 파일에 여러 인증서가 포함된 경우 각 인증서는 다음과 같이 개별 블록으로 구분됩니다.

```
-----BEGIN CERTIFICATE-----
  //end-user
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //intermediate
-----END CERTIFICATE-----
-----BEGIN CERTIFICATE-----
  //root
-----END CERTIFICATE-----
```

### PEM 파일 예

CERTIFICATE 블록이 있는 PEM 파일은 일반적으로 다음과 같습니다.

```
---- BEGIN CERTIFICATE----

EggHozdmgGz7zbC1mcJ2rcNAQEEBBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcMIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUQAwgY8xCzAJBgNVNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

RSA가 있는 PEM 파일은 다음과 같이 시작됩니다.

```
-----BEGIN RSA PRIVATE KEY-----
```

## 참조 ##

* [공개 키 암호화](https://en.wikipedia.org/wiki/Public-key_cryptography)
* [P7C 파일 생성은 어떻게 하나요?](https://www.ibm.com/support/pages/how-create-pkcs7-p7b-p7c-certificate-your-trading-partner)

