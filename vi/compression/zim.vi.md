{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp ZIM - Tệp lưu trữ OpenZIM",
  "description":"Tìm hiểu về định dạng tệp ZIM và API có thể tạo và mở tệp ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Tệp ZIM là gì? ##

Các tệp có phần mở rộng .zim là các tệp lưu trữ được tạo để lưu trữ nội dung Wiki ngoại tuyến. Nó được coi là định dạng tệp mở phù hợp nhất để lưu trữ Wikipedia trên USB. Nó lưu trữ nội dung trang web ở định dạng nhỏ gọn. Tên của nó xuất phát từ "Zeno IMproved", là định dạng tệp Zeno trước đó. ZIM được duy trì bởi dự án [openZIM ](https://openzim.org/) được Wikimedia CH tài trợ và được Wikimedia Foundation hỗ trợ. Các tệp ZIM có thể được mở bằng các ứng dụng như Kiwix và ZIMReader. Dự án OpenZIM đã tổ chức triển khai định dạng tệp ZIM trên [Github](https://github.com/openzim) để nhận đóng góp từ cộng đồng OpenSource.

## Thông số kỹ thuật định dạng tệp ZIM

Định dạng tệp ZIM được phát triển dựa trên [định dạng tệp Zeno](https://openzim.org/wiki/Zeno_file_format) và không tương thích ngược. Thông số định dạng của định dạng tệp ZIM [có sẵn trực tuyến](https://openzim.org/wiki/ZIM_file_format) của openZIM để nhà phát triển tham khảo. OpenZIM đã cung cấp triển khai mã nguồn mở C++, [LibZim](https://openzim.org/wiki/Zimlib), để đọc và ghi các tệp ZIM.

Định dạng tệp ZIM sử dụng nén LZMA2 để làm cho nội dung nhỏ gọn.

{{< figure src="../ZIM_File_Format.jpeg" alt="Định dạng tệp ZIM" >}}


### Tiêu đề ZIM

Tệp ZIM bắt đầu bằng tiêu đề có độ lệch 0. Tất cả các thành phần đều dựa trên little-endian và tất cả các số nguyên đều là số nguyên không dấu, tức là uint_16, uint_32, uint_64.

|Tên trường |Loại| Bù đắp| Chiều dài| Mô tả|
---|---|---|---|---|
|magicNumber| số nguyên| 0| 4| Số ma thuật để nhận dạng định dạng tệp, phải là 72173914 (0x44D495A)|
|majorVersion| số nguyên| 4| 2| Phiên bản chính của định dạng tệp ZIM (5 hoặc 6)|
|minorVersion| số nguyên| 6| 2| Phiên bản nhỏ của định dạng tệp ZIM|
|uuid| số nguyên| 8| 16| id duy nhất của tệp zim này |
|articleCount| số nguyên| 24| 4| tổng số bài viết|
|clusterCount| số nguyên| 28| 4| tổng số cụm |
|urlPtrPos| số nguyên| 32| 8| vị trí của danh sách con trỏ thư mục được sắp xếp theo URL|
|titlePtrPos| số nguyên| 40| 8| vị trí của danh sách con trỏ thư mục được sắp xếp theo Title|
|cụmPtrPos| số nguyên| 48| 8| vị trí của danh sách con trỏ cụm |
|mimeListPos| số nguyên| 56| 8| vị trí của danh sách loại MIME (cũng như kích thước tiêu đề)|
|trang chính| số nguyên| 64| 4| trang chính hoặc 0xffffffff nếu không có trang chính|
|bố cục| số nguyên| 68| 4| trang bố cục hoặc 0xffffffffff nếu không có trang bố cục|
|checksumPos| số nguyên| 72| 8| con trỏ tới md5checksum của tệp này mà không có tổng kiểm tra. Điểm này luôn luôn là 16 byte trước khi kết thúc tệp.|

## Người giới thiệu ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

