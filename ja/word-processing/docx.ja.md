{
  "date" : "2019-12-03",
  "keywords" :["DOCX","ファイル","形式","ファイルの種類","拡張子","DOCXファイルとは" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DOCX",
  "description":"DOCX ファイル形式と,DOCX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DOCX",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-12-03"
}

## .DOCX オプション番号##

DOCX は、Microsoft Word ドキュメントのよく知られた形式です。 2007 年の Microsoft Office 2007 のリリースで導入されたこの新しいドキュメント形式の構造は、プレーン バイナリから XML ファイルとバイナリ ファイルの組み合わせに変更されました。 Docx ファイルは、Word 2007 およびラテラル バージョンで開くことができますが、DOC ファイル拡張子をサポートする以前のバージョンの MS Word では開くことができません。

## 簡単な歴史 ##

Microsoft が DOC ファイル形式の仕様を公開した後、競合他社が形式をリバース エンジニアリングし、独自のアプリケーションで同じサポートを提供することは容易になりました。さらに、Open Document Format という形での Open Office との競合により、Microsoft はよりオープンで幅広い標準を採用することを余儀なくされました。 Microsoft が **Office Open XML** の標準に対応するために変更を行うことを決定したのは、2000 年初頭のことでした。この新しい標準に基づくドキュメントには、[.docx 拡張子](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)、「X」が付けられました。 XML用です。 2007 年までに、この新しいファイル形式は Office 2007 の一部となり、Microsoft Office の新しいバージョンでも引き継がれています。新しいファイル タイプには、ファイル サイズが小さい、破損の変更が少ない、適切にフォーマットされた画像表現などの利点が追加されています。

## DOCX ファイル形式の仕様 - 詳細情報

Docx ファイルは、ZIP アーカイブ内に含まれる XML ファイルのコレクションで構成されます。新しい Word 文書の内容は、その内容を解凍することで表示できます。コレクションには、次のように分類される XML ファイルのリストが含まれています。

* メタデータ ファイル - アーカイブで利用可能な他のファイルに関する情報が含まれています
* ドキュメント - ドキュメントの実際の内容が含まれています

### メタデータ ファイル ###

Microsoft Word は、これらのファイルを使用して、ファイル間の関係を見つけ、ドキュメントの内容を見つけます。 Word 文書のアーカイブを抽出すると、以下に示すような多数のファイルが含まれます。

#### 関係 - \_rels/.rels ####

このファイルには、文書の内容やその他の参照を検索する場所を MS Word に指示する情報が含まれています。各関係は一意の関係 ID によって識別され、参照される XML ファイルをターゲットとして指定します。リレーションシップ ファイルの例を次に示します。

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### コンテンツ タイプ ####

ドキュメントには、画像、テーマ、ワード アートなど、複数のメディア タイプを含めることができます。[Content_Types].xml には、ドキュメントに存在するメディア タイプに関する情報が含まれています。このような XML ファイルの内容は次のとおりです。

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### リソースへの参照 - \_rels/document.xml.rels ####

ドキュメントに埋め込まれた画像などのリソースに関する情報は、この XML ファイルで参照されます。

#### 主なドキュメントの内容 ####

これは、ドキュメントのテキスト コンテンツを含むアーカイブのメイン XML ファイルを参照します。このコンテンツは、OpenOffice XML 仕様に従ってさまざまなノードで表されます。このファイルのほとんどのコンテンツは、段落と表で構成されていますが、他のノードであってもかまいません。

### ファイル形式ノード ###

メインの document.xml ファイルは、ファイルの内容全体を表すノードのコレクションです。各ノードには、追加のノードまたはコンテンツをカプセル化する開始点と終了点があります。このような xml ファイルの簡単な例は次のとおりです。

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

以下は、内容を表すために DOCX ファイルに含まれるいくつかのノードに関する情報です。

`<w:document> ` - ファイルのメイン コンテンツのルート要素を表します。

`<w:body> ` - 段落、表、セクションなど、他の多くの要素ノードで構成できるドキュメントの本文を表します。

#### 段落 ####

段落は、ドキュメント内の主要なコンテンツ ホルダーです。 **で表されます<w:p>** ドキュメント内の要素。段落は、さらに 1 つ以上のランで構成されます **<w:r> ** 段落の実際のテキストが含まれています。ランに加えて、段落には、ハイパーリンク、コメントなどの他のドキュメント要素を含めることもできます。段落構造の例を以下に示します。

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

## 参照 ##

* [MS - DOCX ファイル形式](https://docs.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)
* [Office Open XML](http://officeopenxml.com/)

