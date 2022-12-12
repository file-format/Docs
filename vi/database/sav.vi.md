{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "phần mở rộng", "tệp sav", "định dạng tệp sav", "Loại tệp cơ sở dữ liệu", "Định dạng tệp cơ sở dữ liệu", "tệp sav là gì" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp SAV và API có thể tạo và mở tệp SAV.",
  "title" :"SAV - Tệp dữ liệu SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Tệp SAV là gì?
Tệp SAV là tệp dữ liệu được tạo bởi Gói thống kê cho Khoa học xã hội (SPSS), là một ứng dụng được sử dụng rộng rãi bởi các nhà nghiên cứu thị trường, nhà nghiên cứu y tế, công ty khảo sát, chính phủ, nhà nghiên cứu giáo dục, tổ chức tiếp thị, công cụ khai thác dữ liệu để phân tích thống kê. SAV được lưu ở định dạng nhị phân độc quyền và bao gồm tập dữ liệu cũng như từ điển đại diện cho tập dữ liệu, lưu dữ liệu theo hàng và cột.

## Định dạng tệp SAV
Định dạng tệp SAV đã trở nên tương đối ổn định, nhưng chúng tôi không thể nói nó là tĩnh. Khả năng tương thích ngược và xuôi có sẵn tùy chọn khi cần thiết, nhưng không được duy trì đúng cách. Dữ liệu trong tệp SAV được phân loại thành các phần sau:

### Tiêu đề tệp
Nó bao gồm 176 byte. 4 byte đầu tiên biểu thị chuỗi **$FL2** hoặc **$FL3** trong mã hóa ký tự được sử dụng cho tệp. Ba byte cuối cùng biểu thị rằng dữ liệu trong tệp được nén bằng cách sử dụng **ZLIB**. Chuỗi 60 byte tiếp theo bắt đầu **@(#) SPSS DATA FILE** và cũng xác định hệ điều hành và phiên bản SPSS đã tạo ra tệp. Sau đó, tiêu đề tiếp tục với các trường sáu chữ số, chứa số lượng biến trên mỗi quan sát và mã chữ số để nén và kết thúc bằng dữ liệu ký tự cho biết ngày giờ tạo và nhãn tệp.
### Bản ghi mô tả biến
Bản ghi chứa một chuỗi trường cố định, phân loại loại và tên của biến cùng với thông tin định dạng được sử dụng bởi SPSS. Mỗi bản ghi biến có thể tùy chọn chứa nhãn biến có tối đa 120 ký tự và tối đa ba thông số giá trị bị thiếu.
### Nhãn giá trị
Các nhãn giá trị là tùy chọn và được lưu trữ trong các cặp bản ghi có thẻ số nguyên 3 và 4. Bản ghi đầu tiên là thẻ 3 có một chuỗi các cặp trường, mỗi cặp chứa một giá trị và nhãn giá trị được liên kết. Bản ghi thứ hai là thẻ 4, đại diện cho các biến mà bộ giá trị/nhãn áp dụng cho.
### Các tài liệu
Một hoặc nhiều bản ghi với thẻ số nguyên 6. Tài liệu tùy chọn. chứa các dòng 80 ký tự.
### Bản ghi mở rộng
Một hoặc nhiều bản ghi có thẻ số nguyên 7. Bản ghi mở rộng cung cấp thông tin có thể bỏ qua một cách an toàn, nhưng được bảo toàn, trong nhiều trường hợp, cho phép các tệp được viết bởi phần mềm mới hơn để duy trì khả năng tương thích ngược. Bản ghi mở rộng có thẻ loại phụ số nguyên.
### Bộ kết thúc từ điển
Chỉ ghi với thẻ số nguyên 999. Nó tách từ điển khỏi các quan sát dữ liệu.
### Quan sát dữ liệu
Nó được coi là dữ liệu theo thứ tự quan sát, ví dụ: tất cả các giá trị biến cho quan sát đầu tiên, tiếp theo là tất cả các giá trị cho quan sát thứ hai, v.v. Định dạng của bản ghi dữ liệu khác nhau tùy thuộc vào mã nén trong bản ghi tiêu đề tệp. Phần dữ liệu của tệp .sav có thể được giải nén:
- **code 0**: nén theo bytecode
- **mã 1**: được nén bằng nén ZLIB
 







## Người giới thiệu ##

* [Dòng định dạng tệp dữ liệu hệ thống SPSS (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

