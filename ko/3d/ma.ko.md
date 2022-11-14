{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma 파일", "ma 파일 형식", "파일 형식", "3d","ma 파일 다운로드", ".ma 파일", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"MA 파일 형식과 MA 파일을 열고 생성할 수 있는 API에 대해 알아보세요.",
  "title" :"MA 파일 형식",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## .MA 파일이란?

확장자가 .ma인 파일은 Autodesk Maya 응용 프로그램으로 만든 3D 프로젝트 파일입니다. 여기에는 파일에 대한 정보를 지정하기 위한 많은 텍스트 명령 목록이 포함되어 있습니다. **.ma 파일**은 파일이 손상된 경우 명령 문제를 해결하기 위해 모든 텍스트 편집기에서 열고 편집할 수 있습니다. 이러한 파일에는 지오메트리, 조명, 애니메이션 및 렌더링과 같은 3D 장면 정보를 정의하기 위한 정보가 포함되어 있습니다.

## MA 파일 형식

MA 파일은 바이너리 파일 형식으로 디스크에 저장되는 MB 파일과 달리 ASCII 텍스트 형식으로 디스크에 저장됩니다. MA 파일 형식에 대한 자세한 참조는 [Autodesk Maya 문서](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)에서 볼 수 있으며 참조할 수 있습니다. 개발자의 참조를 위해.

### MA 파일 헤더

MA 파일 헤더는 파일의 생성 정보와 수정된 날짜를 제공하는 주석 섹션으로 시작합니다. Maya 파일 판독기는 이 블록이 정보 목적으로만 사용되기 때문에 무시합니다. 헤더는 "//Maya"로 처음 6자로 시작해야 합니다.

ASCII 파일 헤더는 다음과 같습니다.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### 파일 참조

.ma 파일의 파일 참조 섹션에는 이 파일에서 참조되는 다른 모든 Maya 파일에 대한 정보가 포함되어 있습니다. 참조된 각 파일은 동일한 파일에 포함된 단일 파일 명령을 사용하여 읽을 수 있습니다. 참조에 사용되는 파일 명령의 구문은 다음과 같습니다.

```
file -r -rpr prefixString fileName;
```
또는

```
file -r -ns nameSpace fileName
```
다음은 예제 문자열입니다.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
이 예는 `solar` 파일에 포함된 태양 객체가 "solar_sun"이라는 이름을 사용하여 이 파일에서 액세스할 수 있음을 보여줍니다.

### 요구 사항

.ma 파일의 Requirements 섹션은 일련의 필수 명령어로 구성되어 있으며 파일을 읽기 위해 필요한 버전, 플러그인 정보 등 May 정보를 알려준다. 요구 사항 섹션의 예는 다음과 같습니다.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


다음 섹션에서는 요구 사항을 지정합니다. 이것은 일련의 require 명령으로 구성됩니다. 파일의 이 섹션은 파일을 제대로 로드하는 데 필요한 소프트웨어를 Maya에 알려줍니다. 특히, Maya의 버전과 플러그인.

## MA 파일 다운로드
3D 모델의 MA 파일을 찾아서 다운로드하는 것은 약간 어렵습니다. 따라서 여기에서 샘플 MA 파일을 다운로드할 수 있습니다.

- [Sample.ma](../sample.ma)


## 참고문헌

* [Maya ASCII 파일 구성 - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

