---
date: 2022-05-09
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Định dạng tệp PYD - Mô-đun động Python
linktitle: PYD
description: "Tìm hiểu về định dạng tệp PYD và các API có thể tạo và mở tệp PYD."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## Tệp PYD là gì?

Tệp PYD là một thư viện liên kết động được viết bằng Python có thể chạy bằng mã Python khác trong thời gian chạy. Nó chứa một hoặc nhiều mô-đun Python tạo điều kiện tái sử dụng mã và cung cấp kiến trúc mô-đun để viết ứng dụng. Các tệp PYD có thể được tạo và lưu với phần mở rộng .pyd, ví dụ: helloworld.pyd. Các nhà phát triển ứng dụng có thể sử dụng câu lệnh nhập để đưa các mô-đun PYD vào ứng dụng của họ. Các tệp PYD có thể được mở bằng Python Software Foundation Python có sẵn cho Windows, Mac và Linux OS.

## Định dạng tệp PYD - Thông tin khác

Các tệp PYD được viết bằng ngôn ngữ lập trình Python và được tạo bằng cách biên dịch mã Python.

## Sự khác biệt giữa định dạng tệp PY và PYD

Tệp [PY](/vi/programming/py/) chứa mã nguồn được thực thi như vốn có và không thể được đưa vào dưới dạng mã có thể sử dụng lại trong các ứng dụng Python khác. Tuy nhiên, tệp PYD là một thư viện được liên kết động sẽ được sử dụng trên hệ điều hành Windows.

## Làm cách nào để tạo tệp PYD?

Có thể tạo tệp PYD bằng cách tạo mô-đun có tên, ví dụ: exmaple.pyd. Mô-đun này sẽ chứa tất cả các chức năng dưới dạng một hoặc nhiều chức năng, ví dụ: PyMod_example(). Khi chương trình bao gồm thư viện này và gọi nó, nó có thể được thực hiện bằng cách nhập mô-đun và hàm PyMod_example() sẽ chạy.

## Người giới thiệu ##

* [Tạo tiện ích mở rộng Python trong C/C++](https://sebsauvage.net/python/mingw.html)
* [Python (ngôn ngữ lập trình) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

