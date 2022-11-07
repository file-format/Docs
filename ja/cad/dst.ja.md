{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "ファイル", "形式", "拡張子", "API", "AutoCAD シート セット" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - AutoCAD シート セット ファイル",
  "description" :".dst ファイルと,DST ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## .DSTファイルとは何ですか?

DST ファイルは、シート セットを定義するための関連付けと情報を含む AutoCAD ファイルです。これらは、既定のシート セット ストレージ フォルダである AutoCAD シート セットに格納されます。 DST ファイルには実際の図面レイアウトは含まれていませんが、これらのシート セットに関連付けられている選択した [DWG](/cad/dwg/) および [DWT](/cad/dwt/) ファイルからこれらを参照します。ネットワーク環境では、すべてのチーム メンバーがこれらの関連ファイルにネットワーク アクセスできる必要があります。 DST ファイルは [XML](/web/xml/) ファイル形式でディスクに保存されます。

## DST ファイル形式 - 詳細情報

DST ファイルは、AutoDesk Sheet Set Manager (SSM) ツールで作成されます。チーム内の誰かがファイルにアクセスすると、DST ファイルが短時間開かれ、更新された情報とともに保存されます。同じ DST ファイルへの同時アクセスは、SSM ツールによって管理されます。このツールは、ファイルがアクセスされているときにロック アイコンを表示します。

特定の時点で、シートのステータスは次のいずれかの状態になります。

* シートは編集可能です。
※シートはロックされています。
* シートが見つからないか、予期しないフォルダーの場所にあります。

## 参考文献

* [DST シート セットの使用について](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-577D8EA0-85F2 -4829-B4F9-8CAD6F7AAACC-htm.html)
* [シート セットについて学ぶ](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-34D889BC-19AD- 4CD1-ADB1-F359D9B515FB-htm.html)
* [AutoCAD シート セットをマスターする](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

