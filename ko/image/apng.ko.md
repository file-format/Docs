{
  "date" : "2019-10-11",
  "keywords" :[ "apng 파일", "apng 파일 형식", "apng 파일이란", "파일", "apng 예제", "apng 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APNG 파일 형식 - 애니메이션 휴대용 네트워크 그래픽 파일",
  "description":"APNG 파일 형식과 APNG 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## .APNG 파일이란?

.apng(Animated Portable Network Graphics) 확장자를 가진 파일은 래스터 그래픽 형식이며 Portable Network Graphic([PNG](/ko/image/png/) )의 비공식 확장자입니다. 애니메이션 시퀀스를 나타내는 여러 프레임(각각 PNG 이미지)으로 구성됩니다. 이는 [GIF](/ko/image/gif/) 파일과 유사한 시각화를 제공합니다. APNG 파일은 24비트 이미지와 8비트 투명도를 지원합니다. APNG는 애니메이션이 아닌 GIF 파일과 역호환됩니다. APNG 파일은 동일한 .png 확장자를 사용하며 Mozilla Firefox, APNG 지원 Chrome, iOS 10용 iMessage 앱과 같은 응용 프로그램에서 열 수 있습니다.

## 약력

* APNG 사양은 애니메이션 PNG 이미지를 지원하기 위해 2004년에 만들어졌습니다.
* APNG 디코더는 훨씬 작은 크기로 개발되었으며 PNG 디코더의 뒷면을 사용합니다.
* 지속적인 고민 끝에 .apng 대신 .png로 확장자를 유지하면서 새로운 MIME 형식의 image/apng를 공식화
* APNG는 2007년 4월 20일 PNG 이미지에 대한 획일성과 동시에 사양이 다르기 때문에 PNG 그룹에 의해 공식적으로 거부되었습니다.

## APNG 파일 형식

APNG 파일은 디스크에 바이너리 파일로 저장되며 애니메이션 이미지에는 PNG의 확장 사양을 사용합니다. APNG 파일의 첫 번째 프레임은 표시를 위해 PNG 디코더에서 읽을 수 있는 일반 PNG 스트림입니다. APNG 파일 형식은 PNG 사양을 따르며 데이터는 청크라는 세그먼트에 저장됩니다. 그러나 APNG는 다음과 같은 새로운 청크를 도입했습니다.

'애니메이션 컨트롤 청크(acTL)' - 이 파일이 일반 PNG 파일이 아닌 애니메이션 PNG 파일임을 나타냅니다. 마커 역할을 하며 IDAT 청크 앞에 옵니다. 또한 프레임 수와 애니메이션을 반복하는 시간에 대한 정보도 포함합니다.

'Frame Control Chunk' - 각 시작 시 발생하며, 치수, 위치, 투명도 적용, 종료 후 이전 또는 다음 프레임으로 대체 정보 등의 메타데이터 정보가 발생합니다.

`Frame Data Chunk` - 프레임의 내용을 저장하고 시퀀스 번호로 시작합니다. 이 시퀀스 번호는 기본 이미지의 IDAT 청크와 구조가 동일합니다.

{{< figure src="../APNG.png" alt="애니메이션 PNG - APNG 파일 형식" >}}

APNG는 PNG 파일을 읽는 애플리케이션이 이해하지 못하는 청크를 단순히 무시하도록 설계되었기 때문에 측면 사양이 PNG와 역호환됩니다. 비트 심도, 색상 유형, 압축, 필터, 인터레이스 방식 및 팔레트 정보에 대한 사양은 기본 PNG 형식과 동일하게 사용됩니다.

## APNG 대 GIF

GIF가 이미 존재하고 오랜 기간 동안 사용되기 때문에 APNG가 GIF와 어떻게 다른지 궁금할 것입니다. 다음은 두 파일 형식에 대한 간략한 아이디어를 제공하는 APNG와 GIF 간의 비교 세트입니다.

||APNG|GIF|
---|---|---|
|출판|2004|1987|
|색상 깊이|24비트|8비트|
|프레임 속도|무제한|초당 10프레임|
|투명성|완전 및 부분|완전|
|압축|매우 좋음|좋음|

## 참고문헌

* [APNG 파일 형식](https://en.wikipedia.org/wiki/APNG)
* [공식 PNG 형식 사양](https://www.w3.org/TR/PNG/)

