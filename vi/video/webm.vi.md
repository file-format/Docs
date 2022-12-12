---
date: 2019-10-11
keywords: WEBM, Tệp WEBM là gì, Định dạng tệp WEBM
tác giả:
  display_name: Kashif Iqbal
draft: false
toc: true
description: "Tìm hiểu về định dạng tệp WEBM và các API có thể tạo và mở tệp WEBM."
title: WEBM - Định dạng tệp video WebM
linktitle: WEBM
menu:
  docs:
    parent: "video"
lastmod: 2020-09-12
---

## Tệp WEBM là gì?

Tệp có phần mở rộng .webm là tệp video dựa trên định dạng tệp WebM mở, miễn phí bản quyền. Nó được thiết kế để chia sẻ video trên web và xác định cấu trúc vùng chứa tệp bao gồm các định dạng video và âm thanh. WebM miễn phí 100%, triển khai chất lượng cao dựa trên các công nghệ mở như HTML, HTTP và TCP/IP, mở cho mọi người triển khai. WebM đã được thiết kế đặc biệt để phục vụ video trên web, giúp nó được tối ưu hóa để phát trực tuyến với yêu cầu tính toán thấp. Điều này làm cho nó phù hợp để phát lại video trên mọi thiết bị, đặc biệt là netbook, thiết bị cầm tay và máy tính bảng công suất thấp.

## Định dạng tệp WEBM

Cấu trúc tệp WebM dựa trên tập hợp con của định dạng tệp chứa Matroska [MKV](/vi/video/mkv/). Các luồng video có sẵn trong tệp WebM được nén bằng công nghệ nén VP8 hoặc VP9 có hiệu quả nén cao. Tương tự, các luồng âm thanh trong tệp WebM được nén bằng codec Vorbis hoặc Opus do [Xiph Foundation](https://www.xiph.org/) phát triển. Tất cả các video và codec âm thanh này đều miễn phí bản quyền và có thể được sử dụng mà không phải trả bất kỳ khoản phí nào.

Sau đây là các thông số kỹ thuật tóm tắt cho định dạng tệp WebM.

|Trường|Mô tả|
---|---|
|kiểu MIME |video/webm|
|Kiểu MIME chỉ có âm thanh |audio/webm|
|Số nhận dạng loại thống nhất| org.webmproject.webm|
|Tên bộ giải mã video| VP8 hoặc VP9|
|Tên bộ giải mã âm thanh| Vorbis hoặc Opus|

### Phần tử WebM

WebM, là một tập hợp con của các thông số kỹ thuật Matroska, cung cấp hỗ trợ cho một số chức năng của Matroska. Sau đây là mô tả về các yếu tố được hỗ trợ.

#### EBML

|Tên |Mô tả|
---|---|
|EBML|Đặt các đặc điểm EBML của dữ liệu cần tuân theo. Mỗi tài liệu EBML phải bắt đầu bằng tài liệu này.|
|EBMLVersion |Phiên bản của trình phân tích cú pháp EBML được sử dụng để tạo tệp.|
|EBMLReadVersion|Phiên bản EBML tối thiểu mà trình phân tích cú pháp phải hỗ trợ để đọc tệp này.|
|EBMLMaxIDLength |Độ dài tối đa của ID bạn sẽ tìm thấy trong tệp này (4 hoặc ít hơn trong Matroska).|
|EBMLMaxSizeLength|Độ dài tối đa của các kích thước bạn sẽ tìm thấy trong tệp này (8 hoặc ít hơn trong Matroska). Điều này không ghi đè kích thước phần tử được chỉ định ở đầu phần tử. Các phần tử có kích thước được chỉ định lớn hơn kích thước được EBMLMaxSizeLength cho phép sẽ bị coi là không hợp lệ.|
|DocType|Một chuỗi mô tả loại tài liệu theo sau tiêu đề EBML này (trong trường hợp của chúng tôi là "webm").|
|DocTypeVersion|Phiên bản của trình thông dịch DocType được sử dụng để tạo tệp.|
|DocTypeReadVersion|Phiên bản DocType tối thiểu mà trình thông dịch phải hỗ trợ để đọc tệp này.|

#### Các yếu tố toàn cục

Hiện tại, chỉ hỗ trợ phần tử `Void` được sử dụng để vô hiệu hóa dữ liệu bị hỏng nhằm tránh các hành vi không mong muốn khi sử dụng dữ liệu bị hỏng. Nội dung bị loại bỏ. Cũng được sử dụng để dự trữ không gian trong một phần tử phụ để sử dụng sau này.

#### Bộ phận
Phần tử này chứa tất cả các phần tử cấp cao nhất (cấp 1) khác. Thông thường, tệp Matroska bao gồm 1 phân đoạn.

#### Thông tin tìm kiếm Meta

Các thông tin tìm kiếm sau đây được hỗ trợ.

|Tên thành phần |Mô tả|
---|---|
|SeekHead |Chứa vị trí của phần tử cấp 1 khác.|
|Seek |Chứa một mục tìm kiếm duy nhất cho một phần tử EBML.|
|SeekID |ID nhị phân tương ứng với tên phần tử.|
|SeekPosition |Vị trí của phần tử trong phân đoạn tính bằng octet (0 = phần tử cấp 1 đầu tiên).|

## Người giới thiệu

* [WebM](https://www.webmproject.org/)
* [Kho lưu trữ mã WebM](https://www.webmproject.org/code/#webp-repositories)

