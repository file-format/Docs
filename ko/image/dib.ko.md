{
  "date" : "2020-01-10",
  "keywords" :[ "dib 파일", "dib 파일 형식", "dib 파일이란", "파일", "dib 예제", "dib 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"DIB 파일을 만들고 열 수 있는 DIB 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## .DIB 파일이란?

DIB(장치 독립 비트맵)는 표준 비트맵 파일([BMP]()/image/bmp/))과 구조가 유사한 래스터 이미지 파일입니다. 여기에는 RGB 색상을 픽셀 값에 매핑하는 방법을 설명하는 색상 테이블이 포함되어 있습니다. 이를 통해 DIB는 모든 장치에서 이미지를 나타낼 수 있습니다. Windows 및 macOS에서 표준 BMP 파일을 열 수 있는 거의 모든 응용 프로그램에서 열 수 있습니다. DIB는 이진 파일이며 BMP와 유사한 복잡한 파일 형식을 갖습니다. DIB 이미지는 색상 깊이 및 인치당 픽셀 측면에서 렌더링 장치의 출력 기능과 무관합니다.

## DIB 파일 형식 사양 ##
DIB에는 다음 색상 및 치수 정보가 포함됩니다.

* 직사각형 이미지가 생성된 장치의 색상 형식입니다.
* 직사각형 이미지가 생성된 장치의 해상도입니다.
* 이미지가 생성된 장치의 팔레트입니다.
* 빨강, 초록, 파랑(RGB) 삼중항을 직사각형 이미지의 픽셀에 매핑하는 비트 배열입니다.
* 비트 배열의 크기를 줄이는 데 사용되는 데이터 압축 체계(있는 경우)를 나타내는 데이터 압축 식별자입니다.

### DIB 데이터 블록 형식 ###

DIB는 디스크에 저장된 .DIB 파일과 비교하여 메모리 블록의 컨텍스트에서 제공됩니다. 메모리 블록은 DIB에 대한 Windows API 사양에 따른 구조로 구성됩니다. 실제 DIB는 다음으로 구성됩니다.
* 헤더
* 색상 팔레트
* 픽셀 데이터

실제로 팔레트, 헤더 및 이미지 데이터 작업은 마치 세 개의 개별 메모리 블록인 것처럼 수행됩니다. 이 공통 메모리 블록에 대한 핸들은 GlobalAlloc을 사용하여 할당되며 헤더, 색상 테이블 및 픽셀 데이터를 추출하고 작업하는 데 사용되는 HDIB로 알려져 있습니다.

### 구조 ###
DIB에 포함된 정보는 다양한 구조로 표현됩니다. 여기에는 다음이 포함됩니다.

BITMAPInfo - DIB의 치수 및 색상 정보를 정의합니다.
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
BITMAPINFOHEADER로 구성됩니다.

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
두 개 이상의 RGBQAD 구조가 뒤따릅니다.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### 데이터 비트 ###
|비트|설명|
---|---|
|1비트 형식(흑백)|흑백 비트맵은 두 가지 색상(흑백)으로 구성됩니다. 이 제한된 색상 수로 인해 이러한 비트맵은 디스크 공간을 덜 차지합니다. bitBitCount는 두 색상의 표현에 대해 true 또는 false를 반환합니다. 대부분의 응용 프로그램은 bitBitCount==1인 경우 팔레트를 완전히 건너뜁니다.
|4비트 형식(VGA 또는 16색)|이미지 데이터의 각 바이트는 2픽셀을 나타내며 bitBitCount==4입니다. 이 비트는 픽셀의 색상을 내림차순으로 나타냅니다.
|8비트 형식(256색)|이 8비트 형식은 최대 256색을 나타낼 수 있습니다. 이미지의 비트맵 데이터 배열에 있는 각 바이트는 단일 픽셀을 나타냅니다. 해당 바이트의 값은 bmciColors로 표시되는 256개 항목에서 사용할 색상 팔레트 항목의 번호입니다.
|24비트 형식(TrueColor)|이 비트맵은 최대 2^24개의 색상을 가질 수 있습니다(biBitCount == 24). 비트맵 데이터 배열의 각 3바이트 시퀀스는 픽셀의 세 가지 기본 색조의 상대적 강도를 나타냅니다. 색상은 0에서 255 사이의 값으로 설명되며 Blue, Green, Red의 순서로 3바이트에 저장됩니다. Windows에서 색상에 대한 대부분의 참조는 반대 순서인 빨강/녹색/파랑을 사용하기 때문에 이것은 중요한 구별입니다. 따라서 "RGB" 대신 TrueColor 이미지로 작업할 때 "BGR"을 생각하십시오. Windows용 그리기 프로세스를 가속화하기 위해 색상 팔레트를 지정할 수 있습니다. 이 경우 biClrUsed는 0이 아닙니다. 그러나 보시다시피 픽셀 데이터 자체에 색상 정보가 포함되어 있으므로 필요하지 않습니다.
|32비트 형식|32비트 이미지에는 최대 2^24개의 색상이 있습니다(biBitCount == 24).

## 참조 ##
* [장치 독립 비트맵 - Microsoft 제공](https://learn.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

