{
  "date" : "2019-10-11",
  "keywords" :["bmpファイル","bmpファイル形式","bmpファイルとは","ファイル","bmp例","bmpファイル拡張子","拡張子","形式"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - 画像ファイル形式",
  "description":"BMP ファイル形式と,BMP ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# BMP ファイルとは? #

拡張子が .BMP のファイルは、ビットマップ デジタル画像の保存に使用されるビットマップ画像ファイルを表します。これらのイメージは、グラフィックス アダプターに依存せず、デバイスに依存しないビットマップ (DIB) ファイル形式とも呼ばれます。この独立性は、Microsoft Windows や Mac などの複数のプラットフォームでファイルを開く目的に役立ちます。 BMP ファイル形式は、データを 2 次元デジタル画像として、モノクロとさまざまな色深度のカラー形式の両方で保存できます。

## BMP ファイル形式の仕様 ##

デバイスに依存しないビットマップは、デバイスとアプリケーション間でビットマップを交換する際の補助として機能します。このファイル形式は継続的に進化しているため、ヘッダーに含まれる情報はビットマップのバージョンによって異なる場合があります。 1 つのビットマップ ファイルは、固定サイズの構造体と可変サイズの構造体を特定の順序で並べたものです。

ビットマップ ファイル内の構造は、次の順序で配置されます。


|構造|オプション|サイズ|目的
---|---|---|---|
|ファイル ヘッダー|いいえ|14|ビットマップ イメージ ファイルに関する一般的な情報を保存するには
|DIB ヘッダー|いいえ|固定サイズ|ビットマップ イメージに関する詳細情報を格納し、ピクセル形式を定義します。
|追加ビット マスク|はい|12 または 16 バイト|ピクセル フォーマットを定義するには
|カラー パレット|セミ オプション|可変サイズ|ビットマップ イメージ データで使用される色を定義するには
|Gap1|はい|可変サイズ|構造アライメント
|ピクセル配列|いいえ|可変サイズ|ピクセル形式は、DIB ヘッダーまたはエクストラ ビット マスクによって定義されます。
|Gap2|はい|可変サイズ|構造アライメント
|ICC カラー プロファイル|はい|可変サイズ|カラー マネージメント用のカラー プロファイルを定義するには

ビットマップ イメージがメモリに読み込まれると、Windows で GDI API を介して使用される DIB 構造になります。ファイル ヘッダーは、このデータ構造の一部ではありません。色は、明示的な RGB カラー定義の代わりに、現在参照されているパレットへのインデックスを構成する 16 ビット エントリで構成することもできます。これらのいくつか、特にヘッダーを詳しく見てみましょう。

### ビットマップ ファイル ヘッダー ###

ビットマップ ファイル ヘッダーは、ファイルの識別に使用される他のファイル ヘッダーに似ています。 BMP ファイル形式にはさまざまなバリエーションがあるため、BMP ファイル形式の最初の 2 バイトは文字 "B" であり、ASCII エンコーディングでは文字 "M" です。すべての整数値はリトル エンディアン形式で格納されます。

|オフセット hex|オフセット dec|サイズ|目的
---|---|---|---|
|00|0|2 バイト|BMP および DIB ファイルを識別するために使用されるヘッダー フィールドは、ASCII の BM と同じ 16 進数で 0x42 0x4D です。可能な値に従うことができます。* **BM** – Windows 3.1x、95、NT など * **BA** – OS/2 構造体ビットマップ配列 * **CI** – OS/2 構造体カラー アイコン * **CP** – OS/2 const カラー ポインター * **IC** – OS/2 構造体アイコン * **PT** – OS/2 ポインター
|02|2|4 バイト|BMP ファイルのサイズ (バイト単位)
|06|6|2 バイト|予約済み。実際の値は、画像を作成するアプリケーションによって異なります
|08|8|2 バイト|予約済み。実際の値は、画像を作成するアプリケーションによって異なります
|0A|10|4 バイト|ビットマップ画像データ (ピクセル配列) を見つけることができるバイトのオフセット、つまり開始アドレス。

#### DIBヘッダー（ビットマップ情報ヘッダー）####

イメージに関する詳細情報は、このヘッダーによって表されます。この情報に基づいて、画面に画像を表示するために使用されるアプリケーションが決定されます。このようなすべてのヘッダーには、サイズを指定する DWORD (32 ビット) フィールドが含まれているため、アプリケーションはイメージで使用されるヘッダーを簡単に判別できます。これは基本的に、DIB 形式がいくつかの拡張を経たという事実によるものです。以下は、リストされたフィールドを含む DIB ヘッダーです。

＃＃＃＃ カラーパレット ＃＃＃＃

BMP カラー パレットは、ディスプレイ デバイスのカラー パレットの各色の RGB 強度値を指定する構造体の配列です。ビットマップ データの各ピクセルには、カラー パレットへのインデックスとして使用される 1 つの値が格納されます。そのインデックスの要素に格納されている色情報は、そのピクセルの色を指定します。ビットマップ ファイルで使用できる色は、次のように異なります。

* 1、4、および 8 ビット - 常にカラー パレットが含まれていると予想される
* 16、24、および 32 ビット - カラー パレットを含まない
* 16 ビットおよび 32 ビットの BMP ファイル - カラー パレットの代わりにビットフィールド マスク値が含まれます

#### ピクセル ストレージ ####

ビットマップ ピクセルは、各行のサイズがパディングによって 4 バイト (32 ビット DWORD) の倍数に切り上げられる行にパックされたビットとして格納されます。画像のピクセルを格納するために必要なバイトの合計量は、ビット数をカウントするだけでは直接計算できません。パディングが含まれるため、各行のサイズを 4 バイトの倍数に切り上げる効果が必要です。行の長さを 4 バイトの倍数にするために、パディング バイト (必ずしも 0 ではない) を行の末尾に追加する必要があります。ピクセル配列がメモリに読み込まれるとき、各行は 4 の倍数であるメモリ アドレスで開始する必要があります。

イメージは、実際には、ピクセル配列の 32 ビット DWORD 表現によって記述されます。通常、ピクセルは「ボトムアップ」で保存されます。左下隅から始まり、左から右へ、次に行ごとに画像の下から上へと進みます。ピクセル形式とその意味は次のとおりです。

* 1 ピクセルあたり 1 ビット (1bpp) 形式は、2 つの異なる色 (例: 黒と白) をサポートします。
* ピクセルあたり 2 ビット (2bpp) 形式は、4 つの異なる色をサポートし、1 バイトあたり 4 ピクセルを格納します。左端のピクセルが最上位 2 ビットになります。各ピクセル値は、最大 4 色のテーブルへの 2 ビット インデックスです。
* ピクセルあたり 4 ビット (4bpp) 形式は、16 の異なる色をサポートし、1 バイトあたり 2 ピクセルを格納します。左端のピクセルは、より重要なニブルにあります。各ピクセル値は、最大 16 色のテーブルへの 4 ビット インデックスです。
* ピクセルあたり 8 ビット (8bpp) 形式は、256 の異なる色をサポートし、1 バイトあたり 1 ピクセルを格納します。各バイトは、最大 256 色のテーブルへのインデックスです。
* 16 ビット/ピクセル (16bpp) 形式は、65536 の異なる色をサポートし、2 バイトの WORD ごとに 1 ピクセルを格納します。各 WORD は、ピクセルのアルファ、赤、緑、および青のサンプルを定義できます。
* 24 ビット ピクセル (24bpp) 形式は、16,777,216 の異なる色をサポートし、3 バイトごとに 1 つのピクセル値を格納します。各ピクセル値は、ピクセルの赤、緑、青のサンプルを定義します (RGBAX 表記では 8.8.8.0.0)。具体的には、青、緑、赤の順に (各サンプルあたり 8 ビット)。
* 32 ビット/ピクセル (32bpp) 形式は、4,294,967,296 の異なる色をサポートし、4 バイトの DWORD ごとに 1 ピクセルを格納します。各 DWORD は、ピクセルのアルファ、赤、緑、および青のサンプルを定義できます。

## 参照 ##

* [Windows メタファイル形式](http://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [BMP ファイル形式](https://en.wikipedia.org/wiki/BMP_file_format)
