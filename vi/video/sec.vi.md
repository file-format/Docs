---
date: 2022-03-25
keywords: sec, .sec, định dạng tệp sec, định dạng tệp .sec, phần mở rộng .sec, phần mở rộng sec
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp SEC và API có thể tạo và mở tệp SEC."
title: Định dạng tệp SEC - Tệp video bảo mật của Samsung
linktitle: SEC
menu:
  docs:
    parent: "video"
lastmod: 2022-03-25
---

## Tệp SEC là gì?

Tệp SEC là tệp video được tạo bằng hệ thống giám sát Samsung DVR. Video được ghi lại từ camera giám sát và được lưu vào đĩa ở định dạng SEC. Có thể phát lại video SEC đã ghi bằng phần mềm video của Samsung có thể quản lý nguồn cấp dữ liệu video từ nhiều camera.

## Định dạng tệp SEC - Thông tin khác

Tệp SEC chứa luồng h264/AVC bên trong sử dụng định dạng tệp độc quyền. Tiêu đề của tệp SEC bắt đầu bằng số kiểu máy của SRD-1670D. Thông tin ngày và giờ được giữ ở cuối tệp.

### Chuyển đổi tệp SEC sang AVI

Tệp SEC có thể được chuyển đổi sang định dạng tệp [AVI](/vi/video/avi/) tiêu chuẩn bằng cách sử dụng FFmpeg.

```
ffmpeg -i 0010600.sec -vcodec copy -vsync drop -fflags genpts -f avi 0010600.avi
```

## Người giới thiệu ##

- [Tệp Samsung và SEC](https://sreadys.wordpress.com/2013/07/19/samsung-and-sec-files/)

