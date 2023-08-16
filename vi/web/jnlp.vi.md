---
date: 2022-07-30
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Định dạng tệp JNLP - Tệp JNP là gì?
linktitle: JNLP
description: "Tìm hiểu về định dạng tệp JNLP và các API có thể tạo và mở tệp JNLP."
menu:
  docs:
    parent: "web"
lastmod: 2022-07-30
---

## Tệp JNLP là gì?

Tệp JNLP là tệp Java Web Start (JWS) chứa thông tin XML để khởi chạy chương trình Java qua mạng. Nó được lưu ở định dạng Java Network Launching Protocol (JNLP). Nó được sử dụng bởi công nghệ Java Web Start (JWS), một công nghệ triển khai ứng dụng để tải xuống và chạy một ứng dụng. Tệp JNLP chứa địa chỉ từ xa của máy chủ mà từ đó chương trình được tải xuống và khởi chạy trên máy cục bộ.

## Định dạng tệp JNLP - Thông tin khác

Các tệp JNLP được lưu dưới dạng tệp **[XML](/vi/web/xml/)** được lưu trữ ở định dạng văn bản mà con người có thể đọc được. Tệp XML có thông tin được sử dụng để khởi chạy và thực thi ứng dụng Java qua mạng. JWS cho phép bạn khởi chạy các ứng dụng bằng cách nhấp vào liên kết trang web. Ứng dụng được tải xuống trong trường hợp nó chưa được tải xuống trên máy tính của người dùng.

Oracle đã ngừng sử dụng JWS khi phát hành Java Platform Standard Edition (JSE) 9. Với điều này, các tệp JNLP không còn được hỗ trợ nữa.

### Cách mở tệp JNLP?

Các ứng dụng có thể **mở tệp JNLP** bao gồm **Microsoft Visual Studio Code**, **Notepad**, **Notepad++**, **Oracle Java Web Start**, **Karakun OpenWebStart** và * *GitHub Atom**.

### Ví dụ về tệp JNLP

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
**Cách sử dụng**

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
## Làm cách nào để chạy các tệp JNLP?

Với việc ngừng sử dụng JWS, các ứng dụng được phát triển dựa trên công nghệ JWS không thể chạy với phiên bản Java mới nhất. Tuy nhiên, các chương trình dựa trên JNLP này có thể được chạy bằng OpenWebStart, đây là sự triển khai lại mã nguồn mở của công nghệ Java Web Start. Nó cài đặt song song với phiên bản Java mới nhất và cung cấp các tính năng được sử dụng phổ biến nhất của Java Web Start và tiêu chuẩn JNLP.

## Người giới thiệu ##

* [Java Web Start là gì và nó được khởi chạy như thế nào?](https://www.java.com/en/download/help/java_webstart.html)
* [Chạy JNLP với Phiên bản Java mới nhất](https://openwebstart.com/)
* [Java Web Start - Wikipedia](https://en.wikipedia.org/wiki/Java_Web_Start)

