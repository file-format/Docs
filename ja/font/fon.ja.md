{
  "date" : "2020-08-20",
  "keywords" :[ "fon ファイル", "fon ファイル形式", "fon ファイルとは", "ファイル", "fon の例", "fon ファイルの拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - フォント ライブラリ ファイル",
  "description":"FON ファイル形式と,FON ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## .FON オプション番号

拡張子が .fon のファイルは、Microsoft Windows 3.x フォント ライブラリであり、実際には実行可能ファイルですが、名前が .fon に変更されています。それ自体が [.fnt](/font/fnt/) ファイルの集まりであり、アプリケーションがシステム フォントにアクセスする際に参照します。そのため、リソース ファイルとして機能します。 Microsoft Windows Font View アプリケーションを使用して Windows OS で開くことができます。

## FONファイル形式

FON ファイルにはフォント リソースが含まれ、リソース (.res) ファイル形式があります。 .res ファイル形式は、ファイル ヘッダーとデータ セクションの仕様を指定します。 .fnt は、リソース ファイルに含まれるリソース データ ファイルでもあります。 FON ファイルにはバイナリ ファイル形式があり、アプリケーション/オクテット ストリーム MIME タイプがあります。

フォント リソースは、他の種類のリソースとは異なり、アプリケーションのリソースに追加されません。代わりに、それらは EXE ファイルに追加され、名前が .fon ファイルに変更されるため、アプリケーションではなくライブラリ ファイルが生成されます。複数の個々のフォントがフォント グループのコンポーネントを構成し、各グループはリソース グループ構造に従います。フォント リソースは、これらのリソース グループ構造を使用します。グループ ヘッダーには、グループから特定のフォントにアクセスするために必要なすべての情報が含まれています。フォント コンポーネント リソースの形式は次のとおりです。
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/font/fnt/) file)
```
1 つの .rc リソース ファイルに複数のリソース宣言を含めることができます。フォント グループは、リソース ファイル内の任意の場所に配置でき、連続している必要はありません。 .RES ファイルを作成するプログラムでは、FONTDIR の手動入力を追加する必要があります。以下は、グループ ヘッダーの構造です。

```
【通常のリソースヘッダ(type=7)】

WORD NumberOfFonts; // .RES ファイルの総数
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfSize;
char dfCopyright[60];
WORD dfType;
WORD dfPoints;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfItalic;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORD dfWeight;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
WORD dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORD dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserved;
char szDeviceName[];
char szFaceName[];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

