{
  "date" : "2019-10-11",
  "keywords" :[ "tệp webp", "định dạng tệp webp", "tệp webp là gì", "tệp", "ví dụ webp", "phần mở rộng tệp webp","tiện ích mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WEBP - Định dạng tệp ảnh Google Raster",
  "description":"Tìm hiểu về định dạng tệp WEBP và API có thể tạo và mở tệp WEBP.",
  "linktitle" : "WEBP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp WEBP là gì?

WebP, do Google giới thiệu, là một định dạng tệp hình ảnh web raster hiện đại dựa trên nén không mất dữ liệu và không mất dữ liệu. Nó cung cấp chất lượng hình ảnh tương tự trong khi giảm đáng kể kích thước hình ảnh. Vì hầu hết các trang web đều sử dụng hình ảnh làm biểu diễn dữ liệu hiệu quả, nên việc sử dụng hình ảnh WebP trong các trang web giúp tải trang web nhanh hơn. Theo Google, hình ảnh không mất dữ liệu WebP có kích thước nhỏ hơn 26% so với [PNG](/vi/image/png/), trong khi hình ảnh không mất dữ liệu WebP nhỏ hơn 25-34% so với hình ảnh [JPEG](/vi/image/jpeg/) tương đương. Hình ảnh được so sánh dựa trên chỉ số Tương đồng về Cấu trúc (SSIM) giữa WebP và các định dạng tệp hình ảnh khác. WebP là một dự án chị em của định dạng bộ chứa đa phương tiện [WebM](https://en.wikipedia.org/wiki/WebM).

## Tổng quan về các tính năng của WebP ##

Hình ảnh WebP sử dụng quy trình nén dựa trên dự đoán pixel từ các khối xung quanh chúng, dẫn đến pixel được sử dụng nhiều lần trong một tệp. Nó hỗ trợ hình ảnh động và dự kiến sẽ hỗ trợ nhiều tính năng hơn trong tương lai. Google đã cung cấp mã nguồn [trực tuyến](https://developers.google.com/speed/webp/download) cho bộ mã hóa và giải mã của mình để được sử dụng khi cần thiết. Hình ảnh WebP cung cấp hỗ trợ cho:

* **Nén có mất dữ liệu:** Nén có mất dữ liệu dựa trên mã hóa khung hình chính [VP8](https://en.wikipedia.org/wiki/VP8). VP8 là một định dạng nén video do On2 Technologies tạo ra như một sự kế thừa cho các định dạng VP6 và VP7.
* **Nén không mất dữ liệu:** Định dạng nén không mất dữ liệu do nhóm WebP phát triển.
* **Độ trong suốt:** Kênh alpha 8 bit rất hữu ích cho hình ảnh đồ họa. Kênh Alpha có thể được sử dụng cùng với RGB mất dữ liệu, một tính năng hiện không khả dụng với bất kỳ định dạng nào khác.
* **Hoạt hình:** Nó hỗ trợ hình ảnh hoạt hình có màu sắc trung thực.
* **Siêu dữ liệu:** Nó có thể có siêu dữ liệu EXIF và XMP (ví dụ: được sử dụng bởi máy ảnh).
* **Cấu hình màu:** Nó có thể có cấu hình ICC nhúng.

Nén WebP bị mất dữ liệu sử dụng mã hóa dự đoán để mã hóa hình ảnh, phương pháp tương tự được sử dụng bởi bộ giải mã video VP8 để nén khung hình chính trong video. Mã hóa dự đoán sử dụng các giá trị trong các khối pixel lân cận để dự đoán các giá trị trong một khối và sau đó chỉ mã hóa phần khác biệt.

Nén WebP không mất dữ liệu sử dụng các đoạn hình ảnh đã thấy để tái tạo chính xác các pixel mới. Nó cũng có thể sử dụng bảng màu cục bộ nếu không tìm thấy kết quả phù hợp thú vị.

## Định dạng tệp ##

Định dạng tệp WebP dựa trên định dạng tài liệu RIFF (định dạng tệp trao đổi tài nguyên). Vùng chứa WebP cung cấp hỗ trợ cho nhiều tính năng hơn là chỉ chứa một hình ảnh duy nhất được mã hóa dưới dạng khung chính VP8. Phần tử cơ bản của tệp RIFF là một đoạn bao gồm:


|Trường|Mô tả
---|---|
|Chunk FourCC: 32 bit|Mã bốn ký tự ASCII được sử dụng để nhận dạng đoạn
|Kích thước đoạn: 32 bit (uint32)|Kích thước của đoạn không bao gồm trường này, mã định danh đoạn hoặc phần đệm
|Tải trọng khối: Byte kích thước khối|Tải trọng dữ liệu. Nếu Kích thước khối là số lẻ, một byte đệm đơn ~-~- phải là 0 ~-~- được thêm vào
|ChunkHeader ('ABCD')|Được sử dụng để mô tả tiêu đề FourCC và Kích thước đoạn của các đoạn riêng lẻ, trong đó 'ABCD' là FourCC cho đoạn đó. Kích thước của phần tử này là 8 byte.

### Tiêu đề WebP ###

Tiêu đề tệp WebP như sau:

* Tiêu đề RIFF - 32 bit đại diện cho các ký tự ASCII 'R' 'I' 'F' 'F'
* Kích thước tệp - 32 bit (uint32) biểu thị kích thước của tệp theo byte bắt đầu từ offset 8. Giá trị tối đa của trường này là 2^32 trừ 10 byte và do đó kích thước của toàn bộ tệp tối đa là 4GiB trừ 2 byte .
* 'WEBP' - 32 bit đại diện cho các ký tự ASCII 'W' 'E' 'B' 'P'

### Định dạng tệp bị mất ###

Hình ảnh WebP sử dụng định dạng tệp bị mất dữ liệu nếu hình ảnh dựa trên mã hóa bị mất dữ liệu và không yêu cầu bất kỳ tính năng nâng cao/mở rộng nào như độ trong suốt, hoạt hình, alpha, v.v. Hình ảnh bị mất dữ liệu nhỏ hơn và cũng được các ứng dụng cũ hỗ trợ.

Trong trường hợp này, tệp WebP bao gồm:

* Tiêu đề tệp WebP 12 byte
* Đoạn VP8

[Hướng dẫn giải mã và định dạng dữ liệu VP8](https://tools.ietf.org/html/rfc6386) minh họa các thông số kỹ thuật của định dạng dòng bit VP8.

### Định dạng tệp không mất dữ liệu ###

Bố cục này được sử dụng khi hình ảnh dựa trên mã hóa không mất dữ liệu và không cần các tính năng nâng cao do định dạng bên ngoài cung cấp. Tuy nhiên, các ứng dụng cũ hơn có thể không đọc được các tệp như vậy.

Trong trường hợp này, tệp WebP bao gồm:

* Tiêu đề tệp WebP 12 byte
* Đoạn VP8L

## Người giới thiệu ##

* [Tham khảo dành cho nhà phát triển WebP - Bởi Google](https://developers.google.com/speed/webp/)
* [Định dạng tệp WebP - Theo Wikipedia](https://vi.wikipedia.org/wiki/WebP)

