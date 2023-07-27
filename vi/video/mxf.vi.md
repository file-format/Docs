{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MXF - Định dạng trao đổi tài liệu",
  "keywords" :[ "MXF", "matroska video", "mkv format", "how to play MXF files", "SMPTE", "multimedia", "video" ],
  "description":"Tìm hiểu về định dạng tệp MXF và các API có thể tạo và mở tệp MXF.",
  "linktitle" : "MXF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-01"
}

## Tệp MXF là gì?

Tệp có phần mở rộng .mxf là định dạng bộ chứa đa phương tiện chứa phương tiện âm thanh và video kỹ thuật số cùng với thông tin siêu dữ liệu về tệp. Nó tuân theo tiêu chuẩn SMPTE (Hiệp hội kỹ sư điện ảnh và truyền hình), một hiệp hội toàn cầu gồm các chuyên gia từ kỹ thuật, công nghệ và giám đốc điều hành làm việc trong ngành truyền thông và giải trí. Các tệp MXF có thể được chuyển đổi sang các định dạng tệp khác, chẳng hạn như [AVI](/vi/video/avi/) hoặc [MOV](/vi/video/mov/).

## Định dạng tệp MXF

Các tệp MXF trên thực tế là các tệp nhị phân bao gồm một chuỗi byte theo định dạng xác định. Các ứng dụng giải mã phải tuân thủ định dạng này để hiểu nó và trích xuất thông tin từ nó. Định dạng này cho phép thêm các mục mới mà không vi phạm khả năng tương thích ngược bằng cách sử dụng mã hóa KLV được mô tả bên dưới.

* Khóa – mã định danh của phần tử, Nhãn chung SMPTE (UL)
* Độ dài – độ dài của dữ liệu là mã hóa có độ dài thay đổi được sử dụng để giảm dung lượng cần thiết cho mục này
* Giá trị – giá trị thực tế của phần tử.

### Thông số kỹ thuật định dạng SMPTE

Định dạng tệp MXF đã được xác định bởi các thông số kỹ thuật SMPTE sau.

