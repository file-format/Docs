{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "usdz file", "usdz file format", "file format", "3d","usdz file download"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Định dạng ZIP mô tả cảnh phổ quát",
  "description":"Tìm hiểu về định dạng tệp USDZ và các API có thể mở và tạo tệp USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## Tệp USDZ là gì?

Tệp có đuôi .usdz là tệp lưu trữ ZIP không nén và không được mã hóa cho định dạng tệp [USD](/vi/3d/usd/) (Mô tả cảnh chung) chứa và proxy cho các tệp có định dạng khác (chẳng hạn như họa tiết và hoạt ảnh) được nhúng trong kho lưu trữ và chạy chúng trực tiếp với thời gian chạy USD mà không cần giải nén. Các tệp USDZ là các gói có thiết kế dựa trên sự trừu tượng hóa cấp độ Ar mới của gói. Usdz đã được đăng ký với IANA và có tên loại phương tiện của mô hình và tên loại phụ là vnd.usd+zip và thông tin chi tiết của nó có thể được tìm thấy trên [trang đăng ký IANA](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip).

## Định dạng tệp USDZ

Các tệp USDZ dựa trên định dạng tệp ZIP lưu trữ các tệp riêng lẻ trong vùng chứa của nó. Điều này cho phép người nhận chỉ cần giải nén nội dung và sử dụng các tệp mô tả cảnh USD thông thường để làm việc và kiểm tra. Hầu như tất cả các hệ điều hành đều cung cấp hỗ trợ dựng sẵn cho các định dạng tệp ZIP và việc chọn định dạng lưu trữ này thay vì bất kỳ phương pháp tùy chỉnh nào giúp các tệp USDZ trở nên hữu ích như một giao thức truyền tải đơn giản.

### Ràng buộc ZIP

Định dạng tệp USDZ sử dụng định dạng tệp ZIP mà không có bất kỳ `nén` và `mã hóa` nào. Điều này nhằm mục đích thiết kế để đáp ứng hai yêu cầu:

* Đối với một gói đã được tải vào bộ nhớ hoặc dưới dạng một tệp trên đĩa, API có sẵn bằng USD để truy cập dữ liệu có trong hình ảnh
* Không cần phải trích xuất các tệp vào đĩa hoặc phân bổ thêm bộ nhớ heap

Với USDZ, cả hai yêu cầu này đều được đáp ứng vì bản thân hầu hết các định dạng hình ảnh đều cho phép các sơ đồ nén bên trong, dẫn đến kích thước tệp nhỏ gọn.

### Yêu cầu Bố cục

Các gói USDZ yêu cầu bố cục của các tệp trong gói là dữ liệu cho mỗi tệp phải bắt đầu ở bội số của 64 byte từ đầu gói. Tuy nhiên, gói phải bắt đầu bằng tệp [USD](/vi/3d/usd/) gốc trong trường hợp nhắm mục tiêu gói bằng tham chiếu đơn giản. Trong trường hợp như vậy, tệp USD đầu tiên này được gọi là Lớp mặc định. Khách hàng muốn cung cấp "nội dung có thể phát trực tuyến" cũng có thể muốn xem xét các ràng buộc về bố cục khác.

## Tải xuống tệp USDZ
Vì các tệp usdz được đóng gói với các hình ảnh và tệp usd chất lượng cao khác nên chúng có thể chiếm dung lượng lưu trữ lớn hơn trên đĩa. Tại đây, bạn có thể tìm thấy tệp ví dụ USDZ đơn giản và nhỏ hơn để tải xuống:

- [Sample.usdz](../sample.usdz)

## Người giới thiệu

* [Thông số định dạng tệp USDZ](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)
