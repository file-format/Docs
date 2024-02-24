{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp PC - Tệp mã nguồn Pro*C - Tệp .pc là gì và làm cách nào để mở tệp?",
  "description" : "Tìm hiểu về Tệp Mã Nguồn PC Pro*C và cách mở tệp đó.",
  "linktitle" : "PC",
  "menu" : {
    "docs" : {
      "identifier" : "programming-en-pc-vi",
      "parent" : "programming"
}
},
  "lastmod" : "2024-02-08"
}

## Tập tin PC là gì?

Tệp PC hoặc tệp .pc là tệp mã nguồn ProC. ProC là một trình biên dịch trước được sử dụng với cơ sở dữ liệu Oracle để nhúng các câu lệnh SQL vào mã C hoặc C++. Khi bạn biên dịch tệp Pro*C, nó sẽ tạo mã C hoặc C++ thông thường với các lệnh SQL được nhúng. Điều này cho phép bạn tích hợp liền mạch các hoạt động cơ sở dữ liệu SQL với các chương trình C hoặc C++ của bạn.

Đây là ví dụ cơ bản về hình thức của tệp Pro*C:

```
#include <stdio.h>
#include <sqlca.h>

EXEC SQL INCLUDE sqlca;

int main() {
    EXEC SQL BEGIN DECLARE SECTION;
    int emp_id;
    char emp_name[50];
    EXEC SQL END DECLARE SECTION;

    /* Connect to database */
    EXEC SQL CONNECT :user IDENTIFIED BY :password;

    /* Fetch employee details */
    EXEC SQL SELECT employee_id, employee_name INTO :emp_id, :emp_name FROM employees WHERE employee_id = :input_id;

    /* Print fetched details */
    printf("Employee ID: %d\n", emp_id);
    printf("Employee Name: %s\n", emp_name);

    /* Disconnect from database */
    EXEC SQL COMMIT WORK RELEASE;
    return 0;
}
```

Trong ví dụ này, các câu lệnh SQL có tiền tố EXEC SQL để chỉ ra rằng chúng là các câu lệnh SQL được nhúng. Các câu lệnh này sẽ được trình biên dịch trước Pro*C xử lý khi tệp được biên dịch và mã C thích hợp sẽ được tạo để tương tác với cơ sở dữ liệu Oracle.

## Làm cách nào để mở tập tin PC?

Để mở tệp PC, bạn thường cần trình soạn thảo văn bản hoặc Môi trường phát triển tích hợp (IDE) hỗ trợ chỉnh sửa mã nguồn C hoặc C++. Dưới đây là một số tùy chọn phổ biến:

1.  **Trình soạn thảo văn bản:**
    
- **Notepad** (Windows)
- **Chỉnh sửa văn bản** (Mac)
- **gedit** (Linux)
- **Văn bản tuyệt vời**
- **Nguyên tử**
- **Mã Visual Studio**
2.  **Môi trường phát triển tích hợp (IDE):**
    
- **Nhật thực** với CDT (Công cụ phát triển C/C++)
- **Visual Studio** với Visual C++ hoặc Visual Studio Code với phần mở rộng C++
- **Mã::Khối**
- **NetBeans** với gói C/C++
  
## Người giới thiệu
* [Pro*C](https://en.wikipedia.org/wiki/Pro*C)


