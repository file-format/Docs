{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp CJS - Tệp mã CommonJS",
  "description":"Tệp .cjs là gì và làm cách nào để mở nó?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## Tệp CJS là gì?

Tệp CommonJS (CJS) là tệp chứa mã JavaScript được viết bằng cú pháp CommonJS. CommonJS là một hệ thống mô-đun được thiết kế để hoạt động trong các môi trường ngoài trình duyệt web giao diện người dùng và nó thường được sử dụng trong môi trường JavaScript phía máy chủ, như Node.js.

## Định dạng tệp CJS - Thông tin thêm

Các tệp CJS được viết bằng cú pháp CommonJS và có thể được chỉnh sửa trong bất kỳ trình soạn thảo văn bản nào như Microsoft Notepad hoặc Apple TextEdit. Các mô-đun CommonJS thường được lưu trữ trong các tệp riêng biệt và nhằm mục đích đóng gói và mô-đun hóa mã để tổ chức và bảo trì tốt hơn. Các mô-đun này sử dụng hàm bắt buộc để nhập các phần phụ thuộc và đối tượng module.exports hoặcexports để hiển thị các giá trị và hàm mà các phần khác của mã có thể sử dụng.

## Ví dụ về mã CJS

Các mô-đun CommonJS có cú pháp và cấu trúc cụ thể bao gồm các tính năng như hàm cần thiết để nhập các mô-đun khác và module.exports hoặc xuất các đối tượng để xuất các giá trị, hàm hoặc đối tượng từ một mô-đun. Các mô-đun này được sử dụng để đóng gói và phân tách các đoạn mã, giúp quản lý và duy trì các cơ sở mã JavaScript lớn dễ dàng hơn. Đây là một ví dụ cơ bản về mô-đun CommonJS:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## Người giới thiệu

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)
