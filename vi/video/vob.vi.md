---
date: 2019-10-11
keywords: vob, .vob, định dạng tệp vob, định dạng tệp .vob, phần mở rộng .vob, phần mở rộng vob, định dạng video vob, tệp dvd vob
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp VOB và các API có thể tạo và mở tệp VOB."
title: Định dạng tệp VOB
linktitle: VOB
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Tập tin VOB là gì? ##

Các tệp VOB thường được lưu trữ trong thư mục VIDEO_TS trên DVD có phần mở rộng .vob. Các tệp VOB chứa dữ liệu video và âm thanh cũng như các dữ liệu khác như menu và phụ đề. VOB dựa trên định dạng luồng chương trình MPEG-2 nhưng nó có các giới hạn và thông số kỹ thuật bổ sung trong các luồng riêng tư. Các tệp VOB là một tập hợp con nghiêm ngặt của các luồng chương trình MPEG, vì vậy tất cả các tệp VOB là các luồng chương trình MPEG nhưng tất cả các luồng chương trình MPEG không tuân thủ VOB.

## Cấu trúc của Video DVD ##

Khi DVD được mở trên máy tính, VIDEO_TS là thư mục cấp cao nhất với AUDIO_TS. AUDIO_TS trống và không được sử dụng. Bên trong thư mục VIDEO_TS có các tệp VOB, BUP và IFO. Các tệp VOB chứa nội dung MPEG. Chúng được chia thành các phần có kích thước 1 GB hoặc nhỏ hơn để chúng tương thích với tất cả các hệ điều hành. Các tệp IFO chứa thông tin liên quan đến menu và cấu trúc tiêu đề. Các tệp BUK là các tệp sao lưu của các tệp IFO có cùng tên. Các tệp này có nghĩa là được lưu giữ ở một khu vực riêng biệt về mặt vật lý để trong trường hợp tệp IFO bị hỏng do hư hỏng vật lý đối với DVD, tệp BUK có thể cung cấp thông tin tương tự.

### Bố trí vật lý ###

- Tất cả các tệp trên đĩa phải liền nhau.
- Các file liên quan nên để cạnh nhau (VOB, IFO, BUP).
- Các tệp được đánh số nên theo thứ tự tăng dần.

## Chống sao chép ##

Nhiều DVD video được mã hóa và ngăn chặn việc sao chép dữ liệu từ DVD. Cần có các khóa xác thực và giải mã để phát các tệp nằm trong khu vực dẫn đầu không thể truy cập được của DVD. Các khóa này được sử dụng bởi phần mềm giải mã CSS có trong đầu đĩa DVD hoặc đầu phát phần mềm. Nếu không có các phím, các tệp video sẽ không thể phát được vì các phím sẽ được yêu cầu khi các tệp được mở.

## Người giới thiệu ##

- [VOB - Wikipedia](https://vi.wikipedia.org/wiki/VOB)
- [Cấu trúc thư mục/Video bên trong DVD](https://en.wikibooks.org/wiki/Inside_DVD-Video/Directory_Structure)

