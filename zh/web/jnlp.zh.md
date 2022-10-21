---
date: 2022-07-30
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: "JNLP 文件格式 - 什么是 JNP 文件？"
linktitle: "JNLP"
description: "了解 JNLP 文件格式和可以创建和打开 JNLP 文件的 API。"
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## 什么是一 .jnlp 文件？

JNLP 文件是一个 Java Web Start (JWS) 文件，其中包含用于通过网络启动 Java 程序的 XML 信息。它以 Java 网络启动协议 (JNLP) 格式保存。它由 Java Web Start (JWS) 技术使用，该技术是一种应用程序部署技术，用于下载和运行应用程序。 JNLP 文件包含在本地机器上下载和启动程序的服务器的远程地址。

## JNLP 文件格式 - 更多信息

JNLP 文件保存为 **[XML](/zh/web/xml/)** 文件，这些文件以人类可读的文本格式存储。 XML 文件包含用于通过网络启动和执行 Java 应用程序的信息。 JWS 允许您通过单击网页链接来启动应用程序。如果应用程序尚未下载到用户计算机上，则会下载该应用程序。

Oracle 在 Java 平台标准版 (JSE) 9 的发布中弃用了 JWS。这样，JNLP 文件不再受支持。

### 如何打开 JNLP 文件？

可以**打开 JNLP 文件**的应用程序包括 **Microsoft Visual Studio Code**、**Notepad**、**Notepad++**、**Oracle Java Web Start**、**Karakun OpenWebStart** 和 * *GitHub 原子**。

### JNLP 文件示例

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
**用法**

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
## 如何运行 JNLP 文件？

随着 JWS 的弃用，基于 JWS 技术开发的应用程序无法使用最新版本的 Java 运行。但是，这些基于 JNLP 的程序可以使用 OpenWebStart 运行，OpenWebStart 是 Java Web Start 技术的开源重新实现。它与最新版本的 Java 并行安装，并提供 Java Web Start 和 JNLP 标准最常用的功能。

## 参考 ＃＃

* [什么是 Java Web Start 及其启动方式？](https://www.java.com/en/download/help/java_webstart.html)
* [使用最新版本的 Java 运行 JNLP](https://openwebstart.com/)
* [Java Web Start - 维基百科](https://en.wikipedia.org/wiki/Java_Web_Start)

