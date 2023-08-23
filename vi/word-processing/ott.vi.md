{
  "date" : "2019-10-11",
  "keywords" :[ "tệp ott", "định dạng tệp ott", "tệp ott là gì", "tệp", "ví dụ ott", "phần mở rộng tệp ott","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OTT - Tệp mẫu OpenDocument",
  "description":"Tìm hiểu về định dạng tệp OTT và các API có thể tạo và mở tệp OTT.",
  "linktitle" : "OTT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp OTT là gì?

Các tệp có phần mở rộng OTT đại diện cho các tài liệu mẫu được tạo bởi các ứng dụng tuân theo định dạng tiêu chuẩn OpenDocument của OASIS. Chúng được tạo bằng các ứng dụng xử lý văn bản, chẳng hạn như OpenOffice Writer miễn phí và có thể chứa các cài đặt có thể được sử dụng để tạo tài liệu mới từ các tệp mẫu này. Các cài đặt này bao gồm lề trang, đường viền, đầu trang, chân trang và các cài đặt trang khác. Các mẫu như vậy được sử dụng trong các tài liệu chính thức như tiêu đề thư của công ty và các biểu mẫu tiêu chuẩn hóa.

## Lược Sử ##

Thông số kỹ thuật định dạng tệp ODP dựa trên tiêu chuẩn được phát triển dưới dạng thông số kỹ thuật ODF. Các thông số kỹ thuật này đã phát triển trong quá khứ dưới dạng ba phiên bản do OASIS phát triển và xuất bản như sau:

**2005:** Phiên bản 1.0 được xuất bản vào tháng 5 năm 2005

**2007:** Phiên bản 1.1 được xuất bản vào tháng 2 năm 2007

**2011:** Phiên bản 1.2 được xuất bản vào tháng 9 năm 2011

Có những thay đổi khá nhỏ trong quá trình chuyển đổi từ phiên bản ODF 1.0 sang 1.1. [Phiên bản ODF 1.2](https://www.oasis-open.org/standards#opendocumentv1.2) là phiên bản mới nhất dành cho các thông số kỹ thuật của ODF và nên được các nhà phát triển tham khảo để phát triển các ứng dụng liên quan đến việc đọc/ghi ODS.

## Thông số kỹ thuật định dạng tệp

Định dạng OpenDocument hỗ trợ biểu diễn tài liệu dưới dạng một tài liệu XML duy nhất cũng như tập hợp một số tài liệu con trong một gói dưới dạng lưu trữ [ZIP](/vi/compression/zip/). Mỗi tệp từ kho lưu trữ ZIP lưu trữ một phần của tài liệu hoàn chỉnh. Mỗi tài liệu con lưu trữ một khía cạnh cụ thể của tài liệu. Ví dụ: một tài liệu con chứa thông tin về kiểu dáng và một tài liệu con khác chứa nội dung của tài liệu. Một tài liệu ODF điển hình có các thành phần sau:

* content.xml – Nội dung tài liệu và kiểu tự động được sử dụng trong nội dung.
* style.xml – Các kiểu được sử dụng trong nội dung tài liệu và các kiểu tự động được sử dụng trong chính các kiểu đó.
* meta.xml – Thông tin meta tài liệu, chẳng hạn như tác giả hoặc thời gian của hành động lưu cuối cùng.
* settings.xml – Cài đặt dành riêng cho ứng dụng, chẳng hạn như kích thước cửa sổ hoặc thông tin máy in.

Ngoài những thứ này, trong gói có thể có nhiều tài liệu con khác như hình thu nhỏ của tài liệu, hình ảnh, v.v. Tệp tài liệu là tập hợp con của các tệp ODF nơi nội dung (trang tính) được lưu trữ trong //content.xml// tài liệu con.

## Người giới thiệu ##

* [OpenDocument - Bởi Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

