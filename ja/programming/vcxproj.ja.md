{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "ファイル", "拡張子", "ファイル形式", "Visual C++ プロジェクト", "プログラミング ガイド" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"VCXPROJ ファイル形式と,VCXPROJ ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## .VCXPROJ ファイルとは?

拡張子が .vcxproj のファイルは、[C++](/programming/cpp/) プロジェクト情報を格納する Microsoft Visual C++ プロジェクト ファイルです。これには、最終的な出力をコンパイルおよびビルドするために MSBuild プロジェクト システムによって使用される情報が含まれています。 Visual C++ プロジェクトの VCXPROJ は、.NET プロジェクトの [CSPROJ](/programming/csproj/) と同じです。 VCXPROJ ファイルにはコードは含まれませんが、プロジェクトをビルドするためにプロジェクト用に定義されたすべてのクラス、ターゲット、およびプロパティを参照します。これらは、プレーン テキスト エディターまたはできれば Microsoft Visual Studio IDE で開くことができます。


## VCXPROJ ファイル形式 - 詳細情報

VCXPROJ ファイルは、[XML](/web/xml/) ファイル形式で作成されたテキスト ファイルです。これらは任意のテキスト エディターで開くことができますが、これらのファイルを開いて編集するには、Microsoft Visual Studio IDE を使用することを強くお勧めします。これらは手動編集用に設計されていません。間違いにより、IDE がクラッシュしたり、予期しない方法で動作したりする可能性があります。

サンプル VCXPROJ ファイルの内容は次のとおりです。

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### VCXPROJ ファイルの要素

典型的な VCXPROJ ファイルには、上記の XML の例に見られるように、多数の要素が含まれています。 Microsoft の [VCXPROJ 構造](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) では、各ファイル要素が詳細に説明されており、参照できます。開発者の視点から。

#### プロジェクト要素

これは、VCXPROJ ファイルのルート ノードです。 MSBuild は、この要素を使用して、コンパイルのビルド バージョンと既定のターゲットを読み取ります。

#### ProjectConfigurations ItemGroup 要素

これには、ビルド方法 (デバッグまたはリリース)、32 ビットまたは 64 ビットのコンパイル、最適化オプションなどを含むプロジェクト構成情報が含まれています。このグループの情報は、プロジェクトをロードするために IDE によって使用されます。

#### ProjectConfiguration 要素

VCXPROJ ファイルの ProjectConfiguration 要素には、プロジェクトが読み込まれるビルドとプラットフォームに関する情報が含まれています。その名前は、「$(Configuration)|$(Platform)」の形式に従う必要があります。

#### グローバル PropertyGroup 要素

このセクションには、次のようなプロジェクト レベルの情報を提供する設定が含まれています。

* プロジェクトガイド
* ルート名前空間
* ApplicationType または ApplicationTypeRevision


## 参考文献

* [VCXPROJ 構造 - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [C++ プロジェクト ファイル](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

