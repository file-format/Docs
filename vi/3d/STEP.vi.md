---
date: 2019-10-11
keywords: step, .step, định dạng file step, cách mở file step, phần mở rộng .step, phần mở rộng step
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp BƯỚC
linktitle: STEP
description: "Tìm hiểu về định dạng tệp BƯỚC và API có thể tạo và mở tệp BƯỚC."
menu:
  docs:
    parent: "3d"
lastmod: 2020-18-01
---

## Tệp BƯỚC là gì?

Tệp BƯỚC là định dạng trao đổi dữ liệu được sử dụng rộng rãi cho thiết kế có sự trợ giúp của máy tính (CAD). Nó đã được tiêu chuẩn hóa vào năm 1994 bởi ủy ban ISO dưới tên "ISO 10303-21". ISO 10303-21 xác định cơ chế mã hóa để biểu diễn dữ liệu bằng ngôn ngữ lập mô hình dữ liệu EXPRESS. Tệp BƯỚC còn được gọi là tệp p21 và Tệp vật lý BƯỚC. Các phần mở rộng tệp được sử dụng cho tệp BƯỚC là .stp và .step.

## Lịch sử cơ bản

Năm 1994, thông số kỹ thuật ban đầu của Phần 21 đã được ban hành. Nó có một số lỗi đã được sửa chữa bởi bản sửa lỗi kỹ thuật ban hành năm 1996. Phiên bản thứ hai được xuất bản năm 2002 bao gồm bản sửa lỗi và phần mở rộng cho một số phần dữ liệu. Phiên bản thứ ba được xuất bản vào năm 2016 đã bổ sung các phần liên kết và tham chiếu cho phép lưu trữ các thực thể và giá trị trong các tệp bên ngoài. Hỗ trợ UTF-8 đã được thêm vào chuỗi. Chữ ký số đã được thêm vào để xác minh nội dung của tệp và để xác thực thông tin xác thực. Hỗ trợ nén và lưu trữ cấu trúc trao đổi bằng ZIP cũng được thêm vào.

## Định dạng tệp BƯỚC

Định dạng văn bản thuần túy cho tệp BƯỚC bao gồm một chuỗi các bản ghi. Bộ ký tự được định nghĩa là các điểm mã của ISO 10646. "ISO-10303-21;" là các ký tự đầu tiên trong bản ghi đầu tiên. Nhận xét được bao quanh bởi các ký tự "/*" và "*/". Bản ghi cuối cùng chứa "END-ISO-10303-21;" nếu tệp BƯỚC phù hợp với phiên bản 2002. Trong trường hợp nó phù hợp với phiên bản 2016, có thể có một hoặc nhiều chữ ký điện tử sau "END-ISO-10303-21;" Kẻ hủy diệt. Ngắt dòng được ký hiệu là "\N\" và ngắt trang được ký hiệu là "\F\".

Tệp BƯỚC được chia thành các phần và tên của chúng là các thuật ngữ dành riêng. Tất cả các phần kết thúc bằng bản ghi "ENDSEC" và phải theo thứ tự hiển thị bên dưới.

- **HEADER**: Đây là phần bắt buộc và không được lặp lại. Nó bao gồm các thực thể sau:
  - file_description (mandatory)
  - file_name (mandatory)
  - file_schema (mandatory)
  - schema_population (optional)
  - file_population (optional)
  - section_language (optional)
  - section_context (optional)
- **ANCHOR**: Đây là phần tùy chọn không lặp lại đã được giới thiệu trong phiên bản 2016. Nó định nghĩa các tên bên ngoài cho các thể hiện để chúng có thể được tham chiếu.
- **Tham khảo**: Đây là phần tùy chọn không lặp lại cũng được giới thiệu trong phiên bản 2016. Mỗi mục nhập trong phần này liên kết tên đối tượng mục nhập/giá trị với một đối tượng/giá trị trong tệp bên ngoài.
- **DỮ LIỆU**: Đây là phần có thể lặp lại tùy chọn, chứa nội dung cốt lõi của phiên bản mô hình.
- **CHỮ KÝ**: Đây là phần có thể lặp lại tùy chọn đã được giới thiệu trong phiên bản 2016. Nó giữ chữ ký điện tử để xác minh nội dung của tệp hoặc để xác thực thông tin xác thực.

## Người giới thiệu

- [ISO 10303-21 - Wikipedia](https://vi.wikipedia.org/wiki/ISO_10303-21)

