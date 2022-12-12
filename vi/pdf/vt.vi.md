{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PDF/VT",
  "description":"Tìm hiểu về định dạng tệp PDF/VT và API có thể tạo và mở tệp PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# PDF/VT là gì? #

PDF/VT, được xuất bản dưới dạng [ISO 16612-2](https://www.iso.org/standard/46428.html) vào tháng 8 năm 2010 dưới dạng tiêu chuẩn, được thiết kế để cho phép in tài liệu biến đổi (VDP) ở nhiều định dạng khác nhau. môi trường. Tiêu chuẩn lấy Thông tin biến đổi và In giao dịch làm cơ sở cho tiêu chuẩn. In dữ liệu biến đổi được sử dụng khi một phần thông tin khác nhau đối với mỗi người nhận nội dung. Bản in Giao dịch bao gồm hóa đơn, bảng sao kê và các tài liệu khác kết hợp thông tin thanh toán với thông tin tiếp thị. Điều này dẫn đến sự kết hợp của quá trình xử lý hình ảnh, văn bản và các loại nội dung khác được cải thiện. PDF/VT cho phép quản lý trang linh hoạt và đáng tin cậy đối với dữ liệu in Đầu ra giao dịch khối lượng lớn (HVTO) bằng cách sử dụng khái niệm siêu dữ liệu phần tài liệu (DPM). Các tệp PDF/VT có thể được mở trong trình xem Adobe Acrobat mà không cần thêm bất kỳ thành phần nào khác.

## Phân cấp phần tài liệu ##

Hệ thống phân cấp Phần tài liệu (DPart) giống như cấu trúc cây của các nút phần tài liệu dựa trên tất cả các trang trong tài liệu. Các phần tử của cây này được gọi là các nút DPart. Mỗi nút bên trong chứa các nút DPart khác và mỗi nút lá chỉ định một hoặc nhiều trang cho người nhận. Về cơ bản, hệ thống phân cấp DPart chỉ định trình tự và mối quan hệ của tài liệu hoặc các phần của tài liệu trong tệp PDF/VT. Cấu trúc cây của các nút DPart thể hiện nội dung bên trong của tài liệu PDF/VT một cách dễ dàng vì nó có thể chứa các tài liệu phụ cho nhiều người nhận và mỗi phần tài liệu tương ứng với các trang cho một người nhận. Hệ thống phân cấp DPart là bắt buộc trong các tệp PDF/VT.

## Siêu dữ liệu phần tài liệu (DPM) ##

Siêu dữ liệu phần tài liệu (DPM) được liên kết với mỗi nút trong hệ thống phân cấp phần tài liệu và có thể được sử dụng để truyền đạt thông tin về tài liệu phụ của người nhận cụ thể và các phần của nó. Cụ thể, DPM có thể chứa thông tin về các thuộc tính hoặc thông tin về người nhận ở dạng được mã hóa.

## Mức độ phù hợp ##

PDF/VT được trao cho ba cấp độ tuân thủ sau đây. Tất cả đều dựa trên [PDF](/vi/pdf/) 1.6.

* `PDF/VT-1` - Nó dựa trên PDF/X-4 và chứa tất cả các tài nguyên cần thiết để hiển thị tài liệu PDF.
* `PDF/VT-2` - Được thiết kế để trao đổi nhiều tệp, tài liệu PDF/VT-2 có thể tham chiếu ý định đầu ra bên ngoài, nội dung bên ngoài hoặc cả hai. Một tài liệu PDF/VT và tất cả các tệp PDF được tham chiếu và ý định đầu ra bên ngoài của nó được gọi chung là một bộ tệp PDF/VT-2. Acrobat 9 và hỗ trợ tính năng này.
* `PDF/VT-2s` - Hỗ trợ phát trực tiếp PDF/VT-2. Điều này cho phép các phần dữ liệu được phân đoạn được xử lý.

## Người giới thiệu ##

* [PDF/VT - Theo Wikipedia](https://vi.wikipedia.org/wiki/PDF/VT)
* [Công nghệ đồ họa ISO 16612-2](https://www.iso.org/standard/46428.html)

