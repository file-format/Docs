{
  "date" : "2020-01-11",
  "keywords" :[ "x ファイル", "x ファイル形式", "x ファイルとは", "ファイル", "x 例", "x ファイル拡張子","拡張子", "形式" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"X - DirectX 2.0 ファイル形式",
  "description":"DirectX X ファイル形式と,DirectX X ファイルを開いて作成できる API について学びます。",
  "linktitle" : "X",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2020-01-11"
}

## Xファイルとは何ですか?

拡張子が .x のファイルは、[DirectX](https://www.microsoft.com/en-us/download/search.aspx?q=directx) Microsoft DirectX 2.0 で導入された 3D グラフィックスのレガシー ファイル形式を指します。ゲームでの 3D グラフィックス レンダリングに使用され、メッシュ、テクスチャ、アニメーション、およびユーザー定義オブジェクトの構造を指定します。 Autodesk FBX ファイル形式がより新しい形式としてより適切に機能するため、2014 年以降は廃止されています。 X はテンプレート駆動型であり、使用に関する知識は一切ありません。

Microsoft DirectX および一般的なテキスト エディタを使用して、DirectX X ファイルを開くことができます。

## X ファイル形式

[X ファイル リファレンス](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-d3dx-x-file) には、使用される API 要素のリファレンス情報が含まれています。 DirectX .x ファイルを操作します。この形式は、データ テンプレートを介して高レベルのプリミティブを定義するために他のアプリケーションで使用される低レベルのデータ プリミティブを提供します。 DirectX 6.0 では、.x ファイルの読み取りと書き込みを可能にするインターフェイスとメソッドが導入されました。 DirectX 3.0 では、このファイル形式のバイナリ バージョンが導入されました。

DirectX 9 で定義されている [X ファイル フォーマット リファレンス](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format) には、.x のリファレンス情報が含まれています。バイナリおよびテキストエンコーディングのファイル。

### バイナリエンコーディング

[バイナリ形式](https://docs.microsoft.com/en-us/windows/win32/direct3d9/binary-encoding) は、テキスト形式のトークン化された表現として DirectX X 形式を定義します。これらのトークンは、文法構造を与えるためにスタンドアロンにすることも、必要なデータを提供する記録保持トークンにすることもできます。

#### ヘッダー

バイナリ ヘッダーは、次の定義を使用して読み書きできます。

```
#define XOFFILE_FORMAT_MAGIC \
  ((long)'x' + ((long)'o' << 8) + ((long)'f' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_VERSION \
  ((long)'0' + ((long)'3' << 8) + ((long)'0' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_BINARY \
  ((long)'b' + ((long)'i' << 8) + ((long)'n' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_TEXT   \
  ((long)'t' + ((long)'x' << 8) + ((long)'t' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_COMPRESSED \
  ((long)'c' + ((long)'m' << 8) + ((long)'p' << 16) + ((long)' ' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_32 \
  ((long)'0' + ((long)'0' << 8) + ((long)'3' << 16) + ((long)'2' << 24))

#define XOFFILE_FORMAT_FLOAT_BITS_64 \
  ((long)'0' + ((long)'0' << 8) + ((long)'6' << 16) + ((long)'4' << 24))
```

### テキストエンコーディング

DirectX .x ファイルは、ファイルの使用方法に依存せず、どのアプリケーションにも固有ではありません。このテンプレート主導のアプローチにより、.x ファイル形式を任意のクライアント アプリケーションで使用できます。


#### ヘッダー

可変長ヘッダーは必須であり、データ ストリームの先頭にある必要があります。ヘッダーには次のデータが含まれます。

|タイプ |サブタイプ |サイズ |内容 |内容の意味|
---|---|---|---|---|
|マジックナンバー (必須)| | | 4 バイト |xof |
|バージョン番号 (必須) |メジャー番号 |2 バイト |03 |メジャー バージョン 3|
| | |マイナー番号 |2 バイト |02 |マイナー バージョン 2|
|フォーマットタイプ (必須)| |4 バイト |"txt " |テキスト ファイル|
| | | | | | |「ビン」|バイナリ ファイル|
| | | | | | |"tzip"| MSZip 圧縮テキスト ファイル|
| | | | | | |"bzip"| MSZip 圧縮バイナリ ファイル|
|フロートサイズ (必須)| |4バイト| 0064| 64 ビット浮動小数点数|
| | | | | | |0032 |32 ビット浮動小数点数|


## 参考文献

* [X ファイル レガシー](https://docs.microsoft.com/en-us/windows/win32/direct3d9/x-files--legacy-)
* [DirectX 9 ファイル フォーマット リファレンス](https://docs.microsoft.com/en-us/windows/win32/direct3d9/dx9-graphics-reference-x-file-format)

