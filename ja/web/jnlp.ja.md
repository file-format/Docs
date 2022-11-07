---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: JNLP ファイル形式 - JNP ファイルとは?
linktitle: JNLP
description: "JNLP ファイル形式と,JNLP ファイルを作成して開くことができる API について学びます。"
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## .JNLP オプション番号

JNLP ファイルは、Java プログラムをネットワーク経由で起動するための XML 情報を含む Java Web Start (JWS) ファイルです。 Java Network Launching Protocol (JNLP) 形式で保存されます。アプリケーションをダウンロードして実行するためのアプリケーション展開テクノロジである Java Web Start (JWS) テクノロジによって使用されます。 JNLP ファイルには、プログラムがダウンロードされ、ローカル マシンで起動されるサーバーのリモート アドレスが含まれています。

## JNLP ファイル形式 - 詳細情報

JNLP ファイルは **[XML](/web/xml/)** ファイルとして保存され、人間が判読できるテキスト形式で保存されます。 XML ファイルには、ネットワーク経由で Java アプリケーションを起動および実行するために使用される情報が含まれています。 JWS を使用すると、Web ページのリンクをクリックしてアプリケーションを起動できます。アプリケーションがユーザーのコンピューターにまだダウンロードされていない場合は、アプリケーションがダウンロードされます。

Oracle は、Java Platform Standard Edition (JSE) 9 のリリースで JWS を非推奨にしました。これにより、JNLP ファイルはサポートされなくなりました。

### JNLP ファイルを開くには?

**JNLP ファイルを開く**ことができるアプリケーションには、**Microsoft Visual Studio Code**、**メモ帳**、**メモ帳++**、**Oracle Java Web Start**、**Karakun OpenWebStart**、* などがあります。 *GitHub アトム**。

### JNLP ファイルの例

```
<jnlp spec="1.0" codebase="http://localhost/jws" href="Notepad.jnlp">
   <information>
      <title>Notepad Demo</title>
      <vendor>Sun Microsystems, Inc.</vendor>
   </information>
   <resources>
      <property name="jnlp.publish-url" value="$$context/publish"/>
      <j2se version="1.3+" href="http://java.sun.com/products/autodl/j2se"/>
      <jar href="Notepad.jar"/>
   </resources>
   <application-desc main-class="Notepad"/>
</jnlp>
```
**使用法**

```
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.0 Transitional//EN">
<HTML>
<HEAD>
   <TITLE>Java Web Start Demo</TTLE>    
</HEAD>
<BODY>

<H1>Java Web Start Demo</H1>
<a href="Notepad.jnlp">Lanuch Notepad Application</a>
This link is to the Notepad.jnlp file.
</BODY>
</HTML>
```
## JNLP ファイルを実行するには?

JWS の非推奨により、JWS テクノロジに基づいて開発されたアプリケーションは、最新バージョンの Java で実行できません。ただし、これらの JNLP ベースのプログラムは、Java Web Start テクノロジのオープン ソース再実装である OpenWebStart を使用して実行できます。 Java の最新バージョンと並行してインストールされ、Java Web Start および JNLP 標準の最も一般的に使用される機能を提供します。

## 参照 ##

* [Java Web Start とは? 起動方法](https://www.java.com/ja/download/help/java_webstart.html)
* [最新バージョンの Java で JNLP を実行](https://openwebstart.com/)
* [Java Web Start - ウィキペディア](https://en.wikipedia.org/wiki/Java_Web_Start)

