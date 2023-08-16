---
date: 2019-10-11
keywords: json, .json, định dạng tệp json, cách mở tệp json, ký hiệu đối tượng javascript, định dạng dữ liệu json, định dạng tệp .json
tác giả:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Định dạng tệp JSON - Tệp JSON là gì?
linktitle: JSON
description: "Tìm hiểu về định dạng tệp JSON và các API có thể tạo và mở tệp JSON."
menu:
  docs:
    parent: "web"
lastmod: 2020-04-12
---

## Tệp JSON là gì?

JSON (Ký hiệu đối tượng JavaScript) là một định dạng tệp tiêu chuẩn mở để chia sẻ dữ liệu sử dụng văn bản mà con người có thể đọc được để lưu trữ và truyền dữ liệu. Các tệp JSON được lưu trữ với phần mở rộng .json. JSON yêu cầu ít định dạng hơn và là một giải pháp thay thế tốt cho [XML](/vi/web/xml/). JSON có nguồn gốc từ JavaScript nhưng là định dạng dữ liệu độc lập với ngôn ngữ. Việc tạo và phân tích cú pháp JSON được hỗ trợ bởi nhiều ngôn ngữ lập trình hiện đại. *application/json* là loại phương tiện được sử dụng cho JSON.

## Định dạng tệp JSON - Lịch sử tóm tắt

Cần có giao tiếp giữa máy chủ thời gian thực với máy khách dẫn đến việc tạo JSON. Định dạng JSON lần đầu tiên được chỉ định bởi Douglas Crockford vào tháng 3 năm 2001. JSON dựa trên ECMA-262 Phiên bản thứ 3 tiêu chuẩn—tháng 12 năm 1999, đây là một tập hợp con của JavaScript.

Phiên bản đầu tiên của tiêu chuẩn JSON ECMA-404 đã được xuất bản vào tháng 10 năm 2013 bởi Ecma International. RFC 7159 đã trở thành tài liệu tham khảo chính cho việc sử dụng Internet của JSON vào năm 2014. Vào tháng 11 năm 2017, ISO/IEC 21778:2017 đã được xuất bản dưới dạng tiêu chuẩn quốc tế. RFC 8259 được The Internet Engineering Task Force xuất bản vào ngày 13 tháng 12 năm 2017, đây là phiên bản hiện tại của Tiêu chuẩn Internet STD 90.

## Cấu trúc tệp JSON

Dữ liệu JSON được ghi theo cặp **key/value**. Khóa và giá trị được phân tách bằng dấu hai chấm (:) ở giữa với khóa ở bên trái và giá trị ở bên phải. Các cặp khóa/giá trị khác nhau được phân tách bằng dấu phẩy (,). Khóa là một chuỗi được bao quanh bởi dấu ngoặc kép, ví dụ: "tên". Các giá trị có thể thuộc các loại sau.

- `Số`
- `String`: Dãy ký tự Unicode được bao quanh bởi dấu ngoặc kép.
- `Boolean`: Đúng hoặc Sai.
- `Mảng`: Ví dụ: danh sách các giá trị được bao quanh bởi dấu ngoặc vuông

```json
[ "Táo", "Chuối", "Cam" ]
```

- `Đối tượng`: Tập hợp các cặp khóa/giá trị được bao quanh bởi dấu ngoặc nhọn, chẳng hạn

```json
{"name": "Jack", "age": 30, "favoriteSport" : "Football"}
```

Các đối tượng JSON cũng có thể được lồng vào nhau để thể hiện cấu trúc của dữ liệu. Dưới đây là một ví dụ về đối tượng JSON.

### Ví dụ về định dạng JSON

```json
{
   "name":"Jack",
   "age":30,
   "contactNumbers":[
      {
         "type":"Home",
         "number":"123 123-123"
      },
      {
         "type":"Office",
         "number":"321 321-321"
      }
   ],
   "spouse":null,
   "favoriteSports":[
      "Football",
      "Cricket"
   ]
}
```

## Kích thước tối đa của tệp JSON là bao nhiêu?

Thực tế không có giới hạn về kích thước tối đa của tệp JSON. Nó có thể dài bằng khoảng trống theo yêu cầu của nội dung được lưu trữ.

Khi nói đến việc sử dụng định dạng tệp JSON để truyền dữ liệu qua internet, người ta cần cẩn thận về các tài nguyên sẵn có của máy tính. Nếu dữ liệu JSON lớn được truyền, quá trình truyền sẽ bị ảnh hưởng nếu trình duyệt máy khách có bộ nhớ hạn chế.


Không có giới hạn cố định nào được xác định theo thông số kỹ thuật, nhưng bạn cần cẩn thận để không làm cạn kiệt tài nguyên trên máy tính của người dùng, vì nó sẽ nhanh chóng làm giảm trải nghiệm người dùng của họ và họ có thể sẽ từ bỏ ứng dụng của bạn.

## JSON so với XML

**XML** là một định dạng tệp phổ biến và được sử dụng rộng rãi khác để trao đổi dữ liệu qua internet. Khi nói đến việc trao đổi dữ liệu giữa các ứng dụng, các nhà phát triển có tùy chọn sử dụng cả định dạng tệp XML và JSON. Tuy nhiên, JSON được coi là cách thuận tiện nhất để trao đổi dữ liệu giữa các ứng dụng qua internet vì những lý do sau.

1. JSON cung cấp chế độ xem dữ liệu rõ ràng và dễ đọc hơn so với các định dạng tệp XML
1. JSON giảm chi phí truyền dữ liệu qua internet vì nó có ít ký tự hơn để xác định cùng một bộ dữ liệu so với XML
1. Các ngôn ngữ lập trình hiện đại cung cấp trình phân tích cú pháp dựng sẵn để phân tích cú pháp phản hồi JSON trên web.

## Bạn có biết không?

Bạn có thể trở thành người đóng góp tại FileFormat.com để giữ cho cộng đồng định dạng tệp được cập nhật với những phát hiện của bạn. Nếu bạn phải chia sẻ bất kỳ điều gì về định dạng tệp JSON hoặc tệp Web, bạn có thể đăng phát hiện của mình trong phần [Tin tức về định dạng tệp web](https://news.fileformat.com/t/Web) để mọi người tìm hiểu thêm về các định dạng này.

## Người giới thiệu

- [JSON - Wikipedia](https://en.wikipedia.org/wiki/CSS)
- [Giới thiệu về JSON](https://www.digitalocean.com/community/tutorials/an-introduction-to-json)

