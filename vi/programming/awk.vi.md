{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp AWK - Tệp tập lệnh AWK",
  "description":"Tìm hiểu về định dạng tệp AWK và API có thể tạo và mở tệp AWK.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Tệp AWK là gì?

Tệp AWK là tệp tập lệnh được tạo cho ứng dụng xử lý văn bản **AWK** đi kèm với hệ điều hành Unix và Linux. Nó chứa các hướng dẫn hợp lý để thực hiện các hành động trên văn bản hoặc nội dung của tệp như khớp, thay thế và in văn bản. Điều này giúp tạo báo cáo và văn bản được định dạng từ tệp đầu vào. Tiện ích awk thường nằm trong /usr/bin/awk trên hầu hết các bản phân phối linux/unix.

## Làm cách nào để tạo tập lệnh AWK?

Một tệp AWK có thể được tạo hoặc mở trong bất kỳ trình soạn thảo văn bản nào trên Linux/Unix OS. Có thể tạo tệp tập lệnh AWK mới như sau.

```
$ vi script.awk
```

Thao tác này sẽ mở tệp AWK trong trình soạn thảo văn bản. Nhập một số báo cáo trong trình soạn thảo văn bản như sau.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Dòng đầu tiên của nội dung văn bản này được giải thích như sau.

* \#! – được gọi là `Shebang`, chỉ định trình thông dịch cho các hướng dẫn trong tập lệnh
* /usr/bin/awk – là trình thông dịch
* -f – tùy chọn trình thông dịch, được sử dụng để đọc tệp chương trình

## Làm cách nào để thực thi tập lệnh AWK?

Lưu tệp và làm cho tập lệnh có thể thực thi được bằng cách ban hành lệnh bên dưới:
```
$ chmod +x script.awk
```

Kịch bản sau đó có thể được chạy như sau.

```
$ ./script.awk
```

dẫn đến đầu ra sau đây.

```
Writing my first Awk executable script!
```

## Tài liệu tham khảo ##

* [Viết tập lệnh bằng ngôn ngữ lập trình Awk](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

