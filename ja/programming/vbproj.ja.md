{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "ファイル", "拡張子", "ファイル形式", "VB プロジェクト ファイル", "プログラミング ガイド" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"VBPROJ ファイル形式と,VBPROJ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .VBPROJ ファイルとは?

拡張子が .vbproj のファイルは、Visual Studio ソリューション内でプロジェクトをビルドするために Microsoft の MSBuild エンジンによって使用される Microsoft Visual Basic プロジェクト ファイルです。 [C#](/programming/cs/)で書かれた.NETプロジェクトの[CSPROJ](/programming/csproj/)ファイルに似ています。 MSBuild エンジンは、VBPROJ ファイルからさまざまなグループに含まれる情報を読み取り、出力ファイルを生成します。 VBPROJ ファイルには、プロジェクトを定義するグローバル識別子、クラス、およびプロパティに関連する情報を含めることができます。 VBPROJ ファイルは、Microsoft Visual Studio と、Windows および MacOS オペレーティング システムのメモ帳などの一般的なテキスト エディタを使用して開いて編集できます。

## VBPROJ ファイル形式 - 詳細情報

VBPROJ ファイルは、[MSBuild XML スキーマ](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-プロジェクト ファイル スキーマ参照?view=vs-2019)。 VBPROJ ファイルには、特定の設定グループに関連する情報を定義する XML タグの形式で情報が含まれています。 Microsoft Visual Studio IDE でこれらの設定ファイルを開いて編集することを強くお勧めします。

### VBPROJ 要素

VB 設定ファイルの構成要素は、次の図のようになります。

{{< figure src="../vbproj.png" alt="VBPROJ ファイル形式" >}}

次の表に、これらの要素の簡単な説明を示します。

|要素|説明|
---|---|
|プロジェクト|すべてのプロジェクト ファイルのルート要素であり、プロジェクト ファイルの XML スキーマの識別に加えて、ビルド プロセスのエントリ ポイントを指定する属性を含めることができます。
|特性と条件|プロパティはキーと値のペアで構成され、PropertyGroup 要素内で定義されます。プロパティ要素名はプロパティ キーを表し、要素の内容はプロパティ値を定義します。|
|アイテムとアイテム グループ|プロジェクト ファイル内のアイテムは、ファイル コード ファイル、構成ファイル、コマンド ファイル、およびビルド プロセスの一部として必要なその他のファイルなど、ビルド プロセスへの入力です。アイテムは、ItemGroup 要素内で定義する必要があります。|
|目標とタスク| Task 要素は、個々のビルド命令 (またはタスク) を表します。 MSBuild には、コピー、CSC、VBC、Exec などの多数の定義済みタスクが含まれています。タスクは常に、順次実行される 1 つ以上のタスクのセットである `Target` 要素に含まれている必要があり、プロジェクト ファイルには複数のターゲットを含めることができます。|

## 参考文献

* [プロジェクト ファイルについて](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [MSBuild スキーマ要素](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

