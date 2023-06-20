{
  "date" : "2020-03-16",
  "keywords" :[ "PAT 파일", "포맷", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"PAT 파일 형식과 PAT 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "title" :"PAT 파일 형식",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## .PAT 파일이란?

확장자가 .pat인 파일은 AutoCAD 소프트웨어에서 사용하는 CAD 파일입니다. PAT 파일을 열 수 있는 응용 프로그램은 이러한 파일에 저장된 해치 패턴을 사용하여 영역의 질감/채움에 대한 정보를 얻습니다. 포함된 패턴은 그려진 개체의 재질 모양에 대한 정보를 제공합니다. PAT 파일은 Autodesk AutoCAD, CorelDRAW Graphics Suite 및 Ketron Software와 같은 응용 프로그램에서 열 수 있습니다. PAT 파일은 JPG, PNG, BMP 등과 같은 다양한 이미지 형식으로 변환할 수 있습니다.

## PAT 파일 형식

PAT 파일은 일반 텍스트 형식으로 작성되며 모든 텍스트 편집기에서 열 수 있습니다. 이 파일의 해치 패턴은 벡터 기반이며 AutoCAD 문서에 설명된 구문을 따릅니다.

모든 패턴은 점 0,0에서 시작하며 패턴은 해칭 경계를 덮도록 계산됩니다.

### 패턴 정의

모든 패턴 정의는 다음 필드로 구성됩니다.
* 선행 '\*'
* 이름 - 이름에는 공백, 구두점, 괄호 또는 슬래시를 사용할 수 없습니다.
* 설명

해치 패턴의 표준 형식은 `<\*>입니다.<name> <, 설명>`. 이름과 설명은 쉼표로 구분되며 설명은 80자를 초과할 수 없습니다. 해치 패턴은 이 정보 뒤에 정의됩니다.

### 해치 패턴 예
다음은 정사각형 패턴의 예입니다.
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
평행 사변형 패턴을 보여주는 또 다른 예는 다음과 같습니다.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## 참조 ##

* [Autodesk의 해시 패턴](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

