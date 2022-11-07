---
date: 2021-07-05
keywords: ssp,.ssp,ssp ファイル形式,ssp ファイルの開き方,Scala Server Page
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SSP - Scala Server Pages ファイル形式
linktitle: SSP
description: "SSP ファイル形式とは何か,および SSP ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    identifier: "web-ssp"
    parent: "web"
lastmod: 2021-09-30
---

## .SSP オプション番号

拡張子が .ssp のファイルは、プレーンな HTML のみではなく、式用の Scala コードで作成された Web ページです。 HTML と Scala の組み合わせを使用して、サーバー サイド スクリプトとして機能します。これらのファイルはサーバー上にあり、ユーザーに提供される静的 Web ページを作成するために使用されます。 Scala 自体は汎用プログラミング言語であり、その構文は Velocity、JSP、または Erb を使用したことがあるユーザーにはなじみ深いものです。 SSP ファイルは、テキストとマークアップを生成するための Scala ベースのテンプレート エンジンである [Scalate](https://scalate.github.io/scalate/) を使用して分析および評価できます。

## SSP ファイル形式 - 詳細情報

SSP ファイルはプレーン テキスト ファイルで保存され、Scalate を使用して評価できます。 Ssp テンプレートは、多くの場合 HTML ドキュメントであるプレーン テキストで構成されます。これには、レンダリング エンジンがドキュメントのさまざまな部分を動的にレンダリングする Ssp タグが埋め込まれています。タグは <% ... %> および ${ ... } シーケンスで開始および終了し、これらの外側にあるものはすべてリテラル テキストと見なされます。

### SSPの例

次の例は、レンダリング エンジンによってレンダリングされたときの SSP コードとその出力を示しています。

```PHP
<p>
  <%= List("hi", "there", "reader!").mkString(" ") %>
  ${ "yo "+(3+4) }
</p>
```
出力は次のとおりです。
```
<p>
  hi there reader!
  yo 7
</p>
```

## 参考文献

- [SSP リファレンス](https://scalate.github.io/scalate/documentation/ssp-reference.html)

