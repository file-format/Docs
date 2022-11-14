{
  "date" : "2020-08-20",
  "keywords" :[ "fon 파일", "fon 파일 형식", "fon 파일이란", "파일", "fon 예제", "fon 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - 글꼴 라이브러리 파일",
  "description":"FON 파일을 만들고 열 수 있는 FON 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## .FON 파일이란?

확장자가 .fon인 파일은 실제로 실행 파일이지만 .fon으로 이름이 변경된 Microsoft Windows 3.x 글꼴 라이브러리입니다. 자체적으로 [.fnt](/ko/font/fnt/) 파일의 모음이며 응용 프로그램은 시스템 글꼴에 액세스하는 동안 이를 참조합니다. 이것이 리소스 파일의 역할을 하는 이유입니다. Microsoft Windows 글꼴 보기 응용 프로그램을 사용하여 Windows OS에서 열 수 있습니다.

## FON 파일 형식

FON 파일에는 글꼴 리소스가 포함되며 리소스(.res) 파일 형식이 있습니다. .res 파일 형식은 파일 헤더와 데이터 섹션 사양을 지정합니다. .fnt는 리소스 파일에 포함된 리소스 데이터 파일이기도 합니다. FON 파일은 이진 파일 형식을 가지며 응용 프로그램/옥텟 스트림 MIME 형식을 갖습니다.

글꼴 리소스는 다른 유형의 리소스와 달리 응용 프로그램의 리소스에 추가되지 않습니다. 대신 EXE 파일에 추가되고 .fon 파일로 이름이 바뀌므로 응용 프로그램 대신 라이브러리 파일이 생성됩니다. 여러 개별 글꼴은 각 그룹이 리소스 그룹 구조를 따르는 글꼴 그룹의 구성 요소를 구성합니다. 글꼴 리소스는 이러한 리소스 그룹 구조를 사용합니다. 그룹 헤더에는 그룹의 특정 글꼴에 액세스하는 데 필요한 모든 정보가 있습니다. 글꼴 구성 요소 리소스의 형식은 다음과 같습니다.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/ko/font/fnt/) file)
```
단일 .rc 리소스 파일에 혼합 리소스 선언이 있을 수 있습니다. 글꼴 그룹은 리소스 파일의 어느 위치에나 있을 수 있으며 연속적일 필요는 없습니다. FONTDIR의 수동 입력을 추가하려면 .RES 파일을 생성하는 프로그램이 필요합니다. 다음은 그룹 헤더의 구조입니다.

```
[일반 리소스 헤더(유형 = 7)]

WORD NumberOfFonts; // .RES 파일의 총 개수
```     
The remaining data is repeated for every font in the .RES file.

```
WORD 글꼴서수;
struct FontDirEntry {
워드 df버전;
DWORD df크기;
char df저작권[60];
단어 df 유형;
워드 df포인트;
단어 dfVertRes;
단어 dfHorizRes;
단어 dfAscent;
단어 dfInternalLeading;
단어 dfExternalLeading;
BYTE df이탤릭체;
BYTE df밑줄;
BYTE dfStrikeOut;
단어 dfWeight;
BYTE dfCharSet;
단어 dfPixWidth;
단어 dfPixHeight;
BYTE dfPitchAndFamily;
단어 dfAvgWidth;
단어 dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
워드 dfWidthBytes;
DWORD df장치;
DWORD dfFace;
DWORD dfReserved;
char sz장치 이름[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

