
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS 파일 - APK 세트 아카이브",
  "description":"APKS 파일이란 무엇입니까?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## .APKS 파일이란?

확장자가 .apks인 파일은 Android 패키지 **APK** 파일의 모음인 아카이브 파일입니다. APKS 파일의 각 개별 APK 파일은 기기의 다양한 측면을 고려하여 생성됩니다. 여기에는 아키텍처, 언어, 화면 밀도 및 기타 장치 기능이 포함됩니다. APKS 파일은 **bundletool**에 의해 생성됩니다. Android App Bundle을 빌드하고 장치에 배포하기 위해 App Bundle을 다른 APK로 변환하는 데 사용됩니다.

## APKS 파일 형식 - 추가 정보

APKS 파일은 [ZIP](/ko/compression/zip/) 파일 형식을 사용하여 압축 파일로 저장됩니다.

## APKS 파일을 생성하는 방법은 무엇입니까?

Android App Bundle(AAB)이 준비되면 Google Play 스토어에서의 동작을 테스트하여 기기에 배포할 수 있습니다. 이를 위해 AAB 파일에서 APKS 파일을 생성하고 Google의 Android [bundletool](https://developer.android.com/studio/command-line/bundletool)을 사용하여 테스트 장치에 설치할 수 있습니다. 다음 명령을 사용하여 APK에서 APKS 아카이브 파일을 생성하는 명령줄 도구를 제공합니다.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

APK를 장치에 배포하기 위해 다음과 같이 장치 서명 정보로 APKS 파일에 서명할 수 있습니다.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## 참고문헌

* [번들툴 - 커맨드라인](https://developer.android.com/studio/command-line/bundletool)

