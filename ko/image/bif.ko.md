{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BIF 파일 - Ventana 전체 슬라이드 이미지 형식",
  "description":"BIF 파일을 만들고 열 수 있는 BIF 파일 형식 및 API에 대해 알아보십시오.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## .BIF 파일이란?

BIF 파일은 슬라이드 표본 이미지가 포함된 래스터 이미지 파일입니다. 슬라이드 보기 응용 프로그램에 의해 단일 합성 이미지로 결합되는 여러 TIFF 이미지로 구성됩니다. BIF 파일은 Ventana Medical 시스템 디지털 슬라이드 스캐너로 생성되며 [TIFF](/ko/image/tiff/) v 6.0 정의의 BigTIFF 변형과 완전히 호환됩니다.

## BIF 파일 형식

BIF 파일은 바이너리 이미지 파일로 저장되며 최대 200,000 x 200,000 픽셀로 구성됩니다. 이로 인해 파일 크기가 커져 TIF 표준에서 정의한 32비트 파일 포인터에 의해 부과된 4GB 크기 제한이 깨질 수 있습니다. 그러나 64비트 파일 포인터를 사용하면 이 파일 크기 장벽이 TIFF 표준의 BigTIFF 변형으로 극복됩니다.

### 누가 BIF 파일을 사용합니까?

BIF 파일은 디지털 슬라이드 스캐너에서 슬라이드 표본의 디지털 사본을 스캔하고 생성하는 데 사용됩니다. 병리학자인 경우 슬라이드 보기 응용 프로그램에서 이러한 BIF 파일을 열 수 있습니다. 높은 수준의 세부 정보와 고해상도 데이터를 사용하여 슬라이드 이미지를 확대 및 축소하여 표본 섹션을 다소 자세하게 볼 수 있습니다. 이러한 파일에 있는 [XML](/ko/web/xml/) 메타데이터 파일은 이미지를 결합하는 방법과 파일의 썸네일로 사용할 이미지를 정의합니다.

## BIF 파일을 여는 방법?

다음을 사용하여 BIF 파일을 열 수 있습니다.

* OpenSlide(크로스 플랫폼)
* ImageJ(크로스 플랫폼)
* NetScope 뷰어(Windows)

## 참조 ##

* [로슈 디지털 병리 BIF 백서](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

