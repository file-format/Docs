{
  "date" : "2021-04-08",
  "keywords" :[ "tệp dar", "định dạng tệp dar", "tệp dar là gì", "tệp", "ví dụ về dar", "phần mở rộng tệp dar","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Định dạng tệp trình lưu trữ đĩa",
  "description":"Tìm hiểu về định dạng tệp DAR và API có thể tạo và mở tệp DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Tệp DAR là gì?

Một tệp có phần mở rộng .dar là một kho lưu trữ nén được tạo bằng cách sử dụng kho lưu trữ Đĩa DAR. Nó có thể tạo bản sao lưu/lưu trữ cho toàn bộ đĩa hoặc một nhóm tệp. Nó được tạo ra để thay thế định dạng tệp [TAR](/vi/compression/tar/) trên hệ điều hành UNIX và có thể được tạo dưới dạng tệp lưu trữ chia nhỏ cho số lượng tệp lớn. Kho lưu trữ DAR hỗ trợ tùy chọn xóa các tệp khỏi hệ thống được liên kết với các tệp chính trong kho lưu trữ. Khả năng cung cấp sao lưu chênh lệch, tăng dần và giảm dần của nó làm cho nó vượt trội hơn các tệp TAR.

## Định dạng tệp DAR

Các tệp DAR là các tệp lưu trữ được nén có thể sử dụng bất kỳ kiểu nén trên mỗi tệp nào, chẳng hạn như [gzip](/vi/compression/gz/), [bzip2](/vi/compression/bz2/), lzo, xz hoặc lzma. Định dạng tệp chính xác của tệp DAR tùy thuộc vào loại định dạng được sử dụng để nén nội dung của kho lưu trữ. Nó cũng cho phép mã hóa tùy chọn Blowfish, Twofish, AES, Serpent, Camellia cũng như mã hóa và chữ ký khóa công khai (OpenPGP).

### Tính năng DAR

Một số tính năng của định dạng tệp DAR như sau.

* Xử lý bất kỳ loại inode nào (thư mục, tệp đơn giản, liên kết tượng trưng, thiết bị đặc biệt, đường ống có tên, ổ cắm, cửa ra vào, ...)
* Chăm sóc các inode được liên kết cứng (tệp đơn giản được liên kết cứng, thiết bị char, thiết bị khối, liên kết tượng trưng được liên kết cứng)
* Chăm sóc các tập tin thưa thớt
* Chăm sóc các thuộc tính mở rộng của tệp Linux,
* Chăm sóc tệp Linux ACL
* Xử lý các nhánh tệp Mac OS X
* Quản lý một số thuộc tính cụ thể của hệ thống tệp như Ngày sinh của hệ thống tệp HFS + và các thuộc tính không thay đổi, ghi nhật ký dữ liệu, xóa an toàn, không hợp nhất đuôi, không thể xóa, không có thời gian của hệ thống tệp ext2/3/4.
* Nén từng tệp với gzip, bzip2, lzo, xz hoặc lzma (trái ngược với nén toàn bộ kho lưu trữ). Một cá nhân có thể chọn không nén các tệp đã được nén dựa trên hậu tố tên tệp của họ.
* Giải nén nhanh các tệp từ mọi nơi trong kho lưu trữ
* Liệt kê nhanh nội dung kho lưu trữ thông qua việc lưu danh mục tệp trong kho lưu trữ
* Sao lưu hệ thống tệp trực tiếp: phát hiện khi tệp đã được sửa đổi trong khi tệp được đọc để sao lưu và có thể thử lưu lại tệp đó với số lần thử lại tối đa nhất định
* Tệp băm (MD5, SHA1 hoặc SHA-512) được tạo trực tiếp cho mỗi lát cắt, tệp kết quả tương thích với md5sum hoặc sha1sum, để có thể nhanh chóng kiểm tra tính toàn vẹn của từng lát cắt
* Độc lập với hệ thống tập tin: nó có thể được sử dụng để khôi phục hệ thống về một phân vùng có kích thước khác và/hoặc một phân vùng có hệ thống tập tin khác[5]

## Người giới thiệu

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

