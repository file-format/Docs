{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"CSPROJ ファイル形式と,CSPROJ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## CSProj ファイルとは?
CSPROJ 拡張子を持つファイルは、プロジェクトに含まれるファイルのリストとシステム アセンブリへの参照を含む C# プロジェクト ファイルを表します。 Microsoft VIiual Studio で新しいプロジェクトが開始されると、メイン ソリューション ([.sln](/programming/sln/)) ファイルと共に 1 つの .csproj ファイルを取得します。プロジェクト内に複数のアセンブリがある場合、同じ数のプロジェクト ファイルが存在し、.sln ファイルがプロジェクトの一部としてすべてを結び付けます。このファイルの内容は、含めるコンテンツ、プラットフォーム要件、バージョン管理情報、Web サーバーまたはデータベース サーバーの設定、および実行する必要があるタスクなど、プロジェクトのビルドに必要なすべての要件を定義します。プロジェクト ファイルの内容は XML ファイル形式で整理されており、任意のテキスト エディターで開いて編集および表示できます。また、プロジェクト ファイルを論理的に表示して、適切に配置することもできます。

## CSPROJ ファイル形式 #

開発者は、[MSBuild XML スキーマ](https://msdn.microsoft.com/library/5dy88c2e.aspx) に従って、自分でプロジェクト ファイルを作成できます。プロジェクト ファイルのオープンで透過的な構造により、アプリケーション開発者は、プロジェクトのビルドおよびデプロイ方法を高度かつきめ細かく制御できます。このようなプロジェクト ファイルの内容は、相互に非常に明確な関係を持っています。次の図は、このようなプロジェクト ファイルの主要な要素とこれらの関係を示しています。

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

次のセクションでは、プロジェクト ファイルのファイル形式要素について詳しく説明します。

### プロジェクト要素 ###

[Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) 要素は、すべてのプロジェクト ファイルのルート要素です。プロジェクト ファイルの XML スキーマを識別し、ビルド プロセスのエントリ ポイントを指定する属性を含めることができます。

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### プロパティと条件

プロパティは、プロジェクトのビルドに必要な情報を表します。このようなプロパティは、[PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) 要素内で定義されます。これらのプロパティは、プロパティ要素名がプロパティ キーを定義し、要素の内容がプロパティ値を定義するキーと値のペアで構成されます。たとえば、ServerName および ConnectionString という名前のプロパティを定義して、静的サーバー名と接続文字列を格納できます。

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

要素を評価する基準を指定するために、要素を介して条件を指定できます。これは、以下に示すようにプロパティを定義するときに条件ワードで指定されます。

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

MSBuild は、このプロパティ定義を処理するときに、最初に **$(OutputRoot)** プロパティ値が使用可能かどうかを確認します。プロパティ値が空白の場合、つまり、ユーザーがこのプロパティに値を指定していない場合、条件は **true** と評価され、プロパティ値は **..\Publish\Out.** に設定されます。

### アイテムとアイテム グループ

プロジェクト ファイルは、実際には異なるファイル タイプであるビルド プロセスへの入力を定義します。 MSBuild 命名法では、これらの入力は Item 要素によって表され、[ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx) 要素内で定義されます。 **Property** 要素と同様に、**Item** 要素には好きな名前を付けることができます。ただし、**Include** 属性を指定して、項目が表すファイルまたはワイルドカードを識別する必要があります。

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### ターゲットとタスク

[Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) 要素は、個々のビルド命令 (またはタスク) を表します。 MSBuild には、定義済みのタスクが多数含まれています。例えば：

* **コピー** タスクは、ファイルを新しい場所にコピーします。
* **Csc** タスクは、Visual C# コンパイラを呼び出します。
* **Vbc** タスクは、Visual Basic コンパイラを呼び出します。
* **Exec** タスクは、指定されたプログラムを実行します。
* **Message** タスクはメッセージをロガーに書き込みます。

タスクは常に [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) 要素内に含まれている必要があります。 **Target** 要素は、順次実行される 1 つ以上のタスクのセットであり、プロジェクト ファイルには複数のターゲットを含めることができます。

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## 参考文献

* [プロジェクト ファイルについて - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

