---
date: 2019-10-11
keywords: prc, .prc, định dạng file prc, cách mở file prc, đuôi .prc, đuôi prc
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp PRC
linktitle: PRC
description: "Tìm hiểu về định dạng tệp PRC và các API có thể tạo và mở tệp PRC."
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Các định dạng tệp PRC
Phần mở rộng ".prc" đang được sử dụng cho định dạng tệp 3D Đại diện Sản phẩm Nhỏ gọn và định dạng tệp sách điện tử của MobiPocket.

## Tệp Đại diện Sản phẩm Nhỏ gọn (PRC) là gì?

PRC (Sản phẩm đại diện nhỏ gọn) là định dạng tệp 3D được tối ưu hóa để lưu trữ, tải và hiển thị dữ liệu 3D, đặc biệt là từ các hệ thống CAD (Thiết kế hỗ trợ máy tính). Nó là một tệp nhị phân tuần tự, được viết theo cách di động. PRC có thể được sử dụng để nhúng dữ liệu 3D vào tệp PDF. PRC hỗ trợ hầu hết các cấu trúc chính của CAD như cụm và bộ phận, cây của các thực thể 3D, biểu diễn hình học chính xác, biểu diễn tam giác và đánh dấu. PRC sử dụng phần mở rộng .prc và loại phương tiện internet được sử dụng là *model/prc*.

PRC là một định dạng tệp đa mục đích, dựa trên cách sử dụng của nó, có thể được lưu trữ bằng cách nén thông thường để thể hiện trực tiếp dữ liệu CAD hoặc được lưu trữ bằng cách nén cao để giảm kích thước tệp. Dữ liệu 3D được lưu trữ dưới dạng PDF sử dụng định dạng PRC có thể tương thích với các ứng dụng CAM và CAE.

### Thông số định dạng tệp đại diện cho sản phẩm Compact (PRC)

Tệp PRC có một phần tiêu đề chính, theo sau là một hoặc nhiều cấu trúc tệp, sau đó là một tệp mô hình ở cuối. Cấu trúc tệp có một tiêu đề theo sau là các phần dữ liệu sau:

- **Globals**: Nó chứa các cấu trúc tệp được tham chiếu và màu sắc, kiểu đường và hệ tọa độ cho từng thực thể cây của cấu trúc tệp.
- **Cây**: Nó chứa mô tả về cây các mục như số lần xuất hiện của sản phẩm, định nghĩa bộ phận, mục đại diện và đánh dấu.
- **Tessellation**: Nó chứa tất cả dữ liệu được đánh dấu (tam giác hóa) trong các thực thể lá của cây (các mục biểu diễn và đánh dấu).
- **Hình học**: Nó chứa tất cả dữ liệu hình học và cấu trúc liên kết chính xác của các thực thể lá của cây (các mục đại diện).
- **Hình học bổ sung**: Nó chứa dữ liệu tóm tắt của hình học. Điều này cho phép tệp được tải một phần mà không cần tải toàn bộ hình học.

Sau đây là cấu trúc của một tệp PRC điển hình.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Tệp sách điện tử MobiPocket có phần mở rộng PRC là gì
Định dạng tệp sách điện tử được giới thiệu bởi một công ty Pháp có tên **Mobipocket** cũng đang sử dụng phần mở rộng ".prc". Ban đầu, Mobipocket tung ra một ứng dụng miễn phí cho nhiều thiết bị thông minh như máy tính bảng, PDA và điện thoại thông minh. Phần mở rộng ".prc" thực sự giống với .mobi nhưng được sử dụng đặc biệt cho các PDA chỉ hỗ trợ các phần mở rộng **.prc** hoặc **.pdb**.

### Thông số kỹ thuật định dạng tệp Mobipocket PRC
Định dạng tệp MobiPocket PRC dựa trên tiêu chuẩn Sách điện tử mở sử dụng XHTML và nó cũng có thể bao gồm JavaScript và khung. Hỗ trợ cho các truy vấn SQL gốc được sử dụng với cơ sở dữ liệu nhúng cũng có sẵn.

Mobipocket Reader có một thư viện trang chủ. Người đọc có thể chèn các trang trống vào bất kỳ phần nào của cuốn sách và thêm các hình vẽ biến đổi. Có thể quản lý các đối tượng như Chú thích, dấu trang, chỉnh sửa, ghi chú và bản vẽ từ một vị trí duy nhất. Hình ảnh được chuyển đổi sang định dạng GIF và có kích thước tối đa là 64K, đủ cho điện thoại di động có màn hình nhỏ. Mobipocket Reader có dấu trang điện tử và từ điển tích hợp.

Đầu đọc có chế độ toàn màn hình để đọc và hỗ trợ cho nhiều PDA, Communicators và Điện thoại thông minh. Các sản phẩm của Mobipocket hỗ trợ hầu hết các hệ điều hành Palm, Windows, Symbian, BlackBerry nhưng không hỗ trợ Android. Trình đọc hoạt động trên Linux hoặc Mac OS X bằng RƯỢU.

## Người giới thiệu

- [PRC - Wikipedia](https://vi.wikipedia.org/wiki/PRC_(file_format))
- [Đặc tả định dạng PRC](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- [So sánh các định dạng sách điện tử - Theo Wikipedia](https://en.wikipedia.org/wiki/Comparison_of_e-book_formats)

