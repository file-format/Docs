{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","tệp cd là gì","cách mở tệp cd", "phần mở rộng", "tệp", "tệp cd","định dạng tệp cd", "phần mở rộng tệp cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Tệp sơ đồ lớp Visual Studio",
  "description":"Tìm hiểu về định dạng tệp CD và API có thể tạo và mở tệp CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Tệp CD là gì?

Tệp có phần mở rộng .cd là tệp sơ đồ lớp Visual Studio cung cấp thông tin về cấu trúc và mối quan hệ giữa tất cả các lớp trong giải pháp hiện tại. Một giải pháp Visual Studio (được đại diện bởi [.sln](/vi/programming/sln/)) có thể chứa một hoặc nhiều dự án, mỗi dự án có nhiều lớp khác nhau. Tệp sơ đồ lớp có thể được tạo bằng cách nhấp chuột phải vào dự án và chọn tùy chọn sơ đồ lớp.

## Định dạng Tệp Sơ đồ Lớp (.cd) - Thông tin Khác

Tệp sơ đồ lớp được lưu ở định dạng tệp XML tiêu chuẩn biểu thị các lớp trong dự án dưới dạng các nút XML. Nếu không có Visual Studio, các tệp sơ đồ lớp này có thể được mở trong bất kỳ chương trình ứng dụng nào hỗ trợ mở tệp XML.

### Cách thêm sơ đồ lớp vào dự án Visual Studio

Trong Visual Studio, hãy mở Giải pháp/Dự án mà bạn muốn thêm sơ đồ lớp. Sau đó, bấm chuột phải vào nút dự án rồi chọn Thêm > Mục mới. Hoặc, nhấn Ctrl+Shift+A.

* Hộp thoại Thêm mục mới mở ra.

* Mở rộng Mục chung > Chung, sau đó chọn Sơ đồ lớp từ danh sách mẫu. Đối với các dự án Visual C++, hãy tìm trong danh mục Tiện ích để tìm mẫu Sơ đồ lớp.

### Xuất sơ đồ lớp (CD) sang hình ảnh

Visual Studio cho phép chuyển đổi/xuất sơ đồ lớp sang hình ảnh như [PNG](/vi/image/png/), [JPEG](/vi/image/jpeg/), và [BMP](/vi/image/bmp/). Các tệp sơ đồ lớp đã xuất này có thể được sử dụng cho mục đích lưu giữ hồ sơ tài liệu và gói dữ liệu kỹ thuật (TDP). Để chuyển đổi sơ đồ lớp thành hình ảnh, có thể sử dụng các bước sau từ bên trong Microsoft Visual Studio.

1. Mở tệp sơ đồ lớp (.cd) của bạn.
1. Từ menu Sơ đồ Lớp hoặc menu lối tắt bề mặt sơ đồ, chọn Xuất Sơ đồ dưới dạng Hình ảnh.
1. Chọn sơ đồ.
1. Chọn định dạng bạn muốn.
1. Chọn Xuất để hoàn tất quá trình xuất.

## Người giới thiệu

* [Lớp thiết kế trong Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

