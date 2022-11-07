{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M4S ファイル - M4S ファイルとは?",
  "description":"M4S ファイル形式と,M4S ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## M4Sファイルとは何ですか?

M4S ファイルは、**MPEG-DASH** ストリーミング技術を使用してインターネット経由でストリーミングされるビデオの小さなセグメントです。これには、バイナリ データ形式のビデオ セグメントが含まれます。受信アプリケーション (通常は Web ブラウザーまたはメディア プレーヤー) は、これらのセグメントを受信順に再生します。最初の M4S セグメントは、そこに含まれる初期化データによって識別されます。 **要約**では、M4S ファイルは完全なファイルの小さな個々のメディア セグメントです。

## M4S ファイル形式

M4S ファイルは、[ISO ベース メディア ファイル (ISOBMFF) 形式](https://www.w3.org/TR/mse-byte-stream-format-isobmff/) に基づいています。大きなファイルのこれらの小さなセグメントは、HTTP 経由で個別にダウンロードできます。したがって、大きな [MP4](/video/mp4/) ムービー ファイルがある場合、M4S セグメント ファイルとしてセグメント化することにより、MPEG-DASH (Dynamic Adaptive Streaming over HTTP) 技術を使用してストリーミングできます。この大きなムービー ファイルを M4S としてディスクにダウンロードすると、複数の M4S ファイルがダウンロードされます。これらの .m4s セグメントがすべて連結されると、完全な再生可能なファイルが生成されます。ファイルで最初の初期化セグメントも利用できない限り、メディア プレーヤーはファイルを再生できません。

## MPEG-DASH ストリーミングについて

MPEG-DASH は、アダプティブ ビットレート ストリーミング技術を使用して、インターネット経由で高品質のメディア コンテンツをストリーミングできるようにします。これは、HTTP 経由でストリーミングされる一連の小さなセグメントにコンテンツを分割することによって行われます。映画、ポッドキャスト、スポーツ イベントの生放送などの大きなメディア ファイルは、この方法でストリーミングできます。これらのセグメントは、異なるビット レートでエンコードされます。 MPEG-DASH 対応のメディア プレーヤーは、ビット レート適応アルゴリズムを使用して、最も高いビット レートのセグメントを自動的に選択します。これにより、再生中のイベントの停止または再バッファリングが回避されます。

### M4S ファイル用のオープンソース API

M4S ファイルの読み取りと変換に使用できるオープン ソース API が利用可能です。

* [libdash](https://github.com/bitmovin/libdash) - M4S ファイル用の .NET API
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - M4S ファイルの Javascript クライアント
* [Dash ファイルを作成するための Go ライブラリ](https://github.com/zencoder/go-dash)

### M4S を MP4 に変換するオープンソース API

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## 参照 ###

* [ISO ベース メディア ファイル (ISOBMFF) 形式](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [HTTP 経由の動的適応ストリーミング - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

