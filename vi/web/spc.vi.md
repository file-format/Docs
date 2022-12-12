---
date: 2021-07-05
keywords: spc, .spc, định dạng tệp spc, cách mở tệp spc, Tệp Chứng chỉ Nhà xuất bản Phần mềm
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
title: SPC - Tệp chứng chỉ nhà xuất bản phần mềm
linktitle: SPC
description: "Tìm hiểu về định dạng tệp SPC là gì và các API có thể tạo và mở tệp SPC."
menu:
  docs:
    parent: "web"
lastmod: 2021-09-30
---

## Tệp SPC là gì?

Tệp có phần mở rộng .spc là tệp chứng chỉ bảo mật kỹ thuật số được tạo ở định dạng PKCS #7. Một số ứng dụng, tạo các tệp chứng chỉ này để trao đổi thông tin an toàn. Rất ít ứng dụng như vậy bao gồm OpenSSL và ứng dụng Signcode.exe đi kèm với .NET Framework của Microsoft. Giống như các tệp chứng chỉ khác, chẳng hạn như [.cer](/vi/web/cer/), [.p7c](/vi/web/p7c/) và [.ssp](/vi/web/ssp/), các tệp SPC chứa khóa chung thông tin được mã hóa bằng khóa riêng. Khóa công khai này có thể được chia sẻ công khai với người dùng trong khi khóa riêng được giữ bí mật.

## Định dạng tệp SPC - Thông tin khác

Các tệp SPC được lưu vào đĩa dưới dạng tệp nhị phân có thể được mở trong bất kỳ trình soạn thảo văn bản nào nhưng con người không thể đọc được. Chúng dựa trên phiên bản PKCS # 7 mới nhất hiện có [RFC 2315](https://datatracker.ietf.org/doc/html/rfc2315).

## Người giới thiệu

* [PKCS 7](https://vi.wikipedia.org/wiki/PKCS_7)
* [Tham khảo SSP](https://scalate.github.io/scalate/documentation/ssp-reference.html)

