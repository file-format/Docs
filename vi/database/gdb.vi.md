{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp GDB - Tệp cơ sở dữ liệu địa lý tệp ESRI",
  "description":"Tìm hiểu về định dạng tệp GDB và API có thể tạo và mở tệp GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Tệp GDB là gì?

Tệp ESRI Cơ sở dữ liệu địa lý (FileGDB) là tập hợp các tệp trong một thư mục trên đĩa chứa dữ liệu không gian địa lý có liên quan, chẳng hạn như bộ dữ liệu tính năng, lớp tính năng và bảng liên quan. Nó yêu cầu một số tệp khác được giữ cùng với tệp .gdb trong cùng một thư mục để nó hoạt động. Các truy vấn có thể được thực thi trên tệp .gdb để quản lý dữ liệu không gian cũng như phi không gian.

## Định dạng tệp GDB - Thông tin khác

Cơ sở dữ liệu địa lý tệp được tạo thành từ bảy bảng hệ thống cộng với dữ liệu người dùng. Dữ liệu người dùng có thể được lưu trữ trong các loại bộ dữ liệu sau:

* Lớp tính năng
* Bộ dữ liệu tính năng
* Bộ dữ liệu khảm
* Danh mục raster
* Bộ dữ liệu raster
* Bộ dữ liệu sơ đồ
* Bảng (phi không gian)
* Hộp công cụ

Bộ dữ liệu tính năng có thể chứa các lớp tính năng cũng như các loại bộ dữ liệu sau:

* Tệp đính kèm
* Chú thích liên kết tính năng
* Mạng hình học
* Bộ dữ liệu mạng
* Vải bưu kiện
* Các lớp quan hệ
* Địa hình
* Cấu trúc liên kết

Kích thước tối đa mặc định của bộ dữ liệu trong cơ sở dữ liệu địa lý tệp là 1 TB. Kích thước tối đa có thể tăng lên 256 TB đối với các bộ dữ liệu lớn (thường là raster). Điều này được kiểm soát bởi một từ khóa cấu hình. Xem Từ khóa cấu hình cho cơ sở dữ liệu địa lý tệp để biết thêm thông tin.

Cơ sở dữ liệu địa lý tệp cũng có thể chứa các kiểu con và miền và tham gia vào quá trình sao chép kiểm tra/đăng ký và sao chép một chiều.

Một cơ sở dữ liệu địa lý tệp có thể được truy cập đồng thời bởi một số người dùng. Nếu người dùng đang chỉnh sửa, họ phải chỉnh sửa các bộ dữ liệu khác nhau.

## Thông số kỹ thuật định dạng tệp GDB ##

Tệp GDB là định dạng độc quyền của ESRI và thông số kỹ thuật của nó không được công khai. Vì lý do này, chi tiết định dạng tệp cho FIle GDB không thể được ghi lại ở bất kỳ đâu ngoài một số nguồn đã thực hiện [một phần](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) bằng kỹ thuật đảo ngược .

## Người giới thiệu ##

* [Thông số FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

