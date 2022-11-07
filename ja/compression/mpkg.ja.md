{
  "date" : "2019-10-11",
  "keywords" :["mpkgファイル","mpkgファイル形式","mpkgファイルとは","ファイル","mpkg例","mpkgファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPKG ファイル形式 - メタ パッケージ ファイル",
  "description":"MPKG ファイル形式と,MPKG ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## .MPKG オプション番号

拡張子が .mpkg のファイルは、主に MacOS オペレーティング システムで見られるアーカイブ インストーラー ファイルです。アプリケーションの必要なすべてのインストール ファイルが含まれており、関連ファイルを個別に保持する必要はありません。 1 つの MPKG ファイルには、他のファイルに加えて、インストール ファイルの 1 つとしてパッケージ ファイル [PKG](/compression/pkg/) を含めることができます。 MPKG ファイルは、一般的なソフトウェアでは開くことができず、Apple インストーラーを使用して MacOS で自動的に実行されます。

## MPKG ファイル形式

MPKG ファイルには、含まれる複数のパッケージのインストールに必要なさまざまな種類のファイルが含まれています。これは、サンプル MPKG ファイルのツリー構造である下の画像から見ることができます。このツリー構造は、MacOS ターミナルで「tree」コマンドを使用してエクスポートされます。

{{< figure src="../mpkg.png" alt="MPKG ファイル形式" >}}

画像内のさまざまな要素の説明は次のとおりです。

`Packages Directory` - pkg ファイルのリスト、つまりサブパッケージのリストを保存します
`Resources Directory` - ローカライズされたリソースやイメージ、RTF ドキュメント、PDF ドキュメントなど、pkg によって使用されるリソースを保存します。
`Distribution.dist file` - インストールするサブパッケージやランタイム スクリプトなどの情報を含む xml ドキュメント

MPKG ファイルのサンプル XML ファイルは、関連するサブパッケージに応じて次のようになります。

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - インストールするサブパッケージです。 pkg形式のBundle構造のディレクトリです。 Contents サブディレクトリが含まれています。

## 参考文献

* [OSX フラット パッケージ](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG パッケージ マネージャー](https://github.com/puellavulnerata/mpkg)

