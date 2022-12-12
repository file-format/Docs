---
date: 2022-01-31
keywords: stp, .stp, định dạng file stp, cách mở file stp, đuôi .stp, đuôi stp
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Định dạng tệp STP
linktitle: STP
description: "Tìm hiểu về định dạng tệp STP và các API có thể tạo và mở tệp STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## Tệp STP là gì?

Tệp STP là tệp CAD 3D được sử dụng để trao đổi dữ liệu sản phẩm giữa các ứng dụng CAD và CAM. Nó chứa thông tin về các đối tượng 3D và được lưu tương tự như định dạng tệp **STEP**. Các tệp STP tạo điều kiện thuận lợi cho việc trao đổi dữ liệu giữa các ứng dụng theo Giao thức ứng dụng [STEP](/vi/3d/step/) ISO 10303-2xx. ISO này xác định cơ chế mã hóa để biểu diễn dữ liệu bằng ngôn ngữ lập mô hình dữ liệu EXPRESS. Các tệp STP có thể được mở trong các ứng dụng chẳng hạn như **Autodesk Fusion 360**.

## Định dạng tệp STP - Thông tin khác

Các tệp STP được lưu vào đĩa ở định dạng tệp ASCII đơn giản. Chúng chứa thông tin mô hình 3D dưới dạng văn bản thuần túy mà các ứng dụng CAD/CAM có thể đọc được để tải các mô hình này.

Các tệp STP cũng được lưu với phần mở rộng .step và bao gồm một chuỗi các bản ghi. Các tính năng nổi bật về các tệp này bao gồm:

* Bộ ký tự được định nghĩa là các điểm mã của ISO 10646.
* "ISO-10303-21;" là các ký tự đầu tiên trong bản ghi đầu tiên.
* Nhận xét được bao quanh bởi các ký tự "/*" và "*/".
* Bản ghi cuối cùng chứa "END-ISO-10303-21;" nếu tệp BƯỚC phù hợp với phiên bản 2002.
* Trong trường hợp phù hợp với phiên bản 2016, có thể có một hoặc nhiều chữ ký số sau "END-ISO-10303-21;" Kẻ hủy diệt.
* Ngắt dòng được ký hiệu là "\N\" và ngắt trang được ký hiệu là "\F\".

## Mở tệp STP

Các tệp STP có thể được mở trong Trình xem STP cũng như Trình chỉnh sửa văn bản.

### Mở tệp STP bằng Trình xem STP

Các ứng dụng CAD khác nhau có thể mở tệp STP để xem trên Windows, MacOS và Linux. Bao gồm các:

* Autodesk Fusion 360 (đa nền tảng)
* FreeCAD (đa nền tảng)
* IMSI TurboCAD (Windows, Mac)
* Hệ thống Dassault CATIA (WIndows, Linux)

### Mở tệp STP bằng Trình chỉnh sửa văn bản

Các tệp STP được lưu dưới dạng tệp văn bản thuần túy. Điều này cho phép mở tệp STP bằng trình soạn thảo văn bản. Các trình soạn thảo văn bản phổ biến như Notepad và Notepad++ trên HĐH Windows và Apple TextEdit trên MacOS có thể mở các tệp STP. Sau khi mở trong trình soạn thảo văn bản, người dùng có thể chỉnh sửa các thuộc tính của tệp STP. Tuy nhiên, nó có thể dẫn đến hỏng tệp trong trường hợp cập nhật các thuộc tính không chính xác.

## Làm thế nào để chuyển đổi các tập tin STP

Có một số ứng dụng có thể chuyển đổi tệp STP sang các định dạng tệp khác. Các ứng dụng CAD có thể chuyển đổi tệp STP bao gồm:

* Autodesk Fusion 360
* IMSI Turbo CAD
* SiemensSolid Edge

Ngoài những ứng dụng này, có một số ứng dụng trực tuyến có thể chuyển đổi tệp STP sang các định dạng tệp khác. Các ứng dụng trực tuyến này cho phép bạn tải tệp STP của mình lên máy chủ đám mây nơi chúng được chuyển đổi sang định dạng bạn muốn và quay trở lại để tải xuống.

Autodesk Fusion 360 có thể chuyển đổi các tệp STP sang các định dạng tệp 3D và CAD sau.

* [OBJ](/vi/3d/obj/)
* [3MF](/vi/3d/3mf/)
* [DWG](/vi/cad/dwg/)
* [DXF](/vi/cad/dxf/)
* [ASM](/vi/cad/asm/)
* [IGES](/vi/cad/iges/)
* [STL](/vi/cad/stl/)
* [FBX](/vi/3d/fbx/)
* F3D
* [USD](/vi/3d/usd/)

## Người giới thiệu

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

