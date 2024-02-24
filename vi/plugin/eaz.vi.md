{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp EAZ - Tệp EAZ là gì và làm cách nào để mở tệp?",
  "description":"Tìm hiểu về định dạng tệp EAZ và các API có thể tạo và mở tệp EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-viz"
}
},
  "lastmod" : "2023-12-23"
}

## Một tập tin EAZ là gì?

Tệp EAZ là tệp Bổ trợ được sử dụng bởi ArcGIS Explorer, một ứng dụng miễn phí được ESRI phát triển để khám phá, trực quan hóa và chia sẻ bản đồ. Nó chứa kho lưu trữ tệp nén bao gồm [XML file](/web/xml/), mã được biên dịch và các tệp hỗ trợ cần thiết cho phần bổ trợ. Các tệp này được sử dụng để mở rộng chức năng cơ bản của phần mềm bằng cách kết hợp các nút mới, cửa sổ có thể gắn được và các tiện ích mở rộng khác.

## Định dạng tệp EAZ - Thông tin thêm

Các tệp EAZ được tạo thông qua việc sử dụng ArcGIS Explorer SDK, một bộ công cụ phát triển được thiết kế để tạo các chức năng tùy chỉnh trong ArcGIS Explorer. Các tệp này sử dụng tính năng nén [ZIP](/compression/zip/) để đóng gói nội dung một cách hiệu quả. Cốt lõi của kho lưu trữ, tệp **Addins.xml** nằm trong thư mục gốc, đóng vai trò là thành phần quan trọng phác thảo và nêu chi tiết các tùy chỉnh khác nhau được nhúng trong tệp EAZ.

Về cơ bản, tệp Addins.xml hoạt động như một lộ trình, cung cấp thông tin chi tiết về các cải tiến, sửa đổi và tiện ích mở rộng cụ thể mà tệp EAZ giới thiệu cho ArcGIS Explorer. Thông qua cấu trúc toàn diện này, các nhà phát triển có thể gói gọn và tích hợp liền mạch các tính năng, nút và cửa sổ có thể gắn mới, nâng cao chức năng tổng thể và trải nghiệm người dùng của ứng dụng ArcGIS Explorer.

## Người giới thiệu

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
