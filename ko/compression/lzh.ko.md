{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "압축", "파일", "확장자", "파일 형식", "Lempel-Ziv", "하루야스", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZH 파일 형식",
  "description":"LZH 파일을 만들고 열 수 있는 LZH 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## .LZH 파일이란? ##

확장자가 .lzh 및 .lha인 파일은 일반적으로 아카이브 압축 파일 형식과 관련이 있습니다. 이 파일 형식은 [ZIP](/ko/compression/zip/), [RAR](/ko/compression/rar/) 등과 같은 다른 파일 압축 형식과 동일합니다. 이러한 파일 형식의 주요 목적은 파일의 크기를 줄이는 것입니다. 쉽게 보낼 수 있을 뿐만 아니라 압축된 형태로 함께 보관할 수 있는 형식입니다. AS는 다른 서양 회사와 비교하여 LZH 파일은 일본에서 매우 인기가 있으며 일반적으로 비디오 게임 데이터를 압축하는 데 사용됩니다. Windows 7용 LZH 추가 기능은 Windows 7 일본어 버전에 내장되어 있습니다. Microsoft는 Windows XP 일본어 버전용 Microsoft 압축(LZH) 폴더 추가 기능을 처음 출시했습니다. 이 파일 형식은 Lempel-Ziv 및 Haruyasu 알고리즘에서 사용하는 압축 조항 및 기능으로 구현됩니다.

## LZH 사양 ##

LZH 아카이브의 압축 방법은 -lz1-과 같은 5바이트 텍스트 문자열로 표시됩니다. 압축 파일에서 세 번째에서 일곱 번째 바이트입니다.

|사양|설명|
---|---|
|확장 | .lzh, .lha|
|미디어 유형| 응용 프로그램/x-lzh-압축|
|유형 코드| "LHA_"(LHA-스페이스)|
|UTI| public.archive.lha|
|개발자| 요시자키 하루야스(요시)|
|유형| 압축|
|연장| 라크|

## LZH 파일을 여는 문제 ##

다음은 LZH 파일 형식이 제대로 작동하지 않을 수 있는 몇 가지 문제입니다.
  

* 파일이 손상되었을 수 있습니다. 이 문제를 해결하려면 파일을 다시 다운로드하거나 보낸 사람에게 파일을 다시 보내달라고 요청하세요.
* 두 번째 이유는 이 경우 파일이 감염되었기 때문입니다.
* LZH 파일에 대한 부적절한 링크
* LZH 설명 삭제
* 하드웨어 리소스가 충분하지 않음
* 장비의 오래된 드라이버

## 참조 ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))
