{
  "date" : "2020-01-11",
  "keywords" :[ "x 파일", "x 파일 형식", "x 파일이란", "파일", "x 예제", "x 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0 파일 형식",
  "description":"DirectX X 파일 형식과 DirectX X 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## X 파일이란?

확장자가 .x인 파일은 Microsoft DirectX 2.0과 함께 도입된 [DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) 3D 그래픽 레거시 파일 형식을 나타냅니다. 게임에서 3D 그래픽 렌더링에 사용되었으며 메쉬, 텍스처, 애니메이션 및 사용자 정의 개체에 대한 구조를 지정합니다. Autodesk FBX 파일 형식이 보다 현대적인 형식으로 더 잘 작동하기 때문에 2014년부터 더 이상 사용되지 않습니다. X는 템플릿 기반이며 사용 지식이 없습니다.

Microsoft DirectX 및 일반 텍스트 편집기를 사용하여 DirectX X 파일을 열 수 있습니다.

## X 파일 형식

[X 파일 참조](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file)에는 다음을 수행하는 데 사용되는 API 요소에 대한 참조 정보가 포함되어 있습니다. DirectX .x 파일로 작업합니다. 이 형식은 다른 응용 프로그램에서 데이터 템플릿을 통해 상위 수준 기본 요소를 정의하는 데 사용하는 하위 수준 데이터 기본 요소를 제공합니다. DirectX 6.0에는 .x 파일을 읽고 쓸 수 있는 인터페이스와 메서드가 도입되었습니다. DirectX 3.0은 이 파일 형식의 바이너리 버전을 도입했습니다.

DirectX 9에서 정의한 [X 파일 형식 참조](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)에는 .x에 대한 참조 정보가 포함되어 있습니다. 바이너리 및 텍스트 인코딩의 파일.

### 이진 인코딩

[이진 형식](https://learn.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding)은 DirectX X 형식을 텍스트 형식의 토큰화된 표현으로 정의합니다. 이러한 토큰은 문법적 구조를 제공하기 위해 독립형일 수 있거나 필요한 데이터를 제공하는 기록 보유 토큰일 수 있습니다.

#### 헤더

바이너리 헤더는 다음 정의를 사용하여 읽고 쓸 수 있습니다.

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### 텍스트 인코딩

DirectX .x 파일은 파일이 사용되는 방식에 의존하지 않으며 특정 응용 프로그램과 관련이 없습니다. 이 템플릿 기반 접근 방식을 사용하면 모든 클라이언트 응용 프로그램에서 .x 파일 형식을 사용할 수 있습니다.


#### 헤더

가변 길이 헤더는 필수이며 데이터 스트림의 시작 부분에 있어야 합니다. 헤더에는 다음 데이터가 포함됩니다.

|유형 |하위 유형 |크기 |내용 |내용 의미|
---|---|---|---|---|
|매직넘버(필수)| | 4바이트 |xof |
|버전 번호(필수) |주 번호 |2바이트 |03 |주 버전 3|
| |부 번호 |2바이트 |02 |부 버전 2|
|형식 유형(필수)| |4바이트 |"txt" |텍스트 파일|
| | | |"빈 "| 바이너리 파일|
| | | |"tzip"| MSZip 압축 텍스트 파일|
| | | |"bzip"| MSZip 압축 바이너리 파일|
|플로트 크기(필수)| |4바이트| 0064| 64비트 부동 소수점|
| | | |0032 |32비트 부동 소수점|


## 참고문헌

* [X 파일 레거시](https://learn.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9 파일 형식 참조](https://learn.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

