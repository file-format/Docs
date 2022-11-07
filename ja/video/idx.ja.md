{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - 高効率ビデオ コーデック",
  "description":"IDX ファイル形式と,IDX ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## .IDX オプション番号

IDX ファイルは、.sub (VobSub Subtitles) ファイル内の字幕のメタデータ情報のリストを指す字幕インデックス ファイルです。これは、ユーザーが DVD から字幕を抽出して SUB ファイルにダンプできるようにする VobSub ソフトウェア アプリケーションによって作成および使用されます。 IDX ファイルには、すべてのサブタイトルを指すために使用されるタイムスタンプとバイト オフセットが含まれています。 VobSub は常に、対応する SUB ファイルと共に IDX ファイルを作成します。

## IDX ファイル形式 - 詳細情報

IDX ファイルは、任意のテキスト エディターで開くことができるプレーン テキスト ファイルとして生成および保存されます。 IDXファイルには、画面に表示する字幕テキストの色、画面上の字幕テキストの位置などのパラメーターを読み取るためにメディアプレーヤーによって読み取られる情報が含まれています。

### IDX字幕設定

一般的な IDX ファイルは、このメタデータ情報をファイルの先頭に格納します。字幕設定は **#** で始まります。タイムスタンプと画像参照は、これらすべての字幕設定の後に追加され、**timestamp:** で始まります。

## IDX ファイル形式の例

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## IDXファイルの使い方

映画の Sub および IDX ファイルを取得している場合は、これらの字幕を作成された映画と一緒に再生できます。 VLC、GOM Player、PotPlayer、PowerDVD などの多くのアプリケーションには、これらの SUB および IDX ファイルをロードして、ムービーと一緒に再生する機能があります。ソフトウェア アプリケーションは、SUB および IDX 字幕ファイルを [.mkv](/video/mkv/) ファイルに埋め込むこともできます。

## IDX を SRT に変換する

[SRT](/video/srt/)(SubRipファイル形式)は、SubRipファイル形式で保存された簡易字幕ファイルです。 VobSub ファイル形式と比較して、より一般的に使用されます。したがって、SUB/IDX ファイルを SRT ファイル形式に変換したい場合、これを達成するために使用できるサードパーティ ツールが利用可能です。 SubtitleTools.com で入手できる SUB/IDX から SRT へのコンバーターは、SUB および IDX ファイルを入力として受け取り、これらの VobSub 字幕を SRT ファイルに変換するツールの 1 つです。

## 参考文献

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - ウィキ マルチメディア](https://wiki.multimedia.cx/index.php?title=VOBsub)

