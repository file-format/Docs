{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp TGZ - Tệp Tar được nén",
  "description":"Tìm hiểu về định dạng tệp TGZ và API có thể tạo và mở tệp TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Tệp TGZ là gì?

Tệp có phần mở rộng .tgz là tệp lưu trữ TAR, bao gồm nhiều tệp và thư mục, đã được nén bằng phần mềm nén Gnu Zip (gzip). Tệp [TAR](/vi/compression/tar/) thường kết hợp nhiều tệp thành một tệp duy nhất để sao lưu hoặc phân phối qua internet. Nó là tệp giải nén cho đến khi nó được nén bằng phần mềm gzip, sau đó nó trở thành tệp TGZ. Các tệp TGZ, là các tệp nén, chiếm ít dung lượng trên đĩa hơn và có thể dễ dàng chuyển qua internet qua email. Một số ứng dụng có thể mở tệp TGZ bao gồm WinZip, Tiện ích lưu trữ của Apple, 7-Zip và WinRAR. Các tệp TGZ chủ yếu được sử dụng trong hệ thống UNIX và Linux.

## Định dạng tệp TGZ

Các tệp TGZ được lưu dưới dạng tệp nhị phân được nén bằng thuật toán nén [GZ](/vi/compression/gz/).

## Cách giải nén tệp .tgz trên Linux

Trên Linux/Unix OS, lệnh sau có thể được sử dụng để giải nén các tệp TGZ từ dòng lệnh.

```
tar zxvf tgzCompressedFile.tgz
```

Lệnh trên giải nén tệp TGZ đã nén và giải nén các tệp của tệp lưu trữ TAR vào đĩa.
## Người giới thiệu ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)

