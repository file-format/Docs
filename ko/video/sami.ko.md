{
"날짜": "2023-05-16",
  "keywords": [
"사미 파일",
"사미 파일이 무엇인가요?",
"sami 파일의 예",
"파일",
"사미 파일 확장자",
"확대"
],
  "author": {
"display_name": "샤킬 파이즈"
},
"draft": "false",
"toc": true,
"title": "SAMI 파일 형식 - 자막 및 메타데이터 교환 파일",
  "description":"SAMI 파일을 생성하고 열 수 있는 SAMI 형식과 API에 대해 알아보세요.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent" : "video"
}
},
"lastmod": "2023-05-16"
}

## .SAMI 파일이란?

확장자가 ".sami"인 파일은 일반적으로 SAMI(Subtitles And Metadata Interchange) 파일을 나타냅니다. SAMI는 비디오에 자막을 표시하는 데 사용되는 캡션 형식입니다. 원래는 Microsoft에서 Windows Media Player용으로 개발했습니다.

SAMI 파일에는 자막 또는 폐쇄 캡션에 대한 타이밍 정보와 텍스트 콘텐츠가 포함되어 있어 비디오 재생과 동기화할 수 있습니다. 이 형식은 글꼴 스타일, 색상, 화면에서의 자막 위치 지정과 같은 기본 서식 옵션을 지원합니다.

SAMI 파일은 일반적으로 일반 텍스트 파일이며 텍스트 편집기를 사용하여 열고 편집할 수 있습니다. SAMI 파일의 콘텐츠에는 일반적으로 파일에 대한 정보를 제공하는 헤더 섹션과 해당 타이밍 및 텍스트가 포함된 개별 자막 항목이 포함됩니다.

다음은 SAMI 파일의 모양에 대한 예입니다.

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI 파일은 일반적으로 Windows Media Player 또는 VLC Media Player와 같이 자막 표시를 지원하는 비디오 플레이어 또는 미디어 플레이어와 함께 사용됩니다. 플레이어는 SAMI 파일을 읽고 자막을 비디오 콘텐츠와 동기화하여 시청자가 비디오를 시청하는 동안 캡션을 읽을 수 있도록 합니다.

## 지원되는 HTML 태그

SAMI(자막 및 메타데이터 교환) 파일은 자막 형식 지정 및 스타일 지정을 위해 제한된 HTML 유사 태그 세트를 지원합니다. 다음은 SAMI에서 지원하는 일반적으로 사용되는 태그 중 일부입니다.

- ``<SAMI> :`` 전체 SAMI 파일을 캡슐화하는 루트 요소입니다.
- ``<HEAD> :`` SAMI 파일에 대한 헤더 정보가 포함되어 있습니다.
<html>- ``<TITLE> :`` SAMI 파일의 제목을 지정합니다. </html>
- ``<BODY> :`` 자막 항목과 타이밍 정보를 포함합니다.
- ``<SYNC> :`` 자막 항목의 동기화 지점을 나타냅니다. 자막이 표시되어야 하는 타이밍을 지정합니다.
- ``<P> :`` 자막의 실제 텍스트 내용을 포함합니다. 일반적으로 다음 내에서 사용됩니다.<SYNC> 차단하다.
<html>- `` <FONT>:`` 포함된 텍스트의 글꼴 속성을 정의합니다. 색상, 면, 크기 및 스타일과 같은 속성을 사용하여 글꼴 모양을 수정할 수 있습니다.</font>
- ``<BR> :`` 자막 내에 줄 바꿈을 삽입합니다.
<html>- `` <B>:`` 포함된 텍스트를 굵게 표시합니다.</b>
<html>- `` <I>:`` 둘러싸인 텍스트를 이탤릭체로 렌더링합니다.</i>
<html>- `` <U>:`` 밑줄이 그어진 텍스트를 렌더링합니다.</u>
- ``<C> :`` 화면에서 자막 텍스트의 위치나 정렬을 지정합니다. Center, Middle, Left, Right, Top, Bottom 및 이들의 조합과 같은 속성을 지원합니다.
- ``<LANG> :`` 자막 텍스트의 언어 코드를 지정합니다. 자막의 언어를 식별하는 데 도움이 됩니다.

다음은 SAMI 파일에서 지원하는 기본 태그 중 일부입니다. SAMI는 HTML 태그 및 속성의 전체 범위를 지원하지 않는다는 점에 유의하는 것이 중요합니다. 지원되는 태그는 광범위한 문서 구조나 상호 작용을 제공하기보다는 주로 자막 스타일과 위치 지정에 중점을 둡니다.

## 참고자료
* [사미](https://en.wikipedia.org/wiki/SAMI)

