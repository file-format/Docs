{
  "date" : "2020-11-11",
  "keywords" :[ "MDB", "phần mở rộng", "tệp", "định dạng tệp", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "Tệp cơ sở dữ liệu" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp MDB và API có thể tạo và mở tệp MDB.",
  "title" :"Định dạng tệp MDB - Tệp cơ sở dữ liệu Microsoft Access",
  "linktitle" : "MDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-11"
}

## Tệp MDB là gì?

Tệp có phần mở rộng .mdb là tệp cơ sở dữ liệu Microsoft Access là Hệ thống quản lý cơ sở dữ liệu quan hệ (RDBMS). Nó lưu trữ dữ liệu trong các bảng cơ sở dữ liệu được liên kết với nhau thông qua khóa chính và khóa ngoại. Tệp MDB chứa cấu trúc hoàn chỉnh của các bảng cơ sở dữ liệu, truy vấn, thủ tục được lưu trữ. MDB là định dạng tệp mặc định cho Microsoft Access 2003. Các phiên bản sau của Microsoft Access sử dụng định dạng tệp [ACCDB](/vi/database/accdb/), đây là định dạng tệp mới nhất cho đến nay. Các tệp MDB có thể được mở bằng các ứng dụng như Microsoft Access, MDB Viewer, MDBOpener và có thể được chuyển đổi sang các định dạng ACCDB, [CSV](/vi/spreadsheet/csv/), Excel, v.v.

## Định dạng tệp MDB

Có các thông số kỹ thuật công khai dành cho định dạng MDB và nó vẫn là định dạng tệp độc quyền của Microsoft. Tuy nhiên, Microsoft cung cấp quyền truy cập kết nối vào tệp MDB bằng tiêu chuẩn Kết nối cơ sở dữ liệu mở (ODBC) và Visual Basic for Applications (VBA). Hướng dẫn MDB không chính thức cung cấp mô tả ngắn gọn không chính thức về định dạng MDB dựa trên kỹ thuật đảo ngược và có thể tham khảo để biết về các thông số kỹ thuật.

### Trang

Theo hướng dẫn MDB không chính thức, tệp MDB bao gồm các trang có kích thước cố định (2048 byte cho Jeb DB3 và 4096 byte cho Jet DB 4). Byte đầu tiên cho biết loại trang. Sau đây là các loại trang chính:

`Trang đầu tiên:` Nó chứa thông tin tiêu đề cơ sở dữ liệu cũng bao gồm việc nhận dạng phiên bản Jet DB tương thích với tệp. Ngoài ra, nó cũng bao gồm thông tin bảo mật tệp và bản đồ sử dụng trang.

`Trang định nghĩa bảng:` Trang định nghĩa bảng chỉ định các cột, kiểu dữ liệu, chỉ mục và thông tin khác. Nó sử dụng các trang bổ sung nếu được yêu cầu và bao gồm bản đồ các trang chứa dữ liệu hàng cho bảng này.

`Trang dữ liệu:` Trang dữ liệu là vùng chứa dữ liệu thực tế nơi dữ liệu được lưu trữ theo hàng. Nó sử dụng các trang phụ để lưu trữ các giá trị dữ liệu dài.

Một cơ sở dữ liệu Microsoft Access duy nhất có thể bao gồm nhiều tệp cho phép vượt quá giới hạn kích thước tệp và bảng. Điều này tạo điều kiện để đưa các biểu mẫu và mã vào tệp MDB giao diện người dùng trên máy tính để bàn của người dùng và dữ liệu trong các tệp MDB phụ trợ khác trên các máy chủ được kết nối với mạng.

## Người giới thiệu ##

* [Thông số truy cập](https://support.microsoft.com/en-us/office/access-specutions-0cf3c66f-9cf2-4e32-9568-98c1025bb47c)
* [Hướng dẫn MDB không chính thức](http://jabakobob.net/mdb/)

