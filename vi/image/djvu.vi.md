{
  "date" : "2019-10-11",
  "keywords" :[ "tệp djvu", "định dạng tệp djvu", "tệp djvu là gì", "tệp", "ví dụ djvu", "phần mở rộng tệp djvu","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp DJVU",
  "description":"Tìm hiểu về định dạng tệp DJVU và các API có thể tạo và mở tệp DJVU.",
  "linktitle" : "DJVU",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp DJVU là gì?

DjVu, được phát âm là “déjà vu”, là một định dạng tệp đồ họa dành cho các tài liệu và sách được quét, đặc biệt là những tài liệu có chứa sự kết hợp của văn bản, hình vẽ, hình ảnh và ảnh chụp. Nó được phát triển bởi AT&T Labs. Nó sử dụng nhiều kỹ thuật như tách lớp hình ảnh của văn bản và hình nền, tải lũy tiến, mã hóa số học và nén mất dữ liệu cho hình ảnh bitonal. Vì tệp DJVU có thể chứa hình ảnh màu, ảnh chụp, văn bản và bản vẽ được nén nhưng chất lượng cao và có thể được lưu trong ít dung lượng hơn, do đó, nó được sử dụng trên web dưới dạng sách điện tử, sách hướng dẫn, báo, tài liệu cổ, v.v.

DjVu có thể được phân loại thay thế tốt hơn cho [PDF](/vi/pdf/). Các phần mở rộng tệp được liên kết với DjVu là .DJVU hoặc .DJV. DjVu có thể đạt tỷ lệ nén tốt hơn khoảng 5 – 10 so với các phương pháp hiện có như [JPEG](/vi/image/jpeg/) & [GIF](/vi/image/gif/) đối với tài liệu màu và tốt hơn 3 – 8 lần so với [TIFF](/image/tiff/) trong tài liệu đen trắng. Tài liệu được quét ở 300 DPI với đầy đủ màu sắc lên đến 25 MB có thể được nén xuống còn 30 đến 100 KB. Tương tự, các tài liệu đen trắng có thể được nén tối đa từ 5 đến 30 KB. Trang HTML trung bình có thể lên tới 50 KB, do đó, các tài liệu này có thể được tải lên mạng mà không gặp vấn đề gì.

## Lược Sử ##

Công nghệ DjVu được phát triển trong phòng thí nghiệm AT&T bởi [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner và Paul G từ 1996 đến 2001. Định dạng tệp DjVu đã trải qua nhiều lần sửa đổi, lần gần đây nhất là từ năm 2005.


|Phiên bản|Ngày phát hành|Ghi chú
---|---|---|
|1–19|1996–1999|Đây là các phiên bản phát triển.
|20|Tháng 4 năm 1999|Một trang được đổi thành định dạng Nhiều trang.
|23|Tháng 7 năm 2002|Đoạn CID
|24|Tháng 2 năm 2003|LTAnno chunk
|21|Tháng 9 năm 1999|Định dạng lưu trữ gián tiếp đã được thay thế. Lớp tìm kiếm văn bản đã được thêm vào.
|22|Tháng 4 năm 2001|Hướng trang, màu JB2
|25|Tháng 5 năm 2003|đoạn NAVM. Hỗ trợ cho dấu trang DjVu đã được thêm vào.
|26|Tháng 4 năm 2005|Chú thích văn bản/dòng

## Định dạng tệp DjVu ##

Tài liệu DjVu là các tệp IFF85. Cấu trúc này cung cấp một hệ thống phân cấp chứa thông tin trong tệp DjVu. Những thùng chứa này còn được gọi là "Chunks". Loại khối và ID khối mô tả cách sử dụng khối. Có một tiêu đề 4byte theo sau bởi cấu trúc IFF. Bốn byte đầu tiên của tệp DjVu là 0x41 0x54 0x26 0x54. Phần này thảo luận về các loại tài liệu DjVu khác nhau và các phần tương ứng chứa chúng.


|ID đoạn|Cách sử dụng
---|---|
|MẪU|Khối hỗn hợp có bốn byte dữ liệu đầu tiên của đoạn MẪU là mã định danh phụ.
|FORM:DJVM|Tài liệu DjVu nhiều trang. Đoạn tổng hợp có chứa đoạn DIRM.
|BIỂU MẪU:DJVU|Tài liệu DjVu một trang. Đoạn tổng hợp chứa các đoạn tạo nên một trang trong tài liệu djvu.
|FORM:DJVI|Một tệp DjVu “được chia sẻ” được bao gồm thông qua đoạn INCL. Chú thích được chia sẻ và từ điển hình dạng.
|FORM:THUM|Khối tổng hợp chứa các khối TH44 là các hình thu nhỏ được nhúng.
|DIRM|Thông tin tên trang cho tài liệu nhiều trang.
|NAVM|Thông tin dấu trang
|ANTa, ANTz|Chú thích bao gồm cả cài đặt chế độ xem ban đầu và siêu liên kết, hộp văn bản, v.v.
|TXTa, TXTz|Văn bản Unicode và thông tin bố cục.
|Djbz|Bảng hình chia sẻ.
|Sjbz|BZZ dữ liệu biton JB2 nén được sử dụng để lưu trữ mặt nạ.
|FG44|Dữ liệu IW44 được sử dụng để lưu trữ tiền cảnh
|BG44|Dữ liệu IW44 được sử dụng để lưu trữ nền
|TH44|Dữ liệu IW44 được sử dụng để lưu trữ hình ảnh thu nhỏ được nhúng
|WMRM|Dữ liệu JB2 cần thiết để xóa hình mờ
|FGbz|Dữ liệu màu JB2. Cung cấp một màu cho mỗi (đốm hay hình?) trong đoạn Sjbz tương ứng.
|INFO|Thông tin về trang DjVu
|INCL|ID của đoạn FORM:DJVI được bao gồm.
|BGjp|Nền được mã hóa JPEG
|FGjp|JPEG được mã hóa tiền cảnh
|Smmr|Mặt nạ được mã hóa G4

### Nén DJVU

Một hình ảnh được chia thành nhiều hình ảnh khác nhau và sau đó mỗi hình ảnh được nén riêng. Để tạo tệp DjVu, trước tiên, hình ảnh được tách thành ba hình ảnh, hình nền, hình nền trước và hình ảnh mặt nạ. Thông thường, hình ảnh nền và tiền cảnh là hình ảnh màu có độ phân giải thấp hơn; nhưng hình ảnh mặt nạ là hình ảnh có độ phân giải cao hơn và thông thường văn bản được lưu trữ ở đó. Sau khi tách, hình ảnh nền trước và nền sau được nén thông qua thuật toán nén dựa trên wavelet IW44, trong khi hình ảnh mặt nạ được nén bằng một phương pháp khác gọi là JB2.

Phương pháp mã hóa JB2 loại bỏ phần lớn sự dư thừa trong hình ảnh văn bản bằng cách xác định các hình dạng giống hệt nhau trên trang, chẳng hạn như nhiều lần xuất hiện của một ký tự trong một phông chữ cụ thể. Trước tiên, JB2 mã hóa bitmap của mỗi hình dạng duy nhất bằng cách tận dụng sự dư thừa giữa các hình dạng tương tự. Sau đó, nó mã hóa các vị trí mà mỗi hình dạng xuất hiện trên trang. Cả JB2 và IW44 đều dựa vào một loại bộ mã hóa số học nhị phân thích ứng mới được gọi là bộ mã hóa ZP loại bỏ mọi phần thừa còn lại trong một vài phần trăm của giới hạn Shannon. Bộ mã hóa ZP thích ứng và nhanh hơn các bộ mã hóa số học nhị phân gần đúng khác.

## Người giới thiệu ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)
* [Định dạng tệp DjVu](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

