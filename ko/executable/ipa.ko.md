{
  "date" : "2021-08-30",
  "keywords" :[ "ipa 파일", "ipa 파일 형식", "ipa 파일이란", "파일", "ipa 예제", "ipa 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"IPA 파일 형식과 IPA 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"IPA - iOS 애플리케이션 패키지 파일",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## .IPA 파일이란?
확장자가 .ipa인 파일은 iOS에 속하며 애플리케이션 패키지 파일이라고 합니다. iOS 애플리케이션을 저장하는 아카이브([ZIP](/ko/compression/zip/) 압축을 사용하여 압축) 파일이지만 해당 애플리케이션은 iOS 또는 iPad, iPhone 또는 아이팟 터치. 주로 iTunes, Apple Configurator 2 또는 타사 소프트웨어를 사용하여 IPA 파일을 설치할 수 있습니다.

## IPA 파일 형식
Apple Xcode를 사용하여 앱을 개발하는 IOS 개발자는 앱 스토어 배포 목적을 테스트하기 위해 개발한 앱을 IPA 파일로 패키징해야 하기 때문에 IPA 파일에 익숙합니다. IPA 파일은 iOS 앱으로 설치된 것으로 알려져 있지만 압축을 풀어 포함된 앱 데이터를 볼 수도 있습니다. IPA 파일은 휴대폰의 ARM 아키텍처용 바이너리를 하나만 포함하고 x86 아키텍처용 바이너리를 포함하지 않기 때문에 많은 .ipa 파일을 iPhone 시뮬레이터에 설치할 수 없습니다.
### .ipa 파일의 구조
다음 예는 IPA의 구조를 보여줍니다.

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
위의 내용은 iTunes와 App Store가 인식할 수 있도록 내장된 구조입니다. 이 구조에 따라:
- Payload 디렉토리에는 모든 앱 데이터가 포함됩니다.
- iTunes Artwork 파일은 512×512 픽셀 PNG 이미지로, iTunes 및 iPad의 App Store 앱에 표시하기 위한 앱 아이콘이 포함되어 있습니다.
- iTunesMetadata.plist에는 개발자 이름 및 ID, 저작권 정보, 번들 식별자, 앱 이름, 장르, 출시 날짜, 구매 날짜 등 다양한 정보가 포함되어 있습니다.
- META-INF 폴더에는 IPA를 생성하는 데 사용된 프로그램에 대한 메타데이터만 포함됩니다.


## 참고문헌

* [.ipa - 위키피디아 제공](https://en.wikipedia.org/wiki/.ipa)


