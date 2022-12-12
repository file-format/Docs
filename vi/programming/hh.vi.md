{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","tệp .hh là gì","cách mở tệp .hh", "phần mở rộng", "tệp", "tệp .hh", "định dạng tệp hh", " phần mở rộng tệp .hh",".Ví dụ tệp HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp tiêu đề HH - C++",
  "description":"Tìm hiểu về định dạng tệp HH và API có thể tạo và mở tệp HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## Tệp HH là gì?

Tệp có phần mở rộng .hh là tệp tiêu đề C++ bao gồm phần khai báo biến, hằng và hàm. Các khai báo này được sử dụng bởi các tệp triển khai C++ tương ứng, thường được lưu dưới dạng các tệp [.cpp](/vi/programming/cpp/) chứa triển khai thực tế của logic người dùng. Các tệp tiêu đề .hh được tham chiếu trong các tệp CPP triển khai bằng cách sử dụng chỉ thị `#include`. Bạn có thể thêm nhiều tệp tiêu đề nhất có thể vào dự án C++ của mình để bao gồm các khai báo cấp dự án.

## Định dạng tệp .HH

Tệp .hh là tệp văn bản thuần túy được tạo theo quy tắc định nghĩa tệp tiêu đề. Thông tin phổ biến nhất được khai báo trong tệp .hh bao gồm những thông tin sau.

**`Biến`** - Trong trường hợp Lập trình hướng đối tượng (OOP), tệp tiêu đề lớp chứa các định nghĩa về tất cả các biến cấp lớp có thể truy cập qua các tệp mã nguồn triển khai
**`Tuyên bố phương thức`** - Tất cả các khai báo phương thức được bao gồm trong tệp tiêu đề .h để có thể truy cập được trên nhiều tệp triển khai.
**`Định nghĩa hàm không nội tuyến`** - Các tệp tiêu đề cũng có thể chứa định nghĩa của một phương thức không nội tuyến.
**`Bản đồ thông báo`** - Một tệp tiêu đề cũng có thể chứa các bản đồ thông báo trong trường hợp triển khai mã nguồn MFC. Trong trường hợp như vậy, bản đồ thông báo được liên kết với việc triển khai chức năng được liên kết với các thành phần giao diện người dùng như nút, hộp kiểm, nút radio, v.v.

## Sự khác biệt giữa tệp .H và .HH

Rõ ràng, không có sự khác biệt như vậy giữa các tệp tiêu đề .h và .hh ngoài cách được khuyến nghị sử dụng các tệp này cho các ngôn ngữ tương ứng, ví dụ như [C](/vi/programming/c/) hoặc C++. Việc đặt tên cho các tệp tiêu đề của bạn theo các ngôn ngữ này giúp bạn phân biệt giữa các ngôn ngữ này trong một dự án lớn có thể là sự kết hợp giữa triển khai C và C++.

Ngoài ra, nếu các tiêu đề được phân tách bằng phần mở rộng, thì trình soạn thảo của bạn có thể tự động áp dụng định dạng phù hợp tương ứng.

Nhìn chung, sự khác biệt của hai định dạng tệp này sẽ không gây hại gì mà sẽ có lợi và được khuyến khích tuân theo để phân biệt C và C++.

### Bảo vệ tiêu đề

Các tệp tiêu đề có thể dẫn đến các lỗi phức tạp khi nhiều khai báo được bao gồm trong cùng một tệp do thêm các tệp tiêu đề khác. Định nghĩa trùng lặp này làm tăng lỗi trình biên dịch. Tình huống có vấn đề này có thể tránh được thông qua một cơ chế được gọi là bảo vệ tiêu đề là các chỉ thị biên dịch có điều kiện như được hiển thị bên dưới.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Với tiêu đề này, bộ tiền xử lý sẽ kiểm tra xem `ANY_UNIQUE_NAME_HERE_HPP` đã được xác định chưa. Nếu tiêu đề được đưa vào cùng một tệp nhiều lần, nội dung của tiêu đề sẽ bị bỏ qua.

## Người giới thiệu

* [Header Filers - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Sự khác biệt giữa định dạng tệp .h và .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

