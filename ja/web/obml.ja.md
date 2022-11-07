{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OBML ファイル形式 - Opera Mini に保存された Web ページ ファイル",
  "description" :"OBML ファイルとは何か,および OBML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## .OBML オプション番号

OBML (Opera Binary Markup Language) ファイルは、Opera Mini モバイル Web ブラウザーによって保存された Web ページのオフライン バージョンです。 [HTML](/web/html/) ファイルの自己完結型のコンパクト バージョンであり、オフライン時に特定のデバイスで表示するページのすべての要素が含まれています。 OBML ファイル形式はいくつかのバージョンにアップグレードされ、OBML15 と OBML16 が広く使用されています。考慮すべき重要な点は、Opera Mini の各バージョンは 1 つの OBML フォーマットとしか互換性がないということです。したがって、Opera Mini をアップグレードすると、以前に保存したページが読めるようになります。 OBML ファイルは、HTML および [PDF](/pdf/) に変換できます。

## OBML ファイル形式

OBML ファイル形式は Opera 独自のファイル形式で保存され、そのファイル形式の仕様は公開されていません。ただし、[OMBL 形式](https://github.com/grawity/obml-parser/blob/master/obml.md) をリバース エンジニアリングして、次のように構造を解読しました。

### OBML データ型

リバース エンジニアリングの結果によると、OBML は次のプリミティブ型を使用します。

* `byte` – 符号なし整数 (1 バイト)
* `short` – 符号付き整数 (2 バイト、ビッグエンディアン)
* `medium` – 符号付き整数 (3 バイト、ビッグエンディアン)
 * `blob` – { length: short, data: byte[length] }
* `char` – ASCII 文字を含むバイト
* `string` – UTF-8 でエンコードされたテキストを含む blob

### OBML ヘッダー

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## 参考文献

* [OMBL形式](https://github.com/grawity/obml-parser/blob/master/obml.md)

