{
  "date" : "2021-06-30",
  "keywords" :[ "tệp msi", "định dạng tệp MSI", "tệp msi là gì", "tệp", "ví dụ msi", "phần mở rộng tệp msi","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp MSI và API có thể tạo và mở tệp MSI.",
  "title" :"MSI - Tệp gói cài đặt Windows",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Tệp MSI là gì?
Một tệp MSI được sử dụng để cài đặt và khởi chạy các chương trình Windows; một gói hoàn chỉnh dành cho Microsoft Windows chứa thông tin cài đặt cho một chương trình phần mềm điển hình, bao gồm các tệp cần thiết sẽ được cài đặt và thông tin về vị trí cài đặt. Các tệp MSI cũng có thể chứa gói cập nhật phần mềm. Các tệp MSI tương tự như [EXE](/vi/executable/exe/), nhưng đôi khi EXE có thể không bao gồm thông tin trình cài đặt và chương trình phần mềm có thể chạy trực tiếp khi thực thi tệp EXE.

## Định dạng tệp MSI
Windows Installer thực sự là một API (Giao diện lập trình ứng dụng) và thành phần phần mềm của Microsoft Windows được sử dụng để cài đặt, gỡ bỏ và bảo trì chương trình phần mềm. Thông tin cài đặt và các tệp tùy chọn được đóng gói dưới dạng các gói cài đặt và cơ sở dữ liệu quan hệ lỏng lẻo được cấu trúc dưới dạng Bộ lưu trữ có cấu trúc COM; còn được gọi là **Tệp MSI**, có phần mở rộng tệp .msi. Các gói có phần mở rộng tệp **.mst** chứa **Tập lệnh chuyển đổi** của Windows Installer, các tệp có phần mở rộng **.msm** chứa **Mô-đun Hợp nhất** và phần mở rộng tệp **.pcp** được sử dụng cho **Thuộc tính tạo bản vá**. Windows Installer trở nên nâng cao hơn sau khi có những thay đổi quan trọng so với các phiên bản trước đó, API Thiết lập. Khung GUI và tự động tạo chuỗi hủy cài đặt là các tính năng mới của Windows Installer. Hiện tại nó đã được coi là một giải pháp thay thế cho các khung trình cài đặt thực thi độc lập.

### Cấu trúc logic của các gói MSI
Một gói chỉ định việc cài đặt một hoặc nhiều sản phẩm đầy đủ và thường được xác định bằng **GUID**. Một sản phẩm được tạo thành từ một hoặc nhiều thành phần và được nhóm thành nhiều tính năng khác nhau. Trình cài đặt Windows không xử lý đồng thời các phụ thuộc giữa các sản phẩm khác nhau. Cấu trúc logic của các gói bao gồm các yếu tố sau:

- **Sản phẩm**: Một chương trình đơn lẻ, được cài đặt, hoạt động hoặc một bộ nhiều chương trình được kết hợp với nhau là một sản phẩm. Một sản phẩm được xác định bởi một GUID duy nhất.
- **Tính năng**: Có thể chứa bất kỳ số lượng thành phần và tính năng phụ nào khác. Các gói nhỏ hơn có thể bao gồm một tính năng duy nhất.
- **Thành phần**: Thành phần được Windows Installer coi là một đơn vị; có thể chứa các tệp chương trình, thư mục, khóa đăng ký, thành phần COM và lối tắt.
- **Đường dẫn chính**: Đường dẫn chính là một tệp cụ thể, nguồn dữ liệu ODBC hoặc khóa đăng ký mà tác giả gói chỉ định là quan trọng đối với một thành phần nhất định.

## Người giới thiệu

* [Trình cài đặt Windows - theo Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


