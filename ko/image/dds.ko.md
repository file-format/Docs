{
  "date" : "2022-04-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DDS 파일 형식 - DirectDraw 표면 이미지 파일",
  "description":"DDS 파일을 만들고 열 수 있는 DDS 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "DDS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-04-02"
}

## .DDS 파일이란?

DDS 파일은 DDS(DirectDraw Surface) 컨테이너 형식을 활용하는 래스터 이미지 파일입니다. 비압축 및 압축(DXTn) 텍스처를 저장하고 다양한 유형의 데이터를 저장하기 위해 다양한 유형을 구현합니다. 또한 단일 레이어 텍스처, 밉맵이 있는 텍스처, 큐브 맵, 볼륨 맵 및 텍스처 배열과 같은 여러 유형의 데이터를 지원합니다. 이를 통해 DDS 파일은 디지털 사진 및 Windows 바탕 화면 배경 외에도 비디오 게임 텍스처 단위 모델을 저장할 수 있습니다. DDS 파일 형식은 Microsoft에서 DirectX SDK와 함께 사용하기 위해 개발했습니다.

## DDS 파일 형식

DDS 파일은 바이너리 파일로 저장되며 DirectX SDK와 함께 사용할 수 있습니다. DirectX의 성능을 활용하여 3D 게임과 같은 실시간 렌더링 응용 프로그램을 개발합니다.

### DDS 파일 레이아웃

[DDS 파일 레이아웃](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout)은 Microsoft에서 자세히 문서화했습니다. 바이너리 DDS 파일에는 다음 정보가 포함되어 있습니다.

* 4자리 코드 값 'DDS'(0x20534444)를 포함하는 DWORD(매직 넘버).
* 파일의 데이터에 대한 설명입니다.

DDS_HEADER는 데이터를 설명하고 DDS_PIXELFORMAT은 픽셀 형식을 설명합니다. 이 둘은 더 이상 사용되지 않는 DDSURFACEDESC2, DDSCAPS2 및 DDPIXELFORMAT DirectDraw 7 구조를 대체합니다.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[DDS 파일 형식 프로그래밍 가이드](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide)에서 이 파일 형식의 기술적인 세부 사항을 자세히 설명합니다.

## 참고문헌

* [DDS - 위키피디아 작성](https://en.wikipedia.org/wiki/DirectDraw_Surface)
* [ZSoft PCX 파일 형식 기술 참조 매뉴얼](http://qzx.com/pc-gpe/pcx.txt)

