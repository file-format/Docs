{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tạo tệp - Tệp tập lệnh Xcode Makefile",
  "description":"Tìm hiểu về Định dạng XCode MakeFile và các API có thể tạo và mở tệp MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Tệp MAKE là gì?

Tệp MAKE là tệp tập lệnh XCode tổ chức biên dịch mã. Nó được sử dụng để biên dịch và liên kết các chương trình từ nhiều tệp mã nguồn. Điều này giúp quyết định phần nào của một ứng dụng lớn được yêu cầu biên dịch lại khi ứng dụng cần được cập nhật. Tạo tệp sử dụng một loạt hướng dẫn để chạy tùy thuộc vào tệp nào đã thay đổi.

## Ví dụ định dạng tệp MAKE

Các nội dung sau đây được thực thi bằng tiện ích Make và kết quả đầu ra như sau.

```
hello:
	echo "hello world"
```
**Tạo đầu ra**

```
$ make
echo "hello world"
hello world
```

## Người giới thiệu
* [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
* [Hướng dẫn đối tượng-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

