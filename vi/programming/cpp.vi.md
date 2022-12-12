{
  "date" : "2019-10-11",
  "keywords" :[ "C++", "file", "extension", "file format", "C++", "Programming Language" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPP - Tệp mã nguồn C++",
  "description":"Tìm hiểu về định dạng tệp CPP và các API có thể tạo và mở tệp CPP.",
  "linktitle" : "CPP",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp C++ là gì?

Các tệp có phần mở rộng tệp CPP là các tệp mã nguồn cho các ứng dụng được viết bằng ngôn ngữ lập trình C++. Một dự án C++ đơn lẻ có thể chứa nhiều hơn một tệp CPP dưới dạng mã nguồn ứng dụng. Một dự án như vậy bao gồm các loại tệp khác nhau, trong đó tệp CPP được gọi là tệp triển khai vì chúng chứa tất cả các định nghĩa về phương thức được khai báo trong tệp tiêu đề (.h). Toàn bộ dự án C++ dẫn đến một ứng dụng thực thi được khi được biên dịch như một tổng thể.

## Cấu trúc tệp CPP

Cấu trúc tệp CPP đơn giản so với các tệp tiêu đề. Mục đích chính của tệp triển khai như vậy là để tách giao diện khỏi quá trình triển khai. Điều này dẫn đến việc khai báo tất cả các chức năng thành viên trong tệp tiêu đề và chi tiết của chúng bên trong tệp CPP. Tệp triển khai CPP có thể được sử dụng dưới dạng tệp đơn giản để viết ứng dụng hoặc dưới dạng triển khai lớp.

### Thực hiện độc lập

Tệp CPP khi được sử dụng như một ứng dụng độc lập có thể chứa tất cả các triển khai bên trong nó mà không yêu cầu khai báo phương thức trong tệp tiêu đề. Việc triển khai như vậy bao gồm tất cả các phương thức được xác định trong tệp triển khai trong đó mục nhập của ứng dụng được quản lý bởi một phương thức chính lấy đầu vào tùy chọn của người dùng làm đối số. Nó cũng có thể bao gồm bất kỳ thư viện nào từ Thư viện chuẩn C++ để được sử dụng bởi bất kỳ phương thức nào được khai báo trong tệp.

```
/*
* File: main.cpp
* Author: SomeOne
* Created on November 16, 2018, 4:09 PM
*/

#include <iostream>
using namespace std;

int main()
{
   cout<<"About the CPP file format";
   cout<<std::endl<<"and its very easy";
}
```

### Thực hiện lớp

Trong Lập trình hướng đối tượng (OOP), tệp CPP được sử dụng làm định nghĩa lớp. Trong trường hợp như vậy, tất cả các thành viên dữ liệu của lớp và các hàm thành viên được khai báo bên trong tệp tiêu đề. Mỗi tệp tiêu đề cũng có thể có tham chiếu đến các phương thức thư viện chuẩn. Tệp CPP định nghĩa lớp đề cập đến tệp tiêu đề trong một câu lệnh bao gồm ở đầu tệp. Hầu hết, các nhà phát triển phần mềm bao gồm các nhận xét khi bắt đầu tệp triển khai lớp như vậy để cung cấp thông tin về nội dung thực tế của tệp, chi tiết của tác giả và ngày triển khai. Trong những trường hợp như vậy, các tệp triển khai tiêu đề phải có cùng tên. Một ví dụ về tệp tiêu đề và tệp triển khai như sau.

### Tập tin tiêu đề

```
#include <string>
#include <iostream>

using namespace std;

class MyClass {
public:
   MyClass();     // Constructor
   void add(int i, int j);

private:
   std::string name;
};
```

### Tệp triển khai CPP

```
#include "MyClass.h"

MyClass::MyClass(){
   ...
}
void MyClass::add(int i, int j) {
   int result # i + j;
}
```

## Người giới thiệu

* [Triển khai lớp - Theo Wikipedia](https://en.wikipedia.org/wiki/Class_implementation_file)

