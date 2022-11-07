{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - チャンネル定義フォーマット",
  "description" :"CDF ファイルとは何か,および CDF ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## .CDF ファイルとは?

拡張子が .cdf のファイルは、頻繁な更新を「チャネル」として公開するために使用された XLM ベースの情報配布ファイル形式です。情報は任意の Web サーバーから公開され、Web ブラウザーなどの互換性のある受信プログラムを備えたコンピューターに自動的に配信されます。ユーザーはアクティブなチャネルに登録し、スケジュールされた更新をデスクトップに配信します。
CDF ファイルは、以前は Microsoft の Active Channel、Active Desktop、および Smart Offline Favorites テクノロジと組み合わせて使用されていました。

## CDF ファイル形式

CDF ファイルは、情報交換用の一般的な Web ファイル形式である XML ファイルとして保存されます。 CDF ファイル形式は現在では古い形式であり、広く採用されることはありませんでした。これに比べてネットスケープのRSSの方が有名で広く使われていました。

### CDF ファイル形式の例

以下は、CDF ファイル形式の一般的な例です。

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://ドメイン/フォルダー/"
LASTMOD="1998-11-05T22:12"
PRECACHE="はい"
レベル="0">
<TITLE>チャンネルのタイトル</TITLE>
<ABSTRACT>チャンネル内容のあらすじ。</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="はい"
レベル="1">
<TITLE>ページ 2 のタイトル</TITLE>
<ABSTRACT>Page Two の内容のあらすじ。</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## 参考文献

* [チャネル定義形式 - ウィキペディアによる](https://en.wikipedia.org/wiki/Channel_Definition_Format)

