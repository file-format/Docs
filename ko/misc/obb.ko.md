{
  "date" : "2022-02-16",
  "keywords" :[ "obb 파일", "obb 파일 형식", "obb 파일이란", "파일", "obb 예제", "obb 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBB 파일 형식 - Android 불투명 바이너리 Blob 파일",
  "description":"OBB 파일 형식과 OBB 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## .OBB 파일이란?

OBB 파일은 Android [APK](/ko/compression/apk/) 파일 외에 추가 데이터가 포함된 확장 파일입니다. Google Play 스토어는 크기가 100MB를 초과하는 Android APK 파일을 허용하지 않습니다. 그러나 일부 응용 프로그램은 APK 파일 외에도 고화질 그래픽, 미디어 파일 또는 기타 대형 자산을 호스팅해야 할 수 있습니다. 이것이 OBB 파일 유형이 들어오는 곳입니다. Google Play에서는 이러한 확장 파일을 APK 파일에 대한 보충 파일로 첨부할 수 있습니다.

## OBB 파일 형식

OBB 파일은 APK 파일과 함께 바이너리 파일로 저장됩니다. APK가 OBB 파일과 함께 제공되는 경우 Google Play는 서버에서 확장 파일을 호스팅하며 개발자에게 추가 비용이 청구되지 않습니다. 이러한 추가 파일은 설치를 위해 앱을 다운로드할 때 SD 카드 또는 USB 장착 가능 파티션에 장치의 공유 저장소에 저장됩니다.

OBB 파일은 다운로드 시 다운로드되어 설치됩니다. 그러나 어떤 경우에는 응용 프로그램을 처음 실행할 때 설치를 위해 다운로드됩니다.

### OBB 최대 파일 크기

Google Play 스토어에서는 최대 2GB 크기의 OBB 확장 파일을 업로드할 수 있습니다. 대용량 파일은 압축된 [ZIP](/ko/compression/zip/) 파일로 업로드하여 인터넷을 통한 효율적인 업로드를 권장합니다.

이러한 확장 파일은 앱에 필요한 추가 리소스를 위한 **main** 기본 확장 파일 또는 기본 확장 파일에 대한 소규모 업데이트를 위한 선택적 패치 확장 파일로 호스팅될 수 있습니다.

## 참고문헌

* [안드로이드 개발자 - 확장 파일](https://developer.android.com/google/play/expansion-files)