* SMPTE ST 377-1:2011. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Đặc tả định dạng tệp
* SMPTE ST 377-2 (đang tiến hành kể từ tháng 1 năm 2012). Cú pháp mở rộng được mã hóa KLV cho MXF.
* SMPTE ST 378:2004 (Lưu trữ 2010). Truyền hình — Định dạng trao đổi vật liệu (MXF) — Mô hình hoạt động 1a (Một mặt hàng, Một gói hàng)
* SMPTE ST 379-1:2009. Định dạng trao đổi vật liệu (MXF) — Bộ chứa chung MXF
* SMPTE ST 379-2:2010. Định dạng trao đổi vật liệu (MXF) -- Vùng chứa chung bị ràng buộc MXF
* SMPTE ST 380:2004. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Sơ đồ siêu dữ liệu mô tả-1 (Tiêu chuẩn, Động)
* SMPTE ST 381-1:2005. Tivi — Định dạng trao đổi vật liệu (MXF) — Ánh xạ các luồng MPEG vào Bộ chứa chung MXF (Dynamic)
* SMPTE ST 381-2:2011. Định dạng trao đổi vật liệu (MXF) — Ánh xạ các luồng MPEG vào Bộ chứa chung bị ràng buộc MXF
* SMPTE ST 382:2007. Định dạng trao đổi vật liệu (MXF) — Ánh xạ luồng AES3 và âm thanh sóng phát tới vùng chứa chung MXF
* SMPTE ST 383:2008. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Ánh xạ dữ liệu DV-DIF vào Bộ chứa chung MXF
* SMPTE ST 384:2005. Tivi — Định dạng trao đổi vật liệu (MXF) — Ánh xạ ảnh không nén vào Bộ chứa chung MXF
* SMPTE ST 385:2004. Truyền hình — Định dạng Trao đổi Vật liệu (MXF) — Ánh xạ Bản chất SDTI-CP và Siêu dữ liệu vào Bộ chứa Chung MXF
* SMPTE ST 386:2004 (Lưu trữ 2010). Truyền hình — Định dạng Trao đổi Vật liệu (MXF) — Ánh xạ Dữ liệu Bản chất Loại D-10 vào Bộ chứa Chung MXF
* SMPTE ST 387:2004 (Lưu trữ 2010). Truyền hình — Định dạng Trao đổi Vật liệu (MXF) — Ánh xạ Dữ liệu Bản chất Loại D-11 vào Bộ chứa Chung MXF
* SMPTE ST 388:2004 (Lưu trữ 2010). Truyền hình — Định dạng trao đổi vật liệu (MXF) — Ánh xạ âm thanh được mã hóa theo luật A vào Bộ chứa chung MXF
* SMPTE ST 389:2005. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Phần tử hệ thống phát ngược vùng chứa chung MXF
* SMPTE ST 390:2011. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Mô hình hoạt động chuyên biệt "Atom" (Đại diện đơn giản hóa của một mục)
* SMPTE ST 391:2004 (Lưu trữ 2010). Truyền hình — Định dạng trao đổi vật liệu (MXF) — Mẫu hoạt động 1b (Một mục, Gói tập hợp)
* SMPTE ST 392:2004. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Mẫu hoạt động 2a (Các hạng mục trong danh sách phát, Gói đơn)
* SMPTE ST 393:2004. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Mô hình hoạt động 2b (Các mục trong danh sách phát, các gói tập hợp)
* SMPTE ST 394:2006. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Sơ đồ hệ thống 1 cho Bộ chứa chung MXF
* SMPTE ST 405:2006. Truyền hình — Định dạng trao đổi vật liệu (MXF) — Các thành phần và mục dữ liệu riêng lẻ cho lược đồ hệ thống vùng chứa chung MXF 1
* SMPTE ST 407:2006. Truyền hình — MXF — Mô hình Hoạt động 3a và 3b
* SMPTE ST 408:2006. Truyền hình — MXF — Mô hình Hoạt động 1c, 2c và 3c
* SMPTE ST 410: 2008. Định dạng Trao đổi Vật liệu - Phân vùng Dòng Chung.
* SMPTE ST 422:2006. Định dạng trao đổi vật liệu — Ánh xạ các dòng mã JPEG2000 vào Bộ chứa chung MXF
* SMPTE ST 429.4:2006. Bao bì D-Cinema — Ứng dụng MXF JPEG 2000
* SMPTE ST 429.5:2006. Đóng gói D-Cinema — Tệp theo dõi văn bản có thời gian
* SMPTE ST 429.6:2006. Đóng gói D-Cinema — Mã hóa bản chất tệp theo dõi MXF
* SMPTE ST 434:2006. Định dạng trao đổi vật liệu - Mã hóa XML cho siêu dữ liệu và thông tin cấu trúc tệp
* SMPTE ST 436:2006. Truyền hình — Ánh xạ MXF cho các dòng VBI và các gói dữ liệu phụ trợ
* SMPTE ST 2019-4:2009. Ánh xạ Đơn vị mã hóa VC-3 vào Bộ chứa chung MXF
* SMPTE ST 2037:2009. Ánh xạ VC-1 vào Bộ chứa Chung MXF
* SMPTE RP 2008:2008. Định dạng trao đổi vật liệu — Ánh xạ các luồng AVC vào Bộ chứa chung MXF
* SMPTE RP 2057:2011. Vận chuyển siêu dữ liệu dựa trên văn bản trong MXF
* SMPTE EG 41:2004. Định dạng trao đổi vật liệu (MXF) — Hướng dẫn kỹ thuật. Lưu ý: Tài liệu này không còn được liệt kê trên trang web SMPTE khi được tư vấn vào tháng 1 năm 2012.
* SMPTE EG 42:2004. Định dạng trao đổi vật liệu (MXF) — Siêu dữ liệu mô tả MXF
* SMPTE RDD 3:2008. Đặc tả khả năng tương tác e-VTR MXF
* SMPTE RDD 9-2009. Thông số kỹ thuật về khả năng tương tác MXF của các sản phẩm Sony MPEG Long GOP
* Menu bảng tính đăng ký siêu dữ liệu SMPTE.

### Siêu dữ liệu cấu trúc MXF

Siêu dữ liệu cấu trúc là cơ bản trong tệp MXF vì nó chứa thông tin hữu ích về nội dung của tệp. Siêu dữ liệu MXF chứa thông tin như tốc độ khung hình, kích thước khung hình, ngày tạo tệp và ngày sửa đổi tùy chỉnh. Siêu dữ liệu cấu trúc mô tả cấu trúc và khả năng của tệp MXF bao gồm mô tả về mặt kỹ thuật các thành phần thiết yếu khác nhau và truyền tải cách tạo dòng thời gian đầu ra.

## Người giới thiệu

* [MXF - Wikipedia](https://en.wikipedia.org/wiki/Material_Exchange_Format)
* [MXF - Báo cáo tiến độ](https://tech.ebu.ch/docs/techreview/trev_2010-Q3_MXF-1.pdf)
* [Thư viện mã nguồn mở C++ cho MXF](http://www.freemxf.org/)

