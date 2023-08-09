---
date: 2019-10-11
keywords: py, python, .py, định dạng file py, cách mở file py, cách chạy file py, cách chạy file python, cách chạy python
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp PY
linktitle: PY
description: "Tìm hiểu về định dạng tệp PY và API có thể tạo và mở tệp PY."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## Tệp PY là gì? ##

Tệp có phần mở rộng .py chứa mã nguồn Python. Ngôn ngữ Python đã trở thành ngôn ngữ rất nổi tiếng ngày nay. Nó có thể được sử dụng để viết kịch bản hệ thống, phát triển web và phần mềm và toán học. Python hỗ trợ khả năng tương thích đa nền tảng; có nghĩa là các ứng dụng được phát triển bằng Python có thể hoạt động trên các nền tảng khác nhau như Windows, MAC, Linux, Raspberry Pi, v.v. Python cung cấp một cú pháp đơn giản và dễ đọc tương tự như ngôn ngữ tiếng Anh. Các nhà phát triển có thể viết một ứng dụng phần mềm hợp lý bằng cách viết một vài dòng mã Python. Vì Python chạy trên một hệ thống thông dịch nên mã có thể được thực thi ngay khi nó được viết, điều này rất tốt cho việc tạo nguyên mẫu.

## Lược Sử ##

Python được Guido van Rossum hình thành vào cuối những năm 1980 với tư cách là người kế thừa ngôn ngữ lập trình ABC. Việc triển khai nó bắt đầu vào tháng 12 năm 1989 với Van Rossum là nhà phát triển chính duy nhất. Anh ấy đã làm việc với python cho đến ngày 12 tháng 7 năm 2018. Vào tháng 1 năm 2019, các nhà phát triển cốt lõi của Python tích cực đã bầu ra một "Hội đồng chỉ đạo" gồm 5 thành viên bao gồm Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw và Van Rossum để lãnh đạo dự án.

### Phiên bản ###

- Python 2.0 được phát hành vào ngày 16 tháng 10 năm 2000.
- Python 3.0 được phát hành vào ngày 3 tháng 12 năm 2008.

## Cách chạy tệp py ##

Để kiểm tra phiên bản Python đã cài đặt, bạn có thể sử dụng lệnh sau:

```cmd
python --version
```

Điều này sẽ xuất phiên bản trên bảng điều khiển như

```cmd
Python 3.7.4
```

Nếu Python chưa được cài đặt trên máy của bạn, bạn có thể truy cập [python.org](https://www.python.org/) và tải xuống cũng như cài đặt Python cho hệ điều hành tương ứng của bạn.

Để thực thi tập lệnh Python, bạn có thể sử dụng lệnh sau:

```cmd
python helloworld.py
```

*helloworld.py* là một tệp tập lệnh chứa đoạn mã sau

```py
print("Hello World from Python")
```

Điều này sẽ in phần sau trên cửa sổ giao diện điều khiển.

```cmd
Hello World from Python
```

Lưu ý: Nếu bạn sử dụng IDE, chúng sẽ cung cấp các nút trên màn hình hoặc các phím tắt khác nhau để chạy Python. Ví dụ: một nút phát được hiển thị trong máng xối với trình chỉnh sửa trong PyCharm cho phép bạn thực thi tập lệnh Python.

## Định dạng tệp PY ##

Python được thiết kế để dễ đọc và có những điểm tương đồng với tiếng Anh và Toán. Python sử dụng các dòng mới để biểu thị lệnh hoàn chỉnh thay vì dấu chấm phẩy hoặc dấu ngoặc đơn được sử dụng trong các ngôn ngữ khác. Đối với phạm vi, vòng lặp và hàm, Python dựa vào thụt đầu dòng và khoảng trắng trái ngược với dấu ngoặc nhọn được sử dụng trong các ngôn ngữ khác.

### Cú pháp ###

Sau đây là một ví dụ về cú pháp Python.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Người giới thiệu ##

- [Python (ngôn ngữ lập trình) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

