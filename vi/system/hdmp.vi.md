{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp HDMP - Định dạng tệp kết xuất Heap của Windows",
  "description":"Tìm hiểu về định dạng tệp HDMP và API có thể tạo và mở tệp HDMP.",
  "linktitle" : "HDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## Tệp HDMP là gì?

Tệp HDMP là kết xuất bộ nhớ không nén khi ứng dụng hoặc chương trình gặp sự cố do lỗi. Nó chỉ được tạo bởi Windows XP/Vista và chứa kết xuất trạng thái của ứng dụng khi nó bị lỗi. Khi không được nén, các tệp HDMP chiếm nhiều dung lượng trên đĩa hơn so với các tệp Minidump [MDMP](/vi/system/mdmp/) được nén cho mục đích báo cáo.

Các ứng dụng có thể được sử dụng để **mở** hoặc phân tích các tệp HDMP bao gồm Microsoft Visual Studio với các công cụ Gỡ lỗi cho Windows.

## Định dạng tệp HDMP

Các tệp HDMP được lưu vào đĩa dưới dạng tệp nhị phân và không mang lại bất kỳ lợi ích nào nếu được mở mà không có ứng dụng thích hợp. Chúng chứa dữ liệu hệ thống có liên quan được ghi lại khi xảy ra lỗi.

### Sự khác biệt giữa Định dạng Tệp HDMP và MDMP

HDMP là các tệp kết xuất bộ nhớ không nén. Ngược lại, MDMP là các tệp kết xuất nhỏ được nén để giảm kích thước tệp và gửi tới Microsoft để báo cáo sự cố.

## Tài liệu tham khảo ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

