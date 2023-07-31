{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"SLN ファイル形式と,SLN ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## SLN ファイルとは?
拡張子が .SLN のファイルは、プロジェクトの編成に関する情報をソリューション ファイルに保持する **Visual Studio ソリューション** ファイルを表します。このようなソリューション ファイルの内容は、ファイル内にプレーン テキストで記述されており、任意のテキスト エディターでファイルを開いて確認/編集できます。ソリューション ファイルに含まれる情報は永続的なままであり、[projects](/programming/csproj/) などのソリューションに関連する情報やその他の必要な情報を読み込むために使用されます。ソリューション ファイルによって参照されるプロジェクト ファイルには、そのプロジェクトの項目を階層に設定するための環境を有効にするための追加情報が含まれています。 .sln ファイルにはデータは保存されませんが、必要に応じてプロジェクト情報を .sln ファイルに書き込むことができます。

## **SLN バージョン履歴** ##

ソリューション形式のバージョンは、Microsoft Visual Studio ソリューションごとに時間の経過とともに進化してきました。これらの詳細は以下の通りです。


|Visual Studio バージョン|ソリューション フォーマット バージョン
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **ソリューション ファイルの内容** ###

ソリューション ファイルは、プロジェクトを読み込むために環境によって読み取られるいくつかのセクションで構成されます。サンプルの .sln ファイルの内容は次のとおりです。

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **プロジェクト宣言** ###

ソリューション ファイルには、複数のプロジェクト宣言と、異なるプロジェクト タイプの宣言を含めることができます。たとえば、1 つのソリューション ファイルに CSharp と VB.NET プロジェクトを含めることができます。これらのタイプは、[Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs) を使用するソリューションで区別されます。上記のプロジェクト宣言は、明確な理解のために次のように一般化できます。

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID は、プロジェクトの種類ごとに一意であり、プロジェクトの種類を識別するためにソリューション リーダーによって使用されます。この場合、F184B08F-C81C-45F6-A57F-5ABD9991F28F は、VB.NET プロジェクトであることを示しています。

`プロジェクト GUID:` ソリューション内の他のプロジェクトと区別するプロジェクトの一意の GUID。ソリューション内のプロジェクトの一意の ID により、ソリューション内の他のプロジェクトがそれにアクセスできるようになります。

.sln ファイルのプロジェクト セクションに含まれる情報に基づいて、環境は各プロジェクト ファイルを読み込みます。その後、プロジェクト自体が、プロジェクト階層にデータを入力し、ネストされたプロジェクトをロードします。ソリューションに加えられた変更は、プロジェクトを保存または閉じるときにソリューション ファイルに保存されます。

## Visual Studio ソリューション VS プロジェクト

**プロジェクト:** 論理的には、Visual Studio を使用してアプリまたはソフトウェアの作成を開始するときは、新しいプロジェクトを開始します。プロジェクトには、ソース コード、アイコン、画像、データ ファイルなど、実行可能なアプリ、Web サイト、またはライブラリにコンパイルされる必要なすべてのファイルが含まれています。

**ソリューション:** ソリューションには 1 つ以上のプロジェクトが含まれます。したがって、このソリューションは、Visual Studio プロジェクトのコンテナーのようなものです。論理的に言えば、Web サイト、デスクトップ アプリ、安らかなサービス、モバイル アプリを含む、ビジネスのための完全なソリューションを手に入れたいと考えている人がいると言えます。

### **参考文献** ###

* [ソリューション ファイル - MSDN 提供](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [プロジェクト タイプ GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

