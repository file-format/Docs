{
  "date" : "2021-02-25",
  "keywords" :[ "bdf 파일", "bdf 파일 형식", "bdf 파일이란", "파일", "bdf 예제", "bdf 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BDF - 글리프 비트맵 배포 형식",
  "description":"BDF 파일 형식과 BDF 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "BDF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2021-02-25"
}

## .BDF 파일이란?
BDF 파일은 사람이 읽을 수 있는 형식이며 일반적으로 ASCII 인코딩으로 배포됩니다. 파일은 전체 글꼴과 관련된 전역 정보로 시작하여 개별 글리프에 대한 정보와 비트맵이 이어집니다. 그 안의 데이터는 단일 크기 방향의 글꼴에 대해 표시됩니다. 둘 이상의 방향에서 사용하는 메트릭은 단일 파일에 포함될 수 있습니다. BDF 파일에서 각 항목은 파일의 별도 텍스트 행에 포함됩니다. 공백은 줄에서 항목을 구분하는 데 사용됩니다.

## BDF 파일 형식
Glyph Bitmap Distribution Format의 BDF short; Adobe에서 소유한 비트맵 형식의 글꼴을 저장하기 위한 파일 형식입니다. 콘텐츠는 사람이 읽을 수 있을 뿐만 아니라 컴퓨터에서도 읽을 수 있는 텍스트 파일 형식을 취합니다. BDF는 특히 Unix X Window 환경에서 사용됩니다. 보다 효율적인 PCF 글꼴 형식과 OpenType 및 TrueType 글꼴로 널리 대체되었습니다.
### BDF 파일 구조
BDF 글꼴 파일은 세 섹션으로 구성됩니다.

- 글꼴의 모든 글리프에 적용되는 전역 섹션.
- 각 글리프에 대해 별도의 항목이 있는 섹션.
- ENDFONT 문.

## 예시
다음은 ASCII 대문자 'A'에 대해 하나의 상형 문자가 포함된 글꼴의 예입니다. 전역 선언은 "STARTFONT" 줄로 시작하고 "CHARS" 줄로 끝납니다.
```
STARTFONT 2.1
FONT -gnu-unifont-medium-r-normal--16-160-75-75-c-80-iso10646-1
SIZE 16 75 75
FONTBOUNDINGBOX 16 16 0 -2
STARTPROPERTIES 2
FONT_ASCENT 14
FONT_DESCENT 2
ENDPROPERTIES
CHARS 1
STARTCHAR U+0041
ENCODING 65
SWIDTH 500 0
DWIDTH 8 0
BBX 8 16 0 -2
BITMAP
00
00
00
00
18
24
24
42
42
7E
42
42
42
42
00
00
ENDCHAR
ENDFONT
```



## 참고문헌
* [글리프 비트맵 배포 형식](https://en.wikipedia.org/wiki/Glyph_Bitmap_Distribution_Format)
* [글리프 비트맵 배포 형식(BDF) 사양](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5005.BDF_Spec.pdf)

