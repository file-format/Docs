{
  "date" : "2022-02-17",
  "keywords" :["tệp gpg", "định dạng tệp gpg", "tệp gpg là gì", "tệp", "ví dụ gpg", "phần mở rộng tệp gpg","phần mở rộng", "định dạng"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp GPG - Tệp khóa công khai bảo vệ quyền riêng tư của GNU",
  "description":"Tìm hiểu về tệp GPG và API có thể tạo và mở tệp GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Tệp GPG là gì?

Tệp GPG là tệp khóa mã hóa/giải mã được chương trình mã hóa GNU Privacy Guard (GnuPG) sử dụng. Bản thân chương trình GnuPC dựa trên tiêu chuẩn OpenPGP như RFC4880 đã định nghĩa và còn được gọi là PGP. Chìa khóa để sử dụng thành công GPG trong hệ điều hành hiện đại là hệ thống quản lý khóa linh hoạt của nó. Tiện ích dòng lệnh của GPG cho phép nó dễ dàng tích hợp với các ứng dụng khác.

## Định dạng tệp GPG

Các tệp GPG được lưu dưới dạng tệp nhị phân được mã hóa và tất nhiên chúng không thể đọc được. Để giải mã tệp GPG được mã hóa, bạn cần sử dụng cùng một khóa bảo mật. Và đó là lý do tại sao định dạng tệp nội bộ của các tệp này không được biết đến.

## Mã hóa và giải mã tệp bằng GPG trên Linux

Tiện ích dòng lệnh GPG có thể được sử dụng để mã hóa và giải mã các tệp trên Linux.

### Mã hóa tệp

Một tệp có thể được mã hóa bằng lệnh gpg với tùy chọn -c (tạo) như hình bên dưới.

```
gpg -c file1.txt
```
Chạy lệnh này sẽ yêu cầu một cụm từ khóa để mã hóa nội dung của tệp gốc `file1.txt`. Điều này dẫn đến việc tạo tệp được mã hóa file1.txt.gpg.

### Giải mã và giải nén tệp

Để giải mã và trích xuất một tệp được mã hóa, có thể sử dụng lệnh sau.

```
gpg cfile.txt.gpg
```

## Người giới thiệu

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

