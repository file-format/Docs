{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BIF ファイル - Ventana 全体のスライド画像形式",
  "description":"BIF ファイル形式と,BIF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## .BIF ファイルとは?

BIF ファイルは、スライド標本画像を含むラスター画像ファイルです。これは、スライド表示アプリケーションによって単一の合成画像に結合される複数の TIFF 画像で構成されます。 BIF ファイルは、Ventana Medical システムのデジタル スライド スキャナによって作成され、[TIFF](/ja/image/tiff/) v 6.0 定義の BigTIFF バリアントに完全に準拠しています。

## BIF ファイル形式

BIF ファイルはバイナリ イメージ ファイルとして保存され、最大 200,000 x 200,000 ピクセルで構成されます。これにより、ファイル サイズが大きくなり、TIF 標準で定義された 32 ビット ファイル ポインターによって課される 4 GB のサイズ制限を破る可能性があります。ただし、64 ビットのファイル ポインターでは、このファイル サイズの壁は、TIFF 標準の BigTIFF バリアントによって克服されます。

### BIF ファイルを使用するのは誰ですか?

BIF ファイルは、デジタル スライド スキャナがスライド標本のデジタル コピーをスキャンして作成するために使用されます。病理学者であれば、これらの BIF ファイルをスライド表示アプリケーションで開くことができます。優れた詳細レベルと高解像度データにより、スライド画像をズームインおよびズームアウトして、標本のセクションを多かれ少なかれ詳細に表示できます。これらのファイルにある [XML](/ja/web/xml/) メタデータ ファイルは、画像を組み合わせる方法と、ファイルのサムネイルとして使用する画像を定義します。

## BIF ファイルを開く方法?

次の方法で BIF ファイルを開くことができます。

* OpenSlide (クロスプラットフォーム)
* ImageJ (クロスプラットフォーム)
* NetScope ビューア (Windows)

## 参照 ##

* [Roche Digital Pathology BIF ホワイトペーパー](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

