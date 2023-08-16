---
date: 2019-12-13
keywords: m3u, định dạng tệp m3u, phần mở rộng .m3u, danh sách phát đa phương tiện m3u, định dạng danh sách phát m3u
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp M3U và các API có thể tạo và mở tệp M3U."
title: Định dạng tệp M3U
linktitle: M3U
menu:
  docs:
    parent: "audio"
lastmod: 2020-22-12
---

## Tệp M3U là gì? ##

M3U (URL MP3) là tệp danh sách phát âm thanh được lưu trữ với phần mở rộng .m3u. M3U không phải là một tệp âm thanh thực tế, nó chỉ trỏ đến các tệp âm thanh và đôi khi là video. M3U được Fraunhofer phát triển để sử dụng với phần mềm Winplay3. Nó cũng được hỗ trợ bởi nhiều trình phát đa phương tiện và phần mềm.

## Định dạng tệp M3U

Không có thông số kỹ thuật chính thức cho định dạng tệp M3U, nó là một tiêu chuẩn thực tế. M3U là tệp văn bản thuần túy sử dụng phần mở rộng .m3u nếu văn bản được mã hóa bằng mã hóa không phải Unicode mặc định của hệ thống cục bộ hoặc bằng phần mở rộng .m3u8 nếu văn bản được mã hóa UTF-8. Mỗi mục trong tệp M3U có thể là một trong những mục sau:

- Đường dẫn tuyệt đối đến tệp
- Đường dẫn tệp liên quan đến tệp M3U.
- URL

### M3U mở rộng ###

Trong M3U mở rộng, các lệnh bổ sung được giới thiệu bắt đầu bằng "#" và kết thúc bằng dấu hai chấm (:) nếu chúng có tham số. Đưa ra dưới đây là danh sách các chỉ thị cho M3U mở rộng.

- **#EXTM3U** - Đây là tiêu đề tệp cho biết M3U mở rộng và phải là dòng đầu tiên của tệp.
- **#EXTENC:** - Mã hóa văn bản. Nó phải là dòng thứ 2 của tệp.
- **#EXTINF:** - Được sử dụng cho thông tin bản nhạc và các thuộc tính bổ sung khác.
- **#PLAYLIST:** - Tiêu đề của danh sách phát
- **#EXTGRP:** - Bắt đầu nhóm tên
- **#EXTALB:** - Thông tin album
- **#EXTART:** - Nghệ sĩ album
- **#EXTGENRE** - Thể loại album
- **#EXTM3A** - Danh sách phát tệp đơn cho các bản nhạc hoặc chương trong album.
- **#EXTBYT:** - Kích thước tệp tính bằng byte.
- **#EXTBIN:** - Dữ liệu nhị phân theo sau.
- **#EXTIMG:** - Logo, Ảnh bìa hoặc các hình ảnh khác.

### HLS M3U ###

HLS (HTTP Live Streaming) được Apple tạo ra để truyền phát âm thanh và radio đến các thiết bị iOS. Nó dựa trên M3U mở rộng được mã hóa UTF-8. Nó đã được chuẩn hóa thành RFC 8216 vào năm 2017 bởi IETF. Các thẻ cho danh sách phát HLS bắt đầu bằng "#EXT-X-". Dưới đây là danh sách các thẻ cho HLS

- **EXT-X-VERSION** - Cho biết phiên bản tương thích của tệp dựa trên phương tiện và máy chủ của nó.
- **#EXT-X-START:** - Cho biết điểm bắt đầu ưu tiên cho danh sách phát.
- **#EXT-X-PLAYLIST-TYPE:** - Cung cấp loại danh sách phát (SỰ KIỆN hoặc VOD).
- **#EXT-X-TARGETDURATION:** - Chỉ định thời lượng Phân đoạn tối đa.
- **#EXT-X-MEDIA-SEQUENCE:** - Nó cho biết Số thứ tự phương tiện.
- **#EXT-X-INDEPENDENT-SEGMENTS** - Nó cho biết rằng tất cả các mẫu phương tiện đều độc lập và có thể được giải mã mà không cần các phân đoạn khác.
- **#EXT-X-MEDIA:** - Nó được sử dụng để liên kết các Danh sách phát phương tiện có chứa các Phiên bản thay thế có cùng nội dung.
- **#EXT-X-STREAM-INF:** - Nó chỉ định Luồng biến thể là một phần của Phiên bản.
- **#EXT-X-BYTERANGE:** - Cho biết rằng Phân đoạn phương tiện là một dải con của tài nguyên được xác định bởi URI của nó.
- **#EXT-X-DISCONTINUITY** - Cho biết sự gián đoạn giữa phân đoạn phương tiện trước và sau.
- **#EXT-X-DISCONTINUITY-SEQUENCE:** - Nó cho phép đồng bộ hóa giữa các phiên bản khác nhau của cùng một Luồng biến thể hoặc các Luồng biến thể khác nhau.
- **#EXT-X-KEY:** - Chỉ định cách giải mã Phân đoạn phương tiện.
- **#EXT-X-MAP:** - Chỉ định cách lấy Phần khởi tạo phương tiện. Cần phải phân tích cú pháp Phân đoạn phương tiện hiện hành.
- **#EXT-X-PROGRAM-DATE-TIME:** - Nó liên kết mẫu đầu tiên của Phân đoạn phương tiện với một ngày và/hoặc thời gian tuyệt đối.
- **#EXT-X-DATERANGE:** - Nó liên kết Phạm vi dữ liệu.
- **#EXT-XI-FRAMES-ONLY** - Cho biết rằng mỗi Phân đoạn phương tiện trong Danh sách phát mô tả một khung hình I duy nhất.
- **EXT-XI-FRAME-STREAM-INF** - Nó chỉ ra rằng tệp danh sách phát chứa I-frame của bản trình bày Đa phương tiện.
- **#EXT-X-SESSION-DATA:** - Nó cho phép dữ liệu phiên tùy ý được
được đưa vào Danh sách phát chính.
- **#EXT-X-SESSION-KEY:** - Nó cho phép khóa mã hóa. Khách hàng có thể tải trước các phím này mà không cần đọc danh sách phát trước.
- **#EXT-X-ENDLIST** - Nó cho biết rằng sẽ không có thêm Đoạn phương tiện nào được thêm vào tệp.

Sau đây là danh sách các loại phương tiện Internet được sử dụng bởi M3U:

- **application/vnd.apple.mpegurl**: Đây là loại phương tiện đã đăng ký duy nhất (đăng ký năm 2009) cho M3U được sử dụng để chỉ danh sách phát trong các ứng dụng HLS.
- Các loại phương tiện Internet sau đây được sử dụng bởi các ứng dụng không phải HLS.
  - **application/mpegurl**
  - **application/x-mpegurl**
  - **audio/mpegurl**
  - **audio/x-mpegurl**

## Ví dụ M3U ##

Đây là một ví dụ về tệp M3U.

```console
#EXTM3U

#EXTINF:111, Sample artist name - Sample track title
C:\Music\SampleMusic.mp3

#EXTINF:222,Example Artist name - Example track title
C:\Music\ExampleMusic.mp3
```
## Người giới thiệu ##

- [M3U - Wikipedia](https://en.wikipedia.org/wiki/M3U)
- [Phát trực tiếp HTTP](https://tools.ietf.org/html/rfc8216)

