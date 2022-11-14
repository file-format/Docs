{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "wpl 파일", "확장자", "형식", "wpl 파일이란", "음악", "wpl 파일 형식"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"WPL 파일을 생성, 변환 및 열 수 있는 WPL 파일 형식 및 API에 대해 알아보세요.",
  "title" :"WPL - Windows Media Player 재생 목록 파일",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## .WPL 파일이란?

확장자가 .wpl인 파일에는 Microsoft Windows Media Player에서 실행할 노래 재생 목록이 포함되어 있습니다. 이러한 파일은 일반적으로 사용자가 비디오 및 오디오 컬렉션을 위해 만듭니다. WPL 파일로 작성된 콘텐츠는 .wpl 파일 작성자가 선택한 멀티미디어 파일의 디렉터리 경로 또는 위치일 뿐이므로 미디어 플레이어 응용 프로그램은 디렉터리 위치에서 멀티미디어 콘텐츠를 신속하게 찾고 재생할 수 있습니다.

## WPL 파일 형식

WPL(Windows Media Player 재생 목록)은 Microsoft Windows Media Player 버전 9 이상에서 사용되는 독점 파일 형식입니다. 멀티미디어 재생 목록을 저장하는 컴퓨터 파일 형식입니다. 기본적으로 재생 목록은 .wpl(Windows Media Player 재생 목록) 확장자로 저장됩니다. 이 확장자를 지원하지 않는 장치에서 데이터 디스크를 재생하려면 [.m3u](/ko/audio/m3u) 확장자를 대신 사용할 수 있습니다. WPL 파일의 요소는 XML 형식으로 표시됩니다.

최상위 요소 "smil"은 파일의 요소가 SMIL(Synchronized Multimedia Integration Language) 구조를 따르도록 지정합니다. 파일은 .wpl 확장자로 생성 및 저장되며 MIME 유형은 application/vnd.ms-wpl입니다.

### WPL 예제

다음은 wpl 파일의 예입니다.
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## 참조 ##

* [MPEG-1 오디오 레이어 II - 위키피디아 작성](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

