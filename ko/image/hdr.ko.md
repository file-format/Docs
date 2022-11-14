{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR 파일 형식 - HDR 이미지 파일이란 무엇입니까?",
  "description":"HDR 파일을 만들고 열 수 있는 HDR 파일 형식 및 API에 대해 알아보세요.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## HDR 파일이란?

HDR 파일은 디지털 카메라 사진을 저장하기 위한 HDR(High Dynamic Range) 래스터 이미지 파일 형식입니다. 이를 통해 사진 편집자는 동적 범위가 제한된 디지털 이미지의 색상과 밝기를 향상시킬 수 있습니다. 이렇게 수정하면 모서리 주변의 밝기가 향상되어 자연에 가까운 이미지를 얻을 수 있습니다. HDR 파일은 일반적으로 32비트 래스터 이미지로 저장됩니다. Adobe Photoshop은 HDR 파일을 만들고 열 수 있습니다.

HDR 파일은 HDRI라고도 합니다.

## HDR 파일 형식 - 추가 정보

HDR 파일 형식은 원본 Radiance Picture(.pic) 파일 형식을 기반으로 합니다. HDR 파일의 픽셀 데이터는 일반적으로 압축되지 않은 상태로 저장되지만 경우에 따라 간단한 실행 길이 인코딩 시스템을 사용하여 압축됩니다.

### HDR 파일 구조

HDR 이미지 파일은 다음 세 섹션으로 구성됩니다.

* **헤더:** HDR 파일은 이미지 파일의 첫 번째 바이트(예: "#?RADIANCE")로 식별됩니다.
* **Resolution String:** 헤더 다음에는 4개의 값으로 구성된 단일 해상도 라인이 옵니다. X 및 Y 레이블 각각 뒤에 숫자 정수 값이 옵니다. X와 Y의 순서는 회전을 나타냅니다. 양수 및 음수 값이 있는 X 및 Y 조합은 가능한 모든 이미지 방향 및 회전을 포함합니다.
* **픽셀 데이터:** HDR 파일의 픽셀 데이터는 압축되지 않거나 표준 실행 길이 인코딩을 사용하여 압축됩니다.

## 오픈 소스 HDR/HDRI API

* **[imageinfo](https://github.com/xiaozhuai/imageinfo )** - 크로스 플랫폼 초고속 단일 헤더 [C++](/ko/programming/cpp/) 라이브러리를 사용하여 로드/디코딩 없이 이미지 크기와 형식을 얻습니다.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** - 로드/디코딩 없이 이미지 크기와 형식을 가져오는 Rust 라이브러리. [.avif](/ko/image/avif/), [.bmp](/ko/image/bmp), [.cur](/ko/image/cur/), [.dds](/ko/image/dds/), [.avif]를 지원합니다. gif](/ko/image/gif/), hdr(그림), [heic(heif)](/ko/image/heic/), [.icns](/ko/image/icns/), [.ico](/ko/image/ico /), [.jp2](/ko/image/jp2/), [jpeg(jpg)](/ko/image/jpeg/), [jpx](/ko/image/jpx/), ktx, [png](/ko/image/png /), [psd](/ko/image/psd/), qoi, tga, tiff(tif) 및 webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** - HdrHistogram의 Java 구현입니다.

## 참고문헌

* [래디언스 HDR](http://paulbourke.net/dataformats/pic/)
* [이미지 정보](https://github.com/xiaozhuai/imageinfo )

