{
"ngày": "2023-06-08",
  "keywords": [
"tập tin hpp",
"tập tin hpp là gì",
"tệp hpp chứa gì",
"ví dụ về tệp hpp",
"định dạng của tệp hpp là gì",
"tài liệu",
"phần mở rộng tập tin hpp",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp HPP - Tệp tiêu đề C++",
  "description":"Tìm hiểu về định dạng HPP và các API có thể tạo và mở tệp HPP.",
"linktitle":"HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
      "parent": "programming"
}
},
"lastmod": "2023-06-08"
}

## Một tập tin HPP là gì?

Định dạng tệp ".hpp" thường được sử dụng cho các tệp tiêu đề trong ngôn ngữ lập trình C++. Các tệp tiêu đề thường chứa các khai báo và định nghĩa về hàm, lớp, biến và hằng được sử dụng bởi các tệp mã nguồn khác trong dự án C++.

Mục đích của việc sử dụng các tệp tiêu đề là cung cấp cách chia sẻ mã chung trên nhiều tệp mã nguồn mà không cần sao chép mã. Khi tệp nguồn C++ cần truy cập các khai báo hoặc định nghĩa từ tệp tiêu đề, nó sẽ bao gồm tệp tiêu đề bằng cách sử dụng chỉ thị tiền xử lý `#include`.

Phần mở rộng tệp ".hpp" thường được sử dụng để chỉ ra rằng tệp là tệp tiêu đề C++. Không bắt buộc phải sử dụng tiện ích mở rộng cụ thể này cho các tệp tiêu đề và bạn cũng có thể gặp các tệp tiêu đề có ".h" hoặc các tiện ích mở rộng khác. Việc lựa chọn phần mở rộng phần lớn là vấn đề quy ước và sở thích cá nhân.

Khi tệp nguồn C++ bao gồm tệp tiêu đề bằng cách sử dụng `#include`, trình biên dịch sẽ kết hợp hiệu quả nội dung của tệp tiêu đề với tệp nguồn trước khi biên dịch nó thành một đơn vị. Điều này cho phép tệp nguồn truy cập các khai báo và định nghĩa trong tệp tiêu đề, cung cấp thông tin cần thiết cho trình biên dịch thực hiện kiểm tra kiểu và tạo mã.

## Tệp HPP chứa gì?

Dưới đây là một số nội dung phổ biến bạn có thể tìm thấy trong tệp ".hpp":

- **Khai báo hàm:** Các tệp tiêu đề thường bao gồm các khai báo hàm mà không được triển khai thực tế. Các khai báo này cung cấp thông tin về tên hàm, kiểu trả về và tham số, cho phép các tệp mã nguồn khác sử dụng hàm mà không cần biết chi tiết triển khai.
- **Khai báo lớp:** Tệp tiêu đề có thể chứa các khai báo lớp, bao gồm tên lớp, biến thành viên, hàm thành viên và chỉ định truy cập. Bằng cách đưa khai báo lớp vào tệp tiêu đề, các tệp mã nguồn khác có thể tạo các đối tượng của lớp đó và truy cập các thành viên của lớp đó.
- **Khai báo hằng số:** Tệp tiêu đề có thể xác định các hằng số, chẳng hạn như biến toàn cục hoặc giá trị enum dùng để chia sẻ trên nhiều tệp mã nguồn. Các hằng số này có thể được truy cập bằng cách đưa tệp tiêu đề vào các tệp nguồn khác, cho phép chúng sử dụng các hằng số đã xác định.
- **Định nghĩa loại:** Tệp tiêu đề có thể chứa định nghĩa loại bằng từ khóa "typedef" hoặc nhập bí danh bằng từ khóa "using". Những định nghĩa này tạo ra tên mới cho các kiểu hiện có, làm cho mã dễ đọc và dễ bảo trì hơn.
- **Định nghĩa hàm nội tuyến:** Trong một số trường hợp, tệp tiêu đề có thể chứa định nghĩa hàm nội tuyến. Hàm nội tuyến là các hàm nhỏ được mở rộng tại nơi gọi thay vì được gọi là hàm riêng biệt. Việc đưa định nghĩa hàm nội tuyến vào tệp tiêu đề cho phép trình biên dịch thay thế lệnh gọi hàm bằng nội dung hàm một cách trực tiếp, có khả năng cải thiện hiệu suất.

## Ví dụ về tệp HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Định dạng của tệp HPP là gì?

HPP là một tệp văn bản thuần túy nhưng tuân theo các quy tắc và cú pháp chung của ngôn ngữ lập trình C++. Dưới đây là bảng phân tích định dạng và cấu trúc chung của tệp ".hpp":

- **Bộ bảo vệ tiêu đề:** Thông thường, tệp ".hpp" bắt đầu bằng bộ bảo vệ tiêu đề để ngăn chặn nhiều phần trong cùng một tệp. Điều này đạt được bằng cách sử dụng các chỉ thị tiền xử lý như `#ifndef`, `#define` và `#endif`. Bộ bảo vệ tiêu đề đảm bảo rằng nội dung của tệp chỉ được đưa vào một lần trong quá trình biên dịch.
- **Bao gồm các câu lệnh:** Sau phần bảo vệ tiêu đề, bạn có thể bao gồm các tệp tiêu đề cần thiết khác bằng cách sử dụng lệnh `#include`. Chúng có thể bao gồm các tiêu đề thư viện tiêu chuẩn hoặc các tiêu đề tùy chỉnh khác mà mã của bạn yêu cầu.
- **Khai báo và Định nghĩa:** Nội dung chính của tệp ".hpp" là các khai báo và trong một số trường hợp là định nghĩa về các lớp, hàm, hằng, bí danh loại và các phần tử khác. Ví dụ: bạn có thể khai báo các lớp bằng từ khóa `class`, các hàm sử dụng kiểu trả về, tên và danh sách tham số của chúng và các hằng số sử dụng từ khóa `const` theo sau là loại và tên của chúng.
- **Định nghĩa hàm nội tuyến:** Trong một số trường hợp nhất định, bạn có thể đưa trực tiếp các định nghĩa hàm nội tuyến vào tệp ".hpp". Các hàm nội tuyến thường được định nghĩa bên trong thân lớp, nghĩa là định nghĩa hàm được bao gồm cùng với phần khai báo của nó. Điều này có thể được thực hiện bằng cách thêm tiền tố vào định nghĩa hàm với từ khóa `inline`.
- **Khai báo vùng tên:** Nếu đang sử dụng vùng chứa tên trong mã của mình, bạn có thể khai báo chúng trong tệp ".hpp". Việc này được thực hiện bằng cách sử dụng từ khóa `namespace`, theo sau là tên không gian tên và kèm theo mã liên quan trong khối không gian tên.

## Người giới thiệu
* [Tệp tiêu đề (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

