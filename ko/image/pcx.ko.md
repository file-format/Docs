{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCX 파일 형식 - 그림판 비트맵 이미지 파일",
  "description":"PCX 파일을 만들고 열 수 있는 API와 PCX 파일 형식에 대해 알아보세요.",
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-03-16"
}

## .PCX 파일이란?

PCX 파일인 Picture Exchange 파일은 PC Paintbrush 응용 프로그램의 기본 파일 형식으로 사용된 래스터 이미지 파일 형식입니다. 미국 ZSoft Corporation에서 DOS 및 Windows 플랫폼용으로 개발했으며 [BMP](/ko/image/bmp/), [JPEG](/ko/image/jpeg/) 및 [ PNG](/ko/image/png/) 파일 형식. PCX 파일은 RLE 인코딩을 사용하여 압축되므로 크기가 더 작습니다. 주로 디지털 팩스 파일을 생성하는 데 사용되는 다중 페이지 [DCX](/ko/image/dcx/) 파일에서 사용됩니다.

## PCX 파일 형식

PCX 파일은 바이너리 파일 형식으로 디스크에 저장됩니다. 내부 파일 형식 구조는 리틀 엔디안 바이트 순서를 따르며 다음 세 섹션으로 구성됩니다.

**`PCX 헤더`** - PCX 헤더의 길이는 128바이트입니다. 여기에는 식별자, 버전 번호, 이미지 크기, 16개의 팔레트 색상, 숫자 색상 평면 및 각 평면의 비트 심도, 압축 방법 값이 포함됩니다.

PCX 헤더는 그래픽 파일 형식 백과사전(2nd ed.)을 참조하여 아래와 같습니다.
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

**`이미지 데이터`** - 헤더 바로 뒤에 PCX 이미지 데이터가 옵니다. 헤더의 필드 설정에 따라 이미지 데이터가 압축될 수 있습니다. PCX 파일의 데이터 저장은 지정된 색상 평면의 수에 따라 다릅니다. 이미지 데이터는 행으로 구성됩니다. 플레인이 여러 개일 경우, 플레인 단위로 로우 내에서 레드, 그린, 블루 데이터의 순차 배열로 저장됩니다. 이 패턴은 평면의 각 선에 대해 반복됩니다.

## 참고문헌

* [PCX - 위키피디아 작성](https://en.wikipedia.org/wiki/PCX)

