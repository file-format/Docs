{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LRC ファイル形式 - LRC ファイルとは?",
  "description":"LRC Lyric ファイルと,LRC ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## .LRC オプション番号

LRC ファイルは、オーディオ ソングの歌詞を含むテキスト ベースの歌詞ファイルです。パソコンの音楽プレイヤーやオーディオプレイヤーソフトでオーディオソングを再生すると、並行してLRCファイルが読み込まれ、時間とともに表示されます。 LRC ファイルには、曲の再生中に歌詞を表示するためのキュー ポイントが含まれています。通常、LRC ファイルは対応するオーディオ ファイルと同じ名前 (audio.mp3 や audio.lrc など) です。 LRC ファイルは、[SRT](/video/srt/) などの字幕ファイルに似ています。

## LRC ファイル形式 - 詳細情報

LRC 歌詞形式ファイルはプレーン テキスト ファイルとして保存され、テキスト ファイルで開いて編集することができます。 LRC ファイルの内容には、歌詞テキストを表示するための色情報が含まれています。

## LRCフォーマット

時間をかけて開発されたLRCファイルには複数の形式があります。これらは

### シンプルなLRCフォーマット

ライン タイム タグの形式は [mm:ss.xx] で、mm は分、ss は秒、xx は 100 分の 1 秒です。

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### シンプルフォーマット拡張

M:男性、F:女性、D:デュエットで歌詞の性別を変更・指定できる機能を搭載。

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### 拡張 LRC 形式

拡張 LRC 形式は、Simple LRC 形式の拡張バージョンです。 Word Time Tag を次の形式で追加します。<mm:ss.xx>前の単語の最後に。

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## 参考文献

* [LRC 歌詞ファイル形式 - ウィキペディア](https://en.wikipedia.org/wiki/LRC_(file_format))

