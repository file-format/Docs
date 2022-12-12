{
  "date" : "2021-07-29",
  "keywords" :[ "tệp md5", "định dạng tệp md5", "tệp md5 là gì", "tệp", "ví dụ md5", "phần mở rộng tệp md5","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - Tệp tổng kiểm tra MD5",
  "description":"Tìm hiểu về tệp MD5 và các API có thể tạo và mở tệp MD5.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Tệp MD5 là gì?

Tệp MD5 là tệp tổng kiểm tra được sử dụng để xác minh tính toàn vẹn của tệp. Nó tương tự như dấu vân tay cho tệp được liên kết và được tạo duy nhất bằng cách sử dụng thuật toán sử dụng số lượng bit trong tệp. Nó được sử dụng để xác minh tệp bằng phần mềm như [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). Một ưu điểm của việc sử dụng các tệp MD5 là xác minh rằng các tệp đã tải xuống không bị hỏng.

## Định dạng tệp MD5 - Thông tin khác

Thông thường, tệp MD5 được lưu với cùng tên với tên tệp gốc nhưng có phần mở rộng .md5. Ví dụ: nếu tên tệp được liên kết là `abc_987_123456.grb`, thì tên tệp MD5 tương ứng sẽ là `abc_987_123456.grb.md5`. Các tệp MD5 giúp xác định rằng tệp đã nhận hoặc tải xuống không bị hỏng hoặc bị ảnh hưởng bởi nội dung độc hại. Nói tóm lại, các tệp MD5 đảm bảo tính đầy đủ của một tệp.


## Làm cách nào để kiểm tra Tổng kiểm tra MD5?

Có thể kiểm tra/xác minh một tệp cho MD5 bằng cách sử dụng công cụ [md5sum](https://en.wikipedia.org/wiki/Md5sum) như sau.

```
md5sum -c abc_987_123456.grb.md5
```

## Người giới thiệu

* [md5sum - Wikipedia](https://vi.wikipedia.org/wiki/Md5sum)

