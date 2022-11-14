{
  "date" : "2019-12-03",
  "keywords" :[ "DOCX","파일", "형식", "파일 형식", "확장자","DOCX 파일이란?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"DOCX 파일을 만들고 열 수 있는 DOCX 파일 형식과 API에 대해 알아보세요.",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## .DOCX 파일이란? ##

DOCX는 Microsoft Word 문서용으로 잘 알려진 형식입니다. 2007년 Microsoft Office 2007 출시와 함께 도입된 이 새로운 문서 형식의 구조는 일반 바이너리에서 XML과 바이너리 파일의 조합으로 변경되었습니다. Docx 파일은 Word 2007 및 측면 버전에서 열 수 있지만 DOC 파일 확장자를 지원하는 이전 버전의 MS Word에서는 열 수 없습니다.

## 간략한 역사 ##

Microsoft가 DOC 파일 형식에 대한 사양을 공개한 후 경쟁업체에서 형식을 역설계하고 자체 응용 프로그램에서 동일한 지원을 제공하는 것이 쉬웠습니다. 또한 Open Document 형식 형태의 Open Office와의 경쟁으로 인해 Microsoft는 보다 개방적이고 광범위한 표준을 채택하게 되었습니다. Microsoft가 **Office Open XML** 표준을 수용하기 위해 변경하기로 결정한 것은 2000년 초였습니다. 이 새로운 표준에 따른 문서에는 [.docx 확장자](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), "X" XML을 위한 것입니다. 2007년에 이 새로운 파일 형식은 Office 2007의 일부가 되었으며 새 버전의 Microsoft Office에서도 계속 사용됩니다. 새로운 파일 형식은 작은 파일 크기, 적은 손상 변경 및 올바른 형식의 이미지 표현이라는 이점을 추가했습니다.

## DOCX 파일 형식 사양 - 추가 정보

Docx 파일은 ZIP 아카이브에 포함된 XML 파일 모음으로 구성됩니다. 새 Word 문서의 내용은 내용의 압축을 풀면 볼 수 있습니다. 컬렉션에는 다음과 같이 분류되는 XML 파일 목록이 포함되어 있습니다.

* 메타데이터 파일 - 아카이브에서 사용할 수 있는 다른 파일에 대한 정보를 포함합니다.
* 문서 - 문서의 실제 내용을 포함합니다.

### 메타데이터 파일 ###

Microsoft Word는 이러한 파일을 사용하여 파일 간의 관계를 찾고 문서 내용을 찾습니다. Word 문서 아카이브를 추출하면 아래에 설명된 것과 같은 파일이 많이 포함됩니다.

#### 관계 - \_rels/.rels ####

이 파일에는 문서 내용 및 기타 참조를 찾을 위치를 MS Word에 알려주는 정보가 포함되어 있습니다. 각 관계는 고유한 관계 ID로 식별되며 참조된 XML 파일을 대상으로 지정합니다. 샘플 관계 파일은 다음과 같이 표시됩니다.

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### 콘텐츠 유형 ####

문서에는 이미지, 테마, 워드 아트 등과 같은 여러 미디어 유형이 포함될 수 있습니다. [Content_Types].xml에는 문서에 있는 이러한 미디어 유형에 대한 정보가 포함되어 있습니다. 이러한 XML 파일의 내용은 다음과 같습니다.

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### 리소스 참조 - \_rels/document.xml.rels ####

문서에 포함된 이미지와 같은 리소스에 대한 정보는 이 XML 파일에서 참조됩니다.

#### 주요 문서 내용 ####

이것은 문서의 텍스트 내용을 포함하는 아카이브의 기본 XML 파일을 나타냅니다. 이 콘텐츠는 OpenOffice XML 사양에 따라 다양한 노드로 표시됩니다. 이 파일의 내용은 대부분 단락과 표로 구성되어 있지만 다른 노드도 될 수 있습니다.

### 파일 형식 노드 ###

기본 document.xml 파일은 파일의 전체 내용을 나타내는 노드 모음입니다. 각 노드에는 추가 노드 또는 내용을 캡슐화하는 시작과 끝이 있습니다. 이러한 xml 파일의 간단한 예는 다음과 같습니다.

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

다음은 콘텐츠 표현을 위해 DOCX 파일에 포함된 일부 노드에 대한 정보입니다.

`<w:document> ` - 파일의 주요 내용의 루트 요소를 나타냅니다.

`<w:body> ` - 단락, 테이블 및 섹션과 같은 다른 많은 요소 노드로 구성될 수 있는 문서의 본문을 나타냅니다.

#### 단락 ####

단락은 문서 내의 주요 콘텐츠 홀더입니다. **로 표시됩니다.<w:p> ** 문서 내의 요소. 단락은 하나 이상의 실행으로 구성됩니다 **<w:r> ** 단락의 실제 텍스트를 포함합니다. 실행 외에도 단락에는 하이퍼링크, 주석 등과 같은 다른 문서 요소가 포함될 수 있습니다. 단락 구조의 예는 다음과 같습니다.

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## 참조 ##

* [MS - DOCX 파일 형식](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [오피스 오픈 XML](http://officeopenxml.com/)

