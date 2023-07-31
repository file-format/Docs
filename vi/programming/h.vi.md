{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h","tệp ah là gì","cách mở tệp h", "phần mở rộng", "tệp", "tệp h","định dạng tệp h", "phần mở rộng tệp h", "Ví dụ tệp H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp tiêu đề H - C/C++",
  "description":"Tìm hiểu về định dạng tệp H và các API có thể tạo và mở tệp H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## Tệp H là gì?

Tệp được lưu với phần mở rộng tệp **h** là tệp tiêu đề được sử dụng trong tệp C/C++ để bao gồm phần khai báo biến, hằng và hàm. Chúng được giới thiệu bởi các tệp triển khai [C++](/vi/programming/cpp/) có chứa triển khai thực tế của các chức năng này. Tệp tiêu đề .h cũng có thể bao gồm thông tin bổ sung, chẳng hạn như định nghĩa Macro. Các tệp tiêu đề này được tham chiếu trong các tệp C/C++ bằng chỉ thị `#include`.

Một dự án C++ mới thường chứa một tệp tiêu đề đặc biệt có tên tệp **stdafx.h** là điểm bắt đầu cho tất cả các chuỗi biên dịch và tất cả các tệp tiêu đề có thể được bao gồm trong tệp duy nhất này. Có thể mở tệp .h bằng bất kỳ trình soạn thảo văn bản nào, Eclipse IDE, Microsoft Visual Studio IDE, trình biên dịch Borland C++ và nhiều ứng dụng khác.

## Định dạng tệp .H

Tệp .h là tệp văn bản thuần túy có các quy tắc riêng để xác định cú pháp. Tệp tiêu đề có thể chứa các thông tin sau.

**`Biến`** - Trong trường hợp Lập trình hướng đối tượng (OOP), tệp tiêu đề lớp chứa các định nghĩa về tất cả các biến cấp lớp có thể truy cập qua các tệp mã nguồn triển khai
**`Tuyên bố phương thức`** - Tất cả các khai báo phương thức được bao gồm trong tệp tiêu đề .h để có thể truy cập được trên nhiều tệp triển khai.
**`Định nghĩa hàm không nội tuyến`** - Các tệp tiêu đề cũng có thể chứa định nghĩa của một phương thức không nội tuyến.
**`Bản đồ thông báo`** - Một tệp tiêu đề cũng có thể chứa các bản đồ thông báo trong trường hợp triển khai mã nguồn MFC. Trong trường hợp như vậy, bản đồ thông báo được liên kết với việc triển khai chức năng được liên kết với các thành phần giao diện người dùng như nút, hộp kiểm, nút radio, v.v.


### Bảo vệ tiêu đề

Các tệp tiêu đề có thể dẫn đến các lỗi phức tạp khi nhiều khai báo được đưa vào cùng một tệp do thêm các tệp tiêu đề khác. Định nghĩa trùng lặp này làm tăng lỗi trình biên dịch. Tình huống có vấn đề này có thể tránh được thông qua một cơ chế được gọi là bảo vệ tiêu đề là các chỉ thị biên dịch có điều kiện như được hiển thị bên dưới.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Với tiêu đề này, bộ tiền xử lý sẽ kiểm tra xem `ANY_UNIQUE_NAME_HERE` đã được xác định chưa. Nếu tiêu đề được đưa vào cùng một tệp nhiều lần, nội dung của tiêu đề sẽ bị bỏ qua.

## Ví dụ tệp H

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## Người giới thiệu

* [Header Filers - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

