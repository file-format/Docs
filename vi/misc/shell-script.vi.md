{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell script - Cách chạy nó trên Ubuntu và Linux",
  "description":"Tìm hiểu Shell Script là gì và cách chạy nó trên Ubuntu và Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-vi",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## Tập lệnh Shell là gì?

Tập lệnh Shell bao gồm việc viết một loạt lệnh trong một tệp văn bản thuần túy, thường được gọi là **Shell Script**. Các tập lệnh này được thực thi bởi shell, đây là trình thông dịch dòng lệnh. Các vỏ phổ biến nhất bao gồm

1. Bash (Bourne Again Shell)
2. Zsh (Vỏ Z)
3. Cá.

Các tập lệnh Shell có thể bao gồm từ các dòng lệnh đơn giản đến các chương trình phức tạp và chúng được sử dụng để thực hiện nhiều tác vụ khác nhau, chẳng hạn như thao tác với tệp, quản trị hệ thống và tự động hóa các tác vụ lặp đi lặp lại.

## Lợi ích của Shell Scripting:

1.  **Tự động hóa:** Tập lệnh Shell cho phép người dùng tự động hóa các tác vụ lặp đi lặp lại, tiết kiệm thời gian và giảm nguy cơ xảy ra lỗi do con người.
    
2.  **Tùy chỉnh:** Người dùng có thể tạo tập lệnh phù hợp với nhu cầu cụ thể của họ, mang lại mức độ tùy chỉnh cao.
    
3.  **Xử lý hàng loạt:** Tập lệnh Shell rất tuyệt vời để xử lý các tác vụ xử lý hàng loạt, trong đó nhiều lệnh cần được thực thi theo trình tự.
    
4.  **Quản trị hệ thống:** Tập lệnh Shell thường được sử dụng cho các tác vụ quản trị hệ thống, chẳng hạn như sao lưu, xoay vòng nhật ký và cài đặt phần mềm.

## Viết một tập lệnh Shell đơn giản:

Hãy tạo một tập lệnh shell cơ bản để in tin nhắn chào mừng. Mở trình soạn thảo văn bản và tạo một tệp có tên `greeting.sh`. Thêm các dòng sau:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Lưu tệp và làm cho nó có thể thực thi được bằng cách chạy lệnh sau trong thiết bị đầu cuối:

```
chmod +x greeting.sh
```

Bây giờ, bạn có thể thực thi tập lệnh:

```
./greeting.sh
```

Đầu ra phải là:

```
Hello, welcome to the world of shell scripting!
```

## Chạy Shell Script trên Ubuntu và Linux:

Bây giờ, chúng ta sẽ thảo luận **cách chạy tệp .sh trong Ubuntu và Linux**.

1.  **Làm cho tập lệnh có thể thực thi được:** Trước khi chạy tập lệnh shell, hãy đảm bảo tập lệnh đó có thể thực thi được. Sử dụng lệnh `chmod` như được hiển thị trước đó.
    
2.  **Điều hướng đến Thư mục tập lệnh:** Mở một thiết bị đầu cuối và sử dụng lệnh `cd` để điều hướng đến thư mục chứa tập lệnh shell của bạn.
    
3.  **Chạy tập lệnh:** Thực thi tập lệnh bằng cách nhập `./scriptname.sh` trong terminal, thay thế scriptname bằng tên thật của tập lệnh của bạn.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Sử dụng Lệnh Bash:** Nếu tập lệnh của bạn bắt đầu bằng `#!/bin/bash` (được gọi là **shebang**), bạn cũng có thể chạy tập lệnh đó bằng lệnh `bash`.

```
bash greeting.sh
```

## $@ có nghĩa là gì trong Shell Script?

Trong tập lệnh shell, `$@` đại diện cho tất cả các đối số dòng lệnh được truyền cho tập lệnh. Nó thường được sử dụng để tham chiếu danh sách các đối số dưới dạng các thực thể riêng biệt. Khi được sử dụng trong dấu ngoặc kép, như `$@`, nó giữ nguyên các đối số riêng lẻ, tính đến khoảng trắng và ký tự đặc biệt.

Đây là lời giải thích ngắn gọn:

- `$@`: Đại diện cho tất cả các tham số vị trí (đối số) được truyền cho tập lệnh hoặc hàm. Mỗi đối số được coi là từ riêng biệt.
    
- `$@`: Khi được trích dẫn kép, giữ nguyên sự phân tách các đối số, cho phép khoảng trắng hoặc ký tự đặc biệt trong các đối số riêng lẻ.
    

Đây là ví dụ đơn giản để minh họa:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Ví dụ: khi bạn chạy tập lệnh này với các đối số:

```
bash example.sh arg1 "argument 2" arg3
```

Nó sẽ xuất ra:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Như bạn có thể thấy, `$@` đại diện cho tất cả các đối số và `$@` giữ nguyên các đối số riêng lẻ, ngay cả khi chúng chứa khoảng trắng.

