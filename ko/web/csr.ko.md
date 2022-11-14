{
  "date" : "2022-09-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSR 파일 - 인증서 서명 요청 파일 형식",
  "description" :"CSR 파일이 무엇이며 CSR 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CSR",
  "menu" : {
    "docs" : {
      "identifier":"web-csr",
      "parent" : "web"
}
},
  "lastmod" : "2022-09-04"
}

## .CSR 파일이란?

CSR 파일은 SSL/TLS 인증서를 요청하는 데 사용되는 **인증서 서명 요청** 파일입니다. SSL/TLS 인증서가 필요한 경우 최종적으로 설치될 동일한 서버에서 CSR을 생성합니다. 이 CSR 파일은 인증서 생성을 위해 인증 기관(CA)과 공유됩니다. 여기에는 일반 이름, 조직, 국가 및 더 중요한 것은 인증서 파일에 통합되고 해당 개인 키로 서명된 **공개 키**와 같은 정보가 포함됩니다.

**CSR 파일을 열 수 있는** 응용 프로그램에는 OpenSSL 및 Microsoft IIS가 포함됩니다.

## 인증서 서명 요청 파일 형식

CSR 파일은 Microsoft 메모장과 같은 간단한 텍스트 편집기에서 열고 볼 수 있는 Base-64 PEM 형식으로 생성됩니다. 여기에는 헤더 **-----BEGIN NEW CERTIFICATE REQUEST-----**가 파일 시작 부분에 포함되고 바닥글이 **-----END NEW CERTIFICATE REQUEST-----** 위치에 포함됩니다. 파일의 끝.

### CSR 파일은 어떻게 생겼나요?

CSR 파일의 간단한 예는 다음과 같습니다.

```
-----BEGIN NEW CERTIFICATE REQUEST-----
MIIuasd098f9567a0sd657f80a9sd8f09asdf80asd8f0asdDVDCCAr0CAQAweTEeMBwGA1UEAxMVd3d3L
mpvc2VwaGNoYXBtYW4uY29tMQ8wDQYDVQQLEwZEZXNpZ24xFjAUBgNVBAoTDUpvc2VwaENoYXBt567W4xE
jAQ657BgNVBAcTCU1haWRzdG9uZTENMAsGA1UECBMES2VudDELMAkGA1UEBhMCR0IwgZ8wDQYJKoZIhvcN
AQEBBQADgY0AMIGJAoGBAOEFDpnOKRabQhDa5asDxYPnG0cneW18e8apjOk1yuGRk+3GD7YQvuhBVS1x6w
kw1D267RnmnZgN1nNUK0cRK7sIvOyCh1+jgD7asdfasdfdsu46mLk81j+b4YSEmYZGPLIuclyocPDm0hXa
yjCUqWt7z6LMIKpLym8gayEZzz679Gn97PsbafasdfPkVFBAgMBAAGgggGZMBoGCisGAQQBgjcNAgMxDBY
KNS4xLjI2MDAuMjB7Bgo45457567658rBgEEAYI3AgEOMW0wazAOBgNVHQ452358BAf8EBAMsdfCBPAwRA
YJKoZIhvcNAQkPBDcwNTAOBggqhkiG9w234320DAgICAIAwDgYIKoZIhvcNAwQCAgCAMAcGBSsOAwIHMAo
GCCqGSIb3DQMHMBMGA1UdJQQMMAoGCCsGAQUsdfsdfFBwMB657M567IH9BgorBgEEAYI3DQICMYHu567MI
HrAgEBH567l567oAsdfsdTQBpAGMAcgBvAadsfadsHMAbwBmAHQAIABSAFMAQQAgAFMAQwBoAGEAbgBuAG
UAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIAb567wB2AGkAZABlAHIDg56YkAk0kfHSk
r48685jsEVya3mgfUoyaYMO456ECNZr4Cb+WhPgexfjOO5qwOG1oDOTa567rkc5pG+IPBQnq+4cotT8hWJ
Qwpc+qGb578xUETpxCok756768567567hrhN5079vFXq5dsHkmtOTwkSqSnz9yruVoxYeDQ8jI3KG3HTgx
wFto8oZnm+E+Y4oshUAAAAAAAAAADANB56756gkqhkiG9w0BAQUFAAOBgQAuAxetLz75667gfjBdWpjpix
e657VYZXuPZ+6jvZNL9hOw7Fk5pVVXWdr8csJ6JUW8QdH9KB6ZlM4yg8Df+vat1G6GuD2hiIR7fQ0NtP==
-----END NEW CERTIFICATE REQUEST-----
```

## CSR에는 어떤 정보가 포함됩니까?

CSR 파일에는 다음 정보가 포함됩니다.

1. '비즈니스 및 웹사이트에 대한 정보' - 일반 이름, 조직, 조직 단위, 도시/지역, 주/군/지역(S), 국가 및 이메일 주소와 같은 정보를 포함합니다.
1. '공개 키' - 인증서에 포함되어 전송된 데이터를 암호화하는 데 사용되며 해당 개인 키로 복호화됩니다.
1. '키 유형 및 길이에 대한 정보' - 일반적으로 RSA 2048이지만 RSA 4096+와 같이 더 큰 크기로 제공될 수도 있습니다.

## 참고문헌

* [컨셉 애플리케이션 서버](https://github.com/Devronium/ConceptApplicationServer)

