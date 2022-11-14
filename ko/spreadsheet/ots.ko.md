{
  "date" : "2019-12-16",
  "keywords" :[ "OTS", "파일", "확장자", "파일 형식", "엑셀", "스프레드시트" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"OTS 파일을 만들고 열 수 있는 OTS 파일 형식과 API에 대해 알아보세요.",
  "title" :"OTS - OpenDocument 스프레드시트 템플릿 파일 형식",
  "linktitle" : "OTS",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-01-19"
}

## .OTS 파일이란?

확장자가 .ots인 파일은 Apache OpenOffice에 포함된 Calc 응용 프로그램 소프트웨어로 만든 OpenDocument 스프레드시트 템플릿 파일입니다. Calc 응용 프로그램 소프트웨어는 Microsoft Office에서 사용할 수 있는 Excel과 유사합니다. OTS 파일 형식은 스타일, 글꼴, 데이터, 스프레드시트 레이아웃 및 서식과 관련된 미리 정의된 설정이 포함된 템플릿을 만드는 데 사용됩니다. OTF 파일에는 'mime-type application/vnd.oasis.opendocument.spreadsheet-template'이 있습니다. 이러한 템플릿 파일은 [ODS 파일 형식](/ko/spreadsheet/ods/)으로 저장되는 실제 데이터 파일을 생성하고 저장하기 위한 시작점으로 사용할 수 있습니다. OTS 파일은 OpenOffice 및 LibreOffice와 같은 응용 프로그램과 함께 사용할 수 있습니다.

## OTS 파일 형식

OTS 파일은 [ZIP](/ko/compression/zip/) 아카이브로 패키지가 포함된 여러 하위 문서 모음으로 구성된 OASIS의 OpenDocument XML 기반 파일 형식으로 저장됩니다. 각 zip 아카이브는 전체 문서의 일부를 저장하고 각 하위 문서는 문서의 특정 측면을 저장합니다. 예를 들어, 한 하위 문서에는 스타일 정보가 포함되어 있고 다른 하위 문서에는 문서 내용이 포함되어 있습니다. 일반적인 ODF 문서에는 다음 구성 요소가 있습니다.

### OTS Content.xml

content.xml 파일에는 문서의 실제 내용이 포함되어 있습니다. 그러나 여기에는 이미지와 같은 이진 데이터가 포함되지 않습니다.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### OTS 파일 형식의 Styles.xml

styles.xml 파일에는 스타일 정보가 포함되어 있으며 서식 지정 및 레이아웃에 많이 사용됩니다. 스타일 유형에는 다음이 포함됩니다.

* 단락 스타일
* 페이지 스타일
* 캐릭터 스타일
* 프레임 스타일
* 목록 스타일

### 메타.xml

meta.xml 파일은 Author, Last Modified Date 등과 같은 파일 메타데이터에 대한 정보를 담고 있습니다.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### 설정.xml

`settings.xml` 파일에는 확대/축소 비율 및 커서 위치와 같은 문서 수준 설정이 포함됩니다.

## 참조 ##

* [OpenDocument 1.2 사양](https://www.oasis-open.org/standards#opendocumentv1.2)
* [OpenDocument - 위키피디아 작성](https://en.wikipedia.org/wiki/OpenDocument)

