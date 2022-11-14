{
  "date" : "2019-10-11",
  "keywords" :[ "mng 파일", "mng 파일 형식", "mng 파일이란", "파일", "mng 예제", "mng 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MNG 파일 형식 - 다중 이미지 네트워크 그래픽 파일 형식",
  "description":"MNG 파일 형식과 MNG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .MNG 파일이란?

확장자가 .mng인 파일은 [PNG](/ko/image/png/) 이미지 형식과 유사하지만 애니메이션 이미지를 지원하는 다중 이미지 네트워크 그래픽 파일 형식입니다. 애니메이션의 추가 기능으로 PNG 형식의 과부하를 방지하기 위해 개발되었습니다. MNG도 [GIF](/ko/image/gif/) 파일과 유사하지만 더 많은 압축을 사용하고 전체 알파 기능을 지원합니다. MNG 파일의 비공식 MIME 미디어 유형은 video/x-mng입니다. MNG 파일은 ImageMagik 및 IrfanView와 같은 응용 프로그램에서 열 수 있습니다.

## MNG 파일 형식

MNG 파일 형식은 PNG의 형식과 유사하며 PNG 사양에 정의된 것과 동일한 청크 구조를 사용합니다. MNG 디코더는 명령어 디코딩을 위한 특별한 플래그를 지정하지 않고 PNG 데이터스트림을 디코딩할 수 있어야 합니다. MNG는 여러 이미지를 "프레임"으로 그룹화하며 일부 이미지는 한 위치에서 다른 위치로 이동하기 위한 스프라이트로 사용됩니다. 이 메커니즘을 통해 이미지 데이터를 재전송하지 않고 재사용할 수 있습니다. 개발자 참고용으로 [MNG 사양](http://www.libpng.org/pub/mng/spec/)을 참조할 수 있습니다.

### MNG 서명

MNG 데이터 스트림은 다음을 포함하는 8바이트 서명으로 시작합니다.

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

이것은 PNG 서명과 유사하지만 PNG 대신 MNG를 포함합니다.

### MNG 프레임

MNG 프레임은 더 작은 이미지의 2차원 이미지로 구성됩니다. 각 작은 이미지는 행 및 열 인덱스 조합을 사용하여 액세스할 수 있습니다. 이 형식은 일련의 2차원 평면으로 배열된 3차원 "복셀" 데이터를 저장할 수 있습니다. 각 평면은 PNG 또는 Delta-PNG 데이터스트림으로 표시됩니다. 각 Delta-PNG 데이터스트림은 이미지를 상위 PNG 이미지와의 차이점으로 정의합니다. 이것은 각각에 대해 완전한 PNG 데이터 스트림을 사용하는 것보다 후속 이미지를 나타내는 훨씬 더 간결한 방법을 제공합니다.

## 참조 ##

* [MNG](http://www.libpng.org/pub/mng/)
* [MNG 형식 v 1.0](http://www.libpng.org/pub/mng/spec/)

