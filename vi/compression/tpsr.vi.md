{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp TPSR - Tệp báo cáo phiên thử nghiệm TeamViewer",
  "description":"Tìm hiểu về định dạng tệp TPSR và API có thể tạo và mở tệp TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## Tệp TPSR là gì?

TPSR là tệp giao thức kết nối được TeamViewer Assist AR (trước đây gọi là TeamViewer Pilot) sử dụng. Thông tin được lưu trữ trong tệp TPSR được lưu trữ ở định dạng tệp nén [ZIP](/vi/compression/zip/). TPSR chứa lịch sử chi tiết về kết nối TeamViewer giữa chuyên gia và kỹ thuật viên để giải quyết vấn đề và mục đích xem xét. Thông tin chứa trong tệp TPSR bao gồm loại thiết bị, tên, ID AR hỗ trợ, ID chuyên gia, ngày giờ và thời lượng kết nối. Dữ liệu này được lưu trữ trong tệp [JSON](/vi/web/json/) bên trong kho lưu trữ TPSR đã nén.

## Định dạng tệp TPSR

Tệp TPSR được lưu vào đĩa ở định dạng tệp lưu trữ ZIP nơi nội dung được lưu trữ bên trong tệp JSON. Nó được tạo tự động sau khi hoàn thành kết nối Hỗ trợ AR với điều kiện tùy chọn báo cáo Kết nối được bật trong TeamViewer.

TeamViewer Assist AR cho phép các chuyên gia kết nối với kỹ thuật viên để nhận nguồn cấp dữ liệu TRỰC TIẾP của thiết bị đầu cuối từ xa thông qua camera di động. Họ có thể hỗ trợ các kỹ thuật viên giải quyết vấn đề qua điện thoại.

## Mở tệp TPSR

Bạn có thể mở tệp TPSR bằng phiên bản máy tính để bàn của phần mềm TeamViewer. Nếu được cài đặt trên máy tính của bạn, bấm đúp vào tệp TPSR sẽ mở tệp đó trong phần mềm TeamViewer. Các tệp TPSR cũng có thể được xuất sang các tệp [PDF](/vi/pdf/) hoặc có thể được in để có một bản in của tệp giao thức.

## Người giới thiệu ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

