---
date: 2022-03-20
keywords: mxl, định dạng tệp Musepack, phần mở rộng .mxl
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp MXL và các API có thể tạo và mở tệp MXL."
title: Định dạng tệp MXL - Tệp MusicXML được nén
linktitle: MXL
menu:
  docs:
    parent: "audio"
lastmod: 2022-03-20
---

## Tệp MXL là gì?

Tệp MXL là dạng nén của định dạng tệp MusicXML, là định dạng chuẩn mở để trao đổi bản nhạc kỹ thuật số. Các tệp MusicXML văn bản thuần túy có kích thước lớn và việc sử dụng các tệp đó làm định dạng phân phối trang tính bị ảnh hưởng với kích thước tệp lớn. Sự cố này đã được xử lý bằng [MusicXML](https://www.musicxml.com/) 2.0 bằng cách giới thiệu định dạng tệp MXL nén tệp đủ để giảm kích thước tệp tương tự như tệp MIDI gốc. Loại phương tiện được đề xuất cho các tệp MXL là application/vnd.recordare.musicxml.

## Định dạng tệp MXL

Các tệp MXL được lưu trữ dưới dạng tệp [ZIP](/vi/compression/zip/) được nén [XML](/vi/web/xml/) với phần mở rộng tệp .mxl. Các tệp MXL được nén bằng thuật toán DEFLATE như được chỉ định trong [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt).

### Cấu trúc tệp MXL

Mỗi tệp MXL có định dạng XML dựa trên ZIP phải có tệp META-INF/container.xml mô tả điểm bắt đầu của phiên bản MusicXML của tệp. Không có tệp .xsd tương ứng được xác định cho định dạng tệp MXL.

Một tệp container.xml đơn giản có nội dung như sau. Ví dụ này được lấy từ tệp Dichterliebe01.mxl có sẵn trên trang web MakeMusic.

```
<?xml version="1.0" encoding="UTF-8">
<container>
  <rootfiles>
    <rootfile full-path="Dichterliebe01.musicxml"
              media-type="application/vnd.recordare.musicxml+xml"/>
  </rootfiles>
</container>
```
Trong ví dụ này, các<container> phần tử là phần tử tài liệu. Các<rootfiles> phần tử có thể chứa một hoặc nhiều<rootfile> các phần tử, với phần tử đầu tiên<rootfile> phần tử mô tả gốc MusicXML. Tệp MusicXML được sử dụng làm tệp<rootfile> có thể có<score-partwise> ,<score-timewise> , hoặc<opus> làm thành phần tài liệu của nó.

## Người giới thiệu

* [Tệp MXL nén](https://www.w3.org/2021/06/musicxml40/tutorial/compressed-mxl-files/)
* [RFC 1951](https://www.ietf.org/rfc/rfc1951.txt)

