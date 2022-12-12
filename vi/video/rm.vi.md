---
date: 2019-10-11
keywords: rm, .rm, định dạng tệp rm, định dạng tệp .rm, phần mở rộng .rm, định dạng tệp RealMedia
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp RM và các API có thể tạo và mở tệp RM."
title: Định dạng tệp RM
linktitle: RM
menu:
  docs:
    parent: "video"
lastmod: 2021-04-08
---

## Tệp RM là gì? ##

RealMedia là một định dạng bộ chứa đa phương tiện độc quyền được phát triển bởi RealNetworks sử dụng phần mở rộng .rm. Nó được sử dụng với sự kết hợp của [RealAudio (RA)](/vi/audio/ra/) và [RealVideo(RV)](/vi/video/rv/) để phát trực tuyến qua internet. Các luồng này có tốc độ bit không đổi. Đối với tốc độ bit thay đổi, RealNetworks đã phát triển định dạng Tốc độ bit biến đổi RealMedia (RMVB). RealMedia phù hợp để truyền phát nội dung qua internet và có thể được sử dụng để phát trực tiếp truyền hình chẳng hạn.

## Cấu trúc của tệp RealMedia ##

Tệp RealMedia bao gồm một loạt các đoạn, mỗi đoạn có cấu trúc sau:

```cmd
dword  chunk type (FOURCC)
dword  chunk size, including 8-byte preamble
word   chunk version
byte[] chunk payload
```

Sau đây là các loại khối có trong tệp RealMedia:

- **Tiêu đề tệp RealMedia (.RMF)**: Đây phải là đoạn đầu tiên trong tệp RealMedia. Chỉ có một đoạn RMF trong một tệp. Nó chứa thông tin về số lượng tiêu đề.
- **Tiêu đề thuộc tính tệp (PROP)**: Phần này chứa thông tin về các thuộc tính chung của tệp RealMedia. Chỉ có một đoạn loại này trong mỗi tệp RealMedia.
- **Tiêu đề thuộc tính phương tiện (MDPR)**: Đoạn này chứa thông tin về thuộc tính luồng. Nó chứa thông tin về loại luồng và codec được sử dụng. Có một đoạn MDPR cho mỗi luồng trong tệp.
- **Đầu trang mô tả nội dung (CONT)**: Đoạn này chứa thông tin văn bản như tiêu đề hoặc tác giả của nội dung trong tệp RealMedia. Đoạn này chỉ dành cho mục đích thông tin.
- **Tiêu đề dữ liệu (DATA)**: Đoạn này chứa một nhóm các gói dữ liệu.
- **Phần đầu chỉ mục (INDX)**: Đoạn này xuất hiện sau tất cả các đoạn DATA và chứa các mục nhập chỉ mục. Một tệp có thể có nhiều khối INDX.

## Các định dạng âm thanh và video được hỗ trợ ##

### Định dạng âm thanh ###

- lpcJ: RealAudio 1.0 (VSELP)
- 28_8: RealAudio 2.0 (LD-CELP
-dnet: AC3
- sipr: Sipro
- đầu bếp: Đầu bếp
- atrc: ATRAC3
- ralf: Định dạng RealAudio Lossless
- raac: LC-AAC
- racp: HE-AAC

### Định dạng video ###

- CLV1: Xóa Video
- RV10: H.263
- RV13: H.263
- RV20: H.263+, RV20
- Tiền chất RV30: H.264
- RV40: Tiền thân của H.264, RV40
- RVTR: H.263+ (RV20)

## Người giới thiệu ##

- [RealMedia - Wikipedia](https://en.wikipedia.org/wiki/RealMedia)

