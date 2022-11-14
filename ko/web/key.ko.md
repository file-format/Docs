{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"KEY 파일 형식과 KEY 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"KEY 파일 형식 - 개인 정보 보호 강화 메일 개인 키 파일",
  "linktitle" : "KEY",
  "menu" : {
    "docs" : {
      "identifier":"web-key",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## .KEY 파일이란?

KEY 파일은 PEM(Privacy-Enhanced Mal) 파일 형식으로 디스크에 저장되는 보안 메커니즘의 개인 부분입니다. 웹 브라우저와 브라우징 요청을 제공하는 웹 서버 간에 교환되는 정보를 해독하는 데 사용됩니다. KEY 파일에는 사람의 눈에는 쓸모가 없지만 웹 서버에서 SSL 인증서의 일부로 정보 교환을 암호화/복호화하는 핵심인 인코딩된 문자열이 포함되어 있습니다. KEY 파일은 자동으로 생성되어 클라이언트 측에서 설치됩니다.

**KEY** 파일은 Microsoft 메모장(Windows), Apple TextEdit(Mac) 또는 GitHub Atom(교차 플랫폼)과 같은 텍스트 편집기로 열 수 있습니다. KEY 파일은 [CRT](/ko/web/crt/) 및 [CER](/ko/web/cer/) 파일 형식과 유사합니다.

## KEY 파일 형식 - 추가 정보

KEY 파일은 일반 텍스트 파일로 디스크에 저장되지만 사람이 읽기에는 적합하지 않은 인코딩된 문자열입니다. 실제로 사용자는 텍스트 편집기에서 열 때 문자열에 대해 전혀 이해하지 못합니다. 개인 키 인증서는 기밀이며 누구와도 공유해서는 안 됩니다. 인터넷을 통한 정보 교환 보안의 전체 프로세스에는 다음이 포함됩니다.

* **공개 키** - 브라우저와 웹 서버 간의 데이터 교환을 위해 사용자 정보를 암호화하는 데 사용
* **개인 키** - 웹 서버에서 수신한 정보를 해독하는 데 사용됩니다.

X.509 인증서라고도 하는 SSL 인증서는 웹사이트마다 고유합니다. 다음 구문을 사용하는 KEY 파일:

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

### 키 파일 예

다음은 개인 키 파일의 예입니다.
```
---- BEGIN CERTIFICATE----

MIICUDCCAdoCBDaM1tYwDQYJKoZIhvcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9lVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYwDQYJKoZIhvcNAQEEBQAwgY8xCzAkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7wgY8xCzAJBgNVBAYTAlVTMRMwMIICCDAaBgkqhkiG9w0BBQMwDQQIIfYyAEFKaEECAQUEggHozdmgGz7zbC1mcJ2rcNAQEEBQAwgY8xCzAJBgNVBAYTAlVTMR

----END CERTIFICATE----
```

## 참고문헌

* [공개 키, 개인 키 및 인증서](https://docs.oracle.com/cd/E19509-01/820-3503/ggbgc/index.html)

