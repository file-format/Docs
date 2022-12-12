{
  "date" : "2021-07-20",
  "keywords" :["MJS", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "Tệp mô-đun Node.js ES"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MJS - Tệp Javascript mô-đun Node.js ES",
  "description" :"Tìm hiểu về tệp MJS là gì và các API có thể tạo và mở tệp MJS.",
  "linktitle" : "MJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-20"
}

## Tệp MJS là gì?

Tệp có phần mở rộng .mjs là tệp mã nguồn JavaScript được sử dụng làm Mô-đun ECMA (Mô-đun ECMAScript) trong các ứng dụng Node.js. Hệ thống mô-đun natvie của Node.js là CommonJS được sử dụng để phân tách mã trong các tệp khác nhau nhằm giữ cho mã [JS](/vi/web/js/) được tổ chức. MJS là cách duy nhất được Node.js sử dụng để xác định xem mô-đun là CommonJS hay ES6. Các mô-đun ECMAScript là biểu mẫu tiêu chuẩn để đóng gói mã JavaScript để tái sử dụng. Các tệp MJS có thể được mở trong các trình soạn thảo văn bản như Atom, Vim, Apple xCode, Microsoft Visual Studio và Notepad.

## Định dạng tệp MJS - Thông tin khác

Các tệp MJS được lưu vào đĩa dưới dạng định dạng văn bản thuần túy theo cú pháp JavaScript. Chúng có thể được mở trong bất kỳ trình soạn thảo văn bản nào và con người có thể đọc được. Kể từ năm 2018, hầu hết tất cả các trình duyệt chính đều hỗ trợ các mô-đun ES.

## Sự khác biệt giữa các mô-đun ES và CommonJS

Vậy điều gì làm cho các tệp MJS khác với các tệp JS đơn giản? Sự khác biệt giữa Mô-đun ES và CommonJS có thể được tóm tắt như sau:

* Không yêu cầu, xuất khẩu hoặc module.exports
* Không có \__filename hoặc \__dirname
* Không tải mô-đun JSON
* Không tải mô-đun gốc
* Không yêu cầu.giải quyết
* Không có NODE_PATH
* Không yêu cầu.extensions
* Không yêu cầu.cache

## Người giới thiệu

* [Node.js ESM](https://nodejs.org/docs/latest/api/esm.html)
* [Sự khác biệt giữa JS và MJS](https://nodejs.org/docs/latest/api/esm.html#esm_differences_between_es_modules_and_commonjs)

