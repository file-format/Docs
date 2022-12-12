{
  "date" : "2020-01-10",
  "keywords" :[ "c", ".c","tệp ac là gì","cách mở tệp c", "phần mở rộng", "tệp", "tệp c","định dạng tệp c", "phần mở rộng tệp c"] ,
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp lập trình ngôn ngữ C - C",
  "description":"Tìm hiểu về định dạng tệp C và API có thể tạo và mở tệp C.",
  "linktitle" : "C",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-01-10"
}

## Tệp C là gì?

Tệp được lưu với phần mở rộng tệp c là tệp mã nguồn được viết bằng ngôn ngữ lập trình C. **Tệp C** bao gồm tất cả việc triển khai chức năng của ứng dụng dưới dạng mã nguồn. Việc khai báo mã nguồn được viết trong các tệp tiêu đề được lưu với phần mở rộng [.h](/vi/programming/h/). C ++ là dạng ngôn ngữ C hiện đại và được sử dụng để phát triển hầu hết các phần mềm hiện nay.

## Tóm tắt lịch sử

Ngôn ngữ C ra đời là kết quả của việc tạo ra các tiện ích khác nhau cho hệ điều hành UNIX. Denis Ritchie, người đứng sau việc tạo ra ngôn ngữ lập trình này, công việc ban đầu bắt đầu vào những năm 1960 và đầu những năm 1970.

## Định dạng tệp C

Các tệp C được viết ở định dạng tệp văn bản thuần túy theo cú pháp ngôn ngữ lập trình. Một tệp C điển hình sẽ có:

* câu lệnh nhập ở đầu tệp để nhập bất kỳ Tệp tiêu đề nào
* một hoặc nhiều phương pháp để thực hiện chức năng mong muốn

### Nhập tiêu đề

Các tệp tiêu đề, với phần mở rộng .h, chứa các câu lệnh bao gồm cần thiết để bao gồm các tệp chức năng khác trong dự án. Ngoài ra, chúng chứa các khai báo của các phương thức được xác định trong tệp triển khai. Các tệp tiêu đề được bao gồm bằng cách sử dụng câu lệnh bao gồm như bên dưới.

```
#include <filename.h>
```

### Triển khai mã nguồn

Việc triển khai thực tế các yêu cầu chức năng được mã hóa dưới dạng các phương thức trong tệp C. Mỗi phương thức trong tệp C có kiểu trả về, tên phương thức và có thể có một số tham số đầu vào. Nếu kiểu trả về không bị vô hiệu, phương thức có thể trả về một giá trị nào đó.

### Mã C Ví dụ
Đây là chương trình ví dụ ac:

```
long some_function();
/* int */ other_function();

/* int */ calling_function()
{
    long test1;
    register /* int */ test2;

    test1 = some_function();
    if (test1 > 0)
          test2 = 0;
    else
          test2 = other_function();
    return test2;
}
```



## **Người giới thiệu** ##

* [Triển khai lớp - Theo Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

