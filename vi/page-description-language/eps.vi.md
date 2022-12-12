{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "file", "extension", "file format", "Page Layout", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp EPS và API có thể tạo và mở tệp EPS.",
  "title" :"Định dạng tệp EPS - Tệp PostScript được đóng gói",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp EPS là gì?

Tệp .eps là một tệp hình ảnh được lưu vào đĩa ở định dạng tệp Postscript được đóng gói. Nó có thể chứa bất kỳ sự kết hợp nào của văn bản, đồ họa và hình ảnh. Các tệp EPS cũng có thể bao gồm một hình ảnh xem trước bitmap được đóng gói bên trong để hiển thị bởi các ứng dụng có thể mở các tệp đó.

## Lịch sử tóm tắt về định dạng tệp EPS

Xem nhanh định dạng tệp EPS từ góc độ lịch sử cho thấy thông tin sau:

* Phiên bản đầu tiên của EPS được Adobe phát hành vào khoảng giữa năm 1985 và 1988
* Phiên bản 2.0 của thông số kỹ thuật EPS được xuất bản vào tháng 1 năm 1989
* Thông số kỹ thuật cho phiên bản 3.0 của EPS đã được xuất bản thành một tài liệu riêng vào năm 1992; đây là phiên bản mới nhất được xuất bản.

EPS, kết hợp với cơ chế mở rộng Quy ước cấu trúc mở được mô tả trong khoản 9 của Đặc tả quy ước cấu trúc tài liệu ngôn ngữ PostScript của Adobe, đã tạo thành cơ sở cho các phiên bản đầu tiên của định dạng tệp Tác phẩm nghệ thuật Adobe Illustrator.

## Định dạng tệp EPS

EPS là định dạng tài liệu độc quyền nhưng được công khai và thông số kỹ thuật định dạng tệp EPS có sẵn công khai để nhà phát triển tham khảo. EPS là định dạng tệp tuân thủ [DSC](https://en.wikipedia.org/wiki/Document_Structure_Conventions) (Quy ước cấu trúc tài liệu) và tuân thủ tất cả các quy tắc do DSC thiết lập. DSC là một định dạng tệp đặc biệt cho các tài liệu PostScript của Adobe. Bất kỳ ứng dụng nào tuyên bố có thể đọc tệp EPS đều phải tuân thủ DSC.

Tệp EPS bao gồm hai phần chính như được giải thích bên dưới.

### Xem trước hình ảnh ###

Một tệp EPS điển hình chứa hình ảnh xem trước ở định dạng nhằm mục đích sử dụng thuận tiện trong quy trình làm việc liên quan đến một số hệ thống hoặc ứng dụng. Mục đích của bản xem trước là để có một hình ảnh ở định dạng mà hầu hết các ứng dụng đồ họa có thể hiển thị; bản xem trước thường có độ phân giải thấp hơn, ở kích thước pixel và/hoặc độ sâu bit. Tệp xem trước có thể ở một trong số các định dạng. Thông số kỹ thuật cho EPS_3 liệt kê ba định dạng xem trước "dành riêng cho thiết bị":

* đối với Apple Macintosh, một hình ảnh PICT được sử dụng bởi ứng dụng QuickDraw
* đối với máy tính DOS, một bitmap TIFF
* Siêu tệp Windows.

PICT và Windows Metafile có thể kết hợp cả dữ liệu bitmap và đồ họa vector. Ngoài ra, thông số kỹ thuật xác định một biểu diễn độc lập với thiết bị rất đơn giản cho hình ảnh xem trước được nhúng trong bản đồ bit. Biểu diễn này được gọi là Định dạng trao đổi PostScript được đóng gói (EPSI).

Bản xem trước EPSI là một bản đồ bit được biểu thị dưới dạng thập lục phân ASCII, được bao bọc giữa một vài nhận xét PostScript để nhận dạng và nhằm mục đích đơn giản và dễ vận chuyển. Để phân biệt các tệp EPS với các định dạng xem trước khác nhau, các phần mở rộng tệp DOS và loại tệp Macintosh khác nhau đã được đề xuất trong thông số kỹ thuật EPS.

### Mã PostScript

Ở mức tối thiểu, định dạng tệp EPS phải bao gồm các phần sau:

* chú thích tiêu đề, %!PS-Adobe-3.0 EPSF-3.0
* và một chú thích hộp giới hạn, %%BoundingBox: llx lly urx ury, mô tả các giới hạn của hình minh họa. Bốn đối số này tương ứng với các góc dưới bên trái (llx, lly) và góc trên bên phải (urx, ury) của hộp giới hạn.

Tệp EPS không thể sử dụng bất kỳ toán tử nào sau đây:

* thiết bị ban nhạc,
* rõ ràng
* trang Bản sao
* xóa
* thoát máy chủ
* thiết bị khung
* khôi phục lại
* initclip
* initgraphics
* initmatrix
* từ bỏ
* kết xuất
* thiết lập toàn cầu
* thiết lập trang
* đã chia sẻ
* bắt đầu công việc.

## Chuyển đổi EPS sang các định dạng tệp khác

Các tệp EPS có thể được chuyển đổi sang các định dạng hình ảnh tiêu chuẩn như [JPG](/vi/image/jpeg/), [PNG](/vi/image/png/), [TIFF](/vi/image/tiff/) và [PDF](/vi/pdf /) sử dụng các ứng dụng khác nhau, chẳng hạn như Adobe Illustrator, Photoshop và PaintShop Pro.

Do [lỗ hổng bảo mật](https://support.office.com/en-us/article/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e- a1b5-cbb0c334a840) trong tệp EPS, Office 2016, Office 2013, Office 2010 và Office 365 đã tắt khả năng chèn tệp EPS vào tài liệu Office.

## Người giới thiệu

* [PostScript được đóng gói - Theo Wikipedia](https://vi.wikipedia.org/wiki/Encapsulated_PostScript)

