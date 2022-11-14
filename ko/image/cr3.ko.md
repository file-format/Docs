{
  "date" : "2022-03-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CR3 파일 형식 - Canon Raw 3 이미지 파일",
  "description":"CR3 파일 형식과 CR3 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "CR3",
  "menu" : {
    "docs" : {
      "identifier":"image-cr3",
      "parent" : "image"
}
},
  "lastmod" : "2022-03-26"
}

## .CR3 파일이란?

CR3 파일은 선택한 Canon 디지털 카메라로 만든 Canon RAW 이미지 파일 형식입니다. Canon에서 CR2 파일 형식을 대체하기 위해 도입했으며 일부 Canon 디지털 장치에서 사용됩니다. CR3 파일은 카메라에서 캡처한 처리되지 않은 원본 무손실 이미지 데이터를 저장합니다. 이러한 원시 이미지를 사용하면 고품질 이미지를 제공하고 사진 작가가 편집할 수 있는 충분한 공간을 확보할 수 있습니다. 기본 이미지 데이터 외에도 CR3 파일은 이미지에 대한 메타데이터 정보도 저장합니다.

## CR3 파일 형식

CR3 파일은 ISO 기본 미디어 파일 형식(ISO/IEC 14496-12)의 바이너리 파일로 디스크에 저장되며 사용자 정의 [Canon 태그](https://exiftool.org/TagNames/Canon.html#uuid)도 포함됩니다. 또한 JPEG-LS(Rice-Golomb + RLE)가 혼합된 [Canon 'crx' 코덱](https://github.com/LibRaw/LibRaw/blob/master/src/decoders/crx.cpp)도 포함되어 있습니다. 코딩) 및 JPEG-2000(LeGall 5/3 DWT + 정량화).

## CR3 사용자 정의 태그

CR3 파일에는 다양한 목적을 위한 사용자 정의 태그가 포함되어 있습니다. 이러한 태그 중 일부는 다음과 같습니다.

|태그 ID| 태그 이름| 쓰기 가능 |값/메모|
---|---|---|---|
|'CCTP' |캐논CCTP| - |--> Canon CCTP 태그|
|'CMT1' |IFD0| - |--> EXIF 태그|
|'CMT2' |ExifIFD| - |--> EXIF 태그|
|'CMT3' |메이커노트캐논| - |--> 캐논 태그|
|'CMT4' |GPS 정보| - |--> GPS 태그|
|'CNCV' |압축기 버전| 아니| |
|'CNOP' |캐논CNOP| - |--> Canon CNOP 태그|
|'CNTH' |캐논CNTH| - |--> Canon CNTH 태그|
|'THMB' |썸네일 이미지| 아니| |

## 참고문헌

* [CR2 파일 형식](http://lclevy.free.fr/cr2/)
* [캐논 태그](https://exiftool.org/TagNames/Canon.html#uuid)

