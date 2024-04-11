{
  "date" : "2019-10-11",
  "keywords" :[ "XPS", "Thông số kỹ thuật giấy XML", "Tệp", "Phần mở rộng", "Định dạng tệp", "EMF", "PDF"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPS - Định dạng tệp bố cục trang",
  "description":"Tìm hiểu về định dạng tệp XPS và các API có thể tạo và mở tệp XPS.",
  "linktitle" : "XPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## Tệp XPS là gì? ##

Tệp XPS đại diện cho các tệp bố cục trang dựa trên Thông số kỹ thuật giấy XML do Microsoft tạo. Nó được phát triển để thay thế định dạng tệp EMF và tương tự như định dạng tệp [PDF](/vi/pdf/), nhưng sử dụng XML trong bố cục, giao diện và thông tin in của tài liệu. Trên thực tế, sẽ hợp lý hơn khi nói rằng XPS là một nỗ lực đối với PDF, nhưng không thể có đủ mức độ phổ biến như sở hữu của PDF vì nhiều lý do. Microsoft cung cấp XPS Document Writer theo mặc định từ Windows 7 trở đi để tạo các tệp XPS. Các tệp XPS có thể được tạo bằng cách chọn "Microsoft XPS Document Writer" làm máy in trong khi in tài liệu.

Trình xem XPS được tích hợp như một phần của Windows Vista, Windows 7, Windows 8 và Internet Explorer 6 trở lên. Các tệp XPS trở thành chỉ đọc sau khi chúng được tạo. Điều này làm tăng thêm sự tin tưởng của người dùng đối với các tài liệu đã nhận được gửi dưới dạng XPS về tính xác thực của tài liệu. Một tài liệu XPS có thể chứa một hoặc nhiều trang như được chuyển đổi từ tài liệu gốc.

## Lược Sử ##

Microsoft đã gửi thông số kỹ thuật XPS cho Ecma International. Vào tháng 6 năm 2007, Ủy ban Kỹ thuật Ecma 46 (TC46) đã được thành lập để phát triển một tiêu chuẩn dựa trên Thông số kỹ thuật của OpenXPS Paper. Ecma International đã phê chuẩn Tiêu chuẩn Ecma (ECMA-388) [Thông số kỹ thuật của XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/) vào tháng 6 năm 2009 tại Đại hội đồng lần thứ 97.

## Định dạng tệp XPS ##

Định dạng XPS bao gồm đánh dấu XML xác định thành phần của tài liệu và giao diện trực quan của từng trang cùng với các quy tắc hiển thị để hiển thị hoặc in tài liệu. Nó giữ lại tất cả thông tin để tạo lại một tài liệu trên bất kỳ hệ thống nào, làm cho nó độc lập với các tài nguyên có sẵn trên hệ thống đó. Định dạng về cơ bản là một kho lưu trữ ZIP và nếu bạn đổi tên phần mở rộng tệp thành ZIP, bạn sẽ thấy các tệp cấu thành chứa dữ liệu tài liệu. Những tài liệu này bao gồm:

* tệp trang tài liệu (.fpage) - Chứa nội dung tài liệu và cài đặt định dạng tài liệu. Mỗi trang trong tài liệu XPS có một tệp FPAGE.
* tệp cài đặt tài liệu (.fdoc) - Lưu trữ các cài đặt có trong kho lưu trữ XPS.
* tệp phân đoạn tài liệu (.frag) - Xác định cài đặt cho tệp XPS thực tế và mọi trang trong tài liệu đều có tệp .frag riêng.

{{< figure src="../XPS-1.png" alt="Định dạng tệp XPS" >}}

Các tệp này giữ lại nội dung tài liệu theo cách chẳng hạn như nếu ai đó không cài đặt cùng một phông chữ trên máy của họ, thì trình xem XPS vẫn sẽ hiển thị các phông chữ gốc đó. Điều này ngụ ý việc bao gồm tệp đánh dấu XML cho mỗi:

* Trang
* Chữ
* Phông chữ nhúng
* Hình ảnh raster
* Đồ họa véc tơ 2D
* Quản lý bản quyền kỹ thuật số

Định dạng Tài liệu XPS bao gồm một tập hợp các phần và mối quan hệ được xác định rõ ràng, mỗi phần đáp ứng một mục đích cụ thể trong tài liệu. Định dạng này cũng mở rộng các tính năng của gói, bao gồm chữ ký điện tử, hình thu nhỏ và xen kẽ.

Một tài liệu XPS điển hình trông như sau và có thể được phân tích theo định dạng tệp XPS thông số kỹ thuật.

{{< figure src="../XPS-2.png" alt="Định dạng tệp XPS" >}}


## Người giới thiệu ##

* [Thông số định dạng tệp XPS](https://www.ecma-international.org/publications-and-standards/standards/ecma-388/)
* [XPS - Theo Wikipedia](https://en.wikipedia.org/wiki/Open_XML_Paper_Specification#Viewing_and_creating_XPS_documents)

