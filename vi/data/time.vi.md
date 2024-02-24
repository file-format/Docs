{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp TIME - Tệp .time là gì? Thời điểm tệp được tạo trong Linux",
  "description" : "Tìm hiểu về tệp TIME và tìm hiểu Thời gian khi tệp được tạo trong Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-vi",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Tệp THỜI GIAN là gì?

Định dạng tệp TIME đã được hệ thống web có tên LIGHT sử dụng, hệ thống này giúp người dùng ghi lại, sắp xếp và chia sẻ cuộc sống của họ. Về cơ bản, nó lưu trữ một tập hợp các bài đăng và đại diện cho một thư mục trên trang đời sống của người dùng trong hệ thống.

## Cách tìm hiểu thời điểm tệp được tạo trong Linux

Trong Linux, bạn có thể sử dụng lệnh `stat` để tìm hiểu thời điểm tệp được tạo. Đây là cách bạn có thể làm điều đó:

Mở một terminal và gõ lệnh sau:

```
stat <file_path>
```

Thay thế `<file_path> ` với đường dẫn tới file bạn quan tâm. Ví dụ:

```
stat /path/to/your/file.txt
```

Lệnh này sẽ hiển thị nhiều thông tin khác nhau về tệp, bao gồm cả thời gian tạo tệp. Tìm dòng bắt đầu bằng Birth hoặc File:. Thời gian Sinh cho biết thời điểm tệp được tạo trên hệ thống tệp.

Đây là một ví dụ về kết quả đầu ra có thể trông như thế nào:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Trong ví dụ này, thời gian Sinh cho biết thời điểm tệp được tạo.

