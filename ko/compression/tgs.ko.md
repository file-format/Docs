{
  "date" : "2019-10-11",
  "keywords" :[ "tgs 파일", "tgs 파일 형식", "tgs 파일이란", "파일", "tgs 예제", "tgs 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - 전보 애니메이션 스티커 파일 형식",
  "description":"TGS 파일 형식과 TGS 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## .TGS 파일이란?

확장자가 .tgs인 파일은 플랫폼 간 메시징 서비스 [Telegram](https://core.telegram.org/stickers#animated-stickers)에서 도입한 애니메이션 스티커 파일입니다. 애니메이션 스티커는 메시지 앱 사용자가 정지 이미지인 정적인 그래픽과 달리 메시지에서 더욱 강화되고 생생한 콘텐츠를 보내기 위해 사용됩니다. 텔레그램은 처음에 스틸 이미지 스티커에 [WEBP](/ko/image/webp/) 파일 형식을 사용했습니다. TGS 파일 형식은 정적 WEBP 스티커에 비해 더 높은 해상도와 더 작은 파일 크기로 애니메이션 데이터를 저장할 수 있습니다. TGS 파일은 Telegram, 7-zip, Apple Archive Utility 및 Corel WinZip과 같은 응용 프로그램을 사용하여 열 수 있습니다.

## TGS 파일 형식

Telegram은 2019년 7월에 Lottie 라이브러리를 기반으로 TGS 파일 형식을 도입했습니다. TGS 파일은 Adobe After Effects의 애니메이션에서 내보낸 [JSON](/ko/web/json/) 텍스트로 구성됩니다. 내보낸 JSON 텍스트는 파일 크기를 줄이는 gzip 압축을 사용하여 압축됩니다. 텍스트 파일에 대한 JSON 정보는 높은 압축률의 기반이 되는 텍스트 파일에 저장됩니다.

### TGS 스티커 사양

TGS 파일 형식은 TGS 애니메이션 스티커 생성에 특정 제한을 부과합니다. TGS 애니메이션 파일:

* 스티커/캔버스 크기는 512x512픽셀이어야 합니다.
* 스티커 개체는 캔버스를 벗어나면 안 됩니다.
* 애니메이션 길이는 3초를 초과할 수 없습니다.
* 모든 애니메이션은 반복되어야 합니다.
* 스티커 크기는 Bodymovin에서 렌더링 후 64KB를 초과할 수 없습니다.
* 모든 애니메이션은 초당 60프레임으로 실행되어야 합니다.

### 샘플 TGS JSON 텍스트

압축을 푼 샘플 애니메이션 스티커에는 다음 JSON 텍스트 콘텐츠가 포함되어 있습니다.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## 참조 ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - 위키백과](https://en.wikipedia.org/wiki/Gzip)

