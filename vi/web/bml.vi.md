{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp BML - Tệp ngôn ngữ đánh dấu Bean",
  "description":"Tìm hiểu về định dạng tệp BML và các API có thể tạo và mở tệp BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## Tệp BML là gì?

Tệp có phần mở rộng .bml là tệp Ngôn ngữ đánh dấu Bean lưu trữ các lớp Java để hỗ trợ các ứng dụng Java. Điều này cho phép truy cập vào các đối tượng và phương thức Java và không cần tạo chức năng mới bằng cách sử dụng các lớp Java. Nó chỉ định cách các thành phần được kết nối với nhau để thực hiện các tác vụ hữu ích. BML được phát triển bởi IBM alphaWorks để mô tả các cấu trúc và mối quan hệ thành phần. Các tệp BML có thể được mở và xem bằng bất kỳ trình soạn thảo văn bản nào như Trình duyệt web, Microsoft Notepad và Notepad ++.

## Định dạng tệp BML

Trang web IBM alphaworks đã cung cấp hai triển khai BML. Việc triển khai đầu tiên là một trình thông dịch 'phát' tập lệnh BML để tạo phân cấp bean mong muốn. Việc triển khai thứ hai là một trình biên dịch biên dịch bất kỳ tập lệnh BML nào thành mã Java không phản chiếu. Điều này thuận lợi theo nghĩa nó cho phép nắm bắt cấu trúc liên thành phần của ứng dụng bằng ngôn ngữ được thiết kế cho mục đích cụ thể này với khả năng bổ sung để biên dịch nó thành mã Java 'thông thường'.

## Thẻ BML

Sau đây là giải thích về một số thẻ được sử dụng trong ngôn ngữ BML:

### Các<bean> nhãn:

Các<bean> phần tử được sử dụng để tạo các loại đậu mới hoặc tra cứu các loại đậu theo tên. Các<bean> thẻ có định dạng:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
"Id" trong thẻ được liên kết với sổ đăng ký đối tượng cho JavaBean.

### Các<string> nhãn

Có hai cách thẻ chuỗi có thể được sử dụng:

1. Để tạo một chuỗi không rỗng:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Để tạo một chuỗi rỗng:

```
<string/>
```
## Người giới thiệu

* [Nhắn tin hướng đối tượng bằng XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [Ngôn ngữ đánh dấu vật lý](http://web.mit.edu/mecheng/pml/standards.htm)
* [Ngôn ngữ đánh dấu Bean](https://all4dev.blogspot.com/2019/06/bean-markup-lingu-tutorial.html)

