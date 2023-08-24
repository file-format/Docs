{
  "date" : "2019-10-11",
  "keywords" :[ "vsx 파일", "vsx 파일 형식", "vsx 파일이란", "파일", "vsx 예제", "vsx 파일 확장자","확장자", "형식" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VSX - Microsoft Visio 스텐실 파일 형식",
  "description":"VSX 파일 형식과 VSX 파일을 만들고 열 수 있는 API에 대해 알아보세요.",
  "linktitle" : "VSX",
  "menu" : {
    "docs" : {
	  "identifier":"visio-vsx",
      "parent" : "visio"
}
},
  "lastmod" : "2020-08-03"
}

## .VSX 파일이란?

확장명이 .vsx인 파일은 Microsoft Visio에서 다이어그램을 만드는 데 사용되는 드로잉과 셰이프로 구성된 스텐실을 나타냅니다. VSX 파일은 XML 파일 형식으로 저장되며 Visio 2013까지 지원되었습니다. 이는 Microsoft Visio 2013에 도입된 기본 [VSDX](/ko/visio/vsdx/) 파일 형식과 다릅니다. VSX 파일은 모든 텍스트 편집기에서 열 수 있습니다. 내용을 보려면. VSX 파일은 PDF 및 HTML과 같은 다양한 파일 형식으로 변환할 수 있습니다.

## VSX 파일 형식 ##

XML 편집기에서 연 샘플 VSX 파일은 다음과 같습니다. 일반적인 VSX 파일에는 XML 표현에서 관찰되는 다음과 같은 노드가 있습니다.

### 문서 속성 ###

문서 속성 섹션에 포함된 일부 요소는 다음과 같습니다.

```
<Creator>Creation Information</Creator>
<BuildNumberCreated>939530118</BuildNumberCreated>
<BuildNumberEdited>939530118</BuildNumberEdited>
<PreviewPicture Size#"20172">...</PreviewPicture>
<CustomProps>
<CustomProp Name#"_VPID_EXTENDED_VDX" PropType#"Number">1</CustomProp>
</CustomProps>
<TimeCreated>2012-07-06T23:00:56</TimeCreated>
<TimeSaved>2017-06-11T16:06:08</TimeSaved>
<TimeEdited>2012-07-06T23:06:33</TimeEdited>
<TimePrinted>2012-07-06T23:00:56</TimePrinted>
```

### 문서 설정 ###

일반적인 문서 설정 노드에는 다음 요소가 포함됩니다.

```
<GlueSettings>9</GlueSettings>
<SnapSettings>65847</SnapSettings>
<SnapExtensions>34</SnapExtensions>
<DynamicGridEnabled>0</DynamicGridEnabled>
<ProtectStyles>0</ProtectStyles>
<ProtectShapes>0</ProtectShapes>
<ProtectMasters>0</ProtectMasters>
<ProtectBkgnds>0</ProtectBkgnds>
```

### 색상 ###

색상 노드에는 문서 전체에 사용할 색상 항목이 포함되어 있습니다.

```
<ColorEntry IX#"0" RGB#"#000000"/>
<ColorEntry IX#"1" RGB#"#FFFFFF"/>
<ColorEntry IX#"2" RGB#"#FF0000"/>
<ColorEntry IX#"3" RGB#"#00FF00"/>
<ColorEntry IX#"4" RGB#"#0000FF"/>
<ColorEntry IX#"5" RGB#"#FFFF00"/>
<ColorEntry IX#"6" RGB#"#FF00FF"/>
<ColorEntry IX#"7" RGB#"#00FFFF"/>
<ColorEntry IX#"8" RGB#"#800000"/>
<ColorEntry IX#"9" RGB#"#008000"/>
<ColorEntry IX#"10" RGB#"#000080"/>
<ColorEntry IX#"11" RGB#"#808000"/>
<ColorEntry IX#"12" RGB#"#800080"/>
<ColorEntry IX#"13" RGB#"#008080"/>
<ColorEntry IX#"14" RGB#"#C0C0C0"/>
<ColorEntry IX#"15" RGB#"#E6E6E6"/>
<ColorEntry IX#"16" RGB#"#CDCDCD"/>
<ColorEntry IX#"17" RGB#"#B3B3B3"/>
<ColorEntry IX#"18" RGB#"#9A9A9A"/>
<ColorEntry IX#"19" RGB#"#808080"/>
<ColorEntry IX#"20" RGB#"#666666"/>
<ColorEntry IX#"21" RGB#"#4D4D4D"/>
<ColorEntry IX#"22" RGB#"#333333"/>
<ColorEntry IX#"23" RGB#"#1A1A1A"/>
```

### 얼굴 이름 ###

파일의 FaceNames 노드는 문서에 사용된 TypeFace.FaceNames 속성을 나타냅니다.

```
<FaceName ID#"1" Name#"Arial Unicode MS" UnicodeRanges#"-1 -369098753 63 0" CharSets#"1614742015 -65536" Panos#"2 11 6 4 2 2 2 2 2 4" Flags#"357"/>
<FaceName ID#"2" Name#"Symbol" UnicodeRanges#"0 0 0 0" CharSets#"-2147483648 0" Panos#"5 5 1 2 1 7 6 2 5 7" Flags#"261"/>
<FaceName ID#"3" Name#"Wingdings" UnicodeRanges#"0 0 0 0" CharSets#"-2147483648 0" Panos#"5 0 0 0 0 0 0 0 0 0" Flags#"261"/>
<FaceName ID#"4" Name#"Calibri" UnicodeRanges#"-536870145 1073786111 1 0" CharSets#"536871327 0" Panos#"2 15 5 2 2 2 4 3 2 4" Flags#"261"/>
<FaceName ID#"5" Name#"SimSun" UnicodeRanges#"3 680460288 6 0" CharSets#"262145 0" Panos#"2 1 6 0 3 1 1 1 1 1" Flags#"421"/>
<FaceName ID#"6" Name#"PMingLiU" UnicodeRanges#"-1610611969 684719354 22 0" CharSets#"1048577 0" Panos#"2 2 5 0 0 0 0 0 0 0" Flags#"421"/>
<FaceName ID#"7" Name#"MS PGothic" UnicodeRanges#"-536870145 1791491579 18 0" CharSets#"1073873055 -539557888" Panos#"2 11 6 0 7 2 5 8 2 4" Flags#"421"/>
<FaceName ID#"8" Name#"Dotum" UnicodeRanges#"-1342176593 1775729915 48 0" CharSets#"1074266271 -539557888" Panos#"2 11 6 0 0 1 1 1 1 1" Flags#"421"/>
<FaceName ID#"9" Name#"Sylfaen" UnicodeRanges#"67110535 0 0 0" CharSets#"536871071 0" Panos#"1 10 5 2 5 3 6 3 3 3" Flags#"325"/>
<FaceName ID#"10" Name#"Estrangelo Edessa" UnicodeRanges#"-2147475389 0 128 0" CharSets#"1 0" Panos#"3 8 6 0 0 0 0 0 0 0" Flags#"325"/>
<FaceName ID#"11" Name#"Vrinda" UnicodeRanges#"65539 0 0 0" CharSets#"1 0" Panos#"2 11 5 2 4 2 4 2 2 3" Flags#"325"/>
<FaceName ID#"12" Name#"Shruti" UnicodeRanges#"262147 0 0 0" CharSets#"1 0" Panos#"2 11 5 2 4 2 4 2 2 3" Flags#"325"/>
<FaceName ID#"13" Name#"Mangal" UnicodeRanges#"32771 0 0 0" CharSets#"1 0" Panos#"2 4 5 3 5 2 3 3 2 2" Flags#"325"/>
<FaceName ID#"14" Name#"Tunga" UnicodeRanges#"4194307 0 0 0" CharSets#"1 0" Panos#"2 11 5 2 4 2 4 2 2 3" Flags#"325"/>
<FaceName ID#"15" Name#"Sendnya" UnicodeRanges#"-520082689 -1073741822 8 0" CharSets#"536936959 539492352" Panos#"2 11 6 4 2 2 2 2 2 4" Flags#"327"/>
<FaceName ID#"16" Name#"Raavi" UnicodeRanges#"131075 0 0 0" CharSets#"1 0" Panos#"2 11 5 2 4 2 4 2 2 3" Flags#"325"/>
<FaceName ID#"17" Name#"Dhenu" UnicodeRanges#"-520082689 -1073741822 8 0" CharSets#"536936959 539492352" Panos#"2 11 6 4 2 2 2 2 2 4" Flags#"327"/>
<FaceName ID#"18" Name#"Latha" UnicodeRanges#"1048579 0 0 0" CharSets#"1 0" Panos#"2 11 6 4 2 2 2 2 2 4" Flags#"325"/>
<FaceName ID#"19" Name#"Gautami" UnicodeRanges#"2097155 0 0 0" CharSets#"1 0" Panos#"2 11 5 2 4 2 4 2 2 3" Flags#"325"/>
<FaceName ID#"20" Name#"Cordia New" UnicodeRanges#"-2130706429 0 0 0" CharSets#"65537 0" Panos#"2 11 3 4 2 2 2 2 2 4" Flags#"325"/>
<FaceName ID#"21" Name#"Arial" UnicodeRanges#"-536859905 -1073711037 9 0" CharSets#"1073742335 -65536" Panos#"2 11 6 4 2 2 2 2 2 4" Flags#"325"/>
<FaceName ID#"22" Name#"Malgun Gothic" UnicodeRanges#"-1879047505 30899451 18 0" CharSets#"524289 0" Panos#"2 11 5 3 2 0 0 2 0 4" Flags#"421"/>
<FaceName ID#"23" Name#"Times New Roman" UnicodeRanges#"-536859905 -1073711039 9 0" CharSets#"1073742335 -65536" Panos#"2 2 6 3 5 4 5 2 3 4" Flags#"325"/>
<FaceName ID#"33" Name#"Arial Black" UnicodeRanges#"647 0 0 0" CharSets#"536871071 -539557888" Panos#"2 11 10 4 2 1 2 2 2 4" Flags#"260"/>
```

### 스타일 시트 ###

StyleSheets 노드에는 문서에 사용된 스타일 시트에 대한 정보가 포함되어 있습니다. 각 스타일 시트는 스타일 속성, 선, 채우기 패턴, 텍스트 블록 및 기타 요소에 대한 정보를 가질 수 있습니다.

### 문서 시트 ###

DocumentSheet 노드에는 문서 속성 및 사용자 이름 정보에 대한 정보가 포함되어 있으며 다음과 같습니다.

```
<DocProps>
<OutputFormat>0</OutputFormat>
<LockPreview>0</LockPreview>
<AddMarkup>0</AddMarkup>
<ViewMarkup>0</ViewMarkup>
<PreviewQuality>0</PreviewQuality>
<PreviewScope>0</PreviewScope>
<DocLangID>1033</DocLangID>
</DocProps>
<User NameU#"msvNoAutoConnect" ID#"1">
<Value>1</Value>
<Prompt F#"No Formula"/>
</User>
</DocumentSheet>
```

### 페이지 ###

페이지 속성, 레이아웃, 눈금자 격자, 도형, 이미지 및 기타 유사한 데이터와 같은 Visio 문서의 페이지에 대한 정보가 포함되어 있습니다.

