{
  "date" : "2021-05-24",
  "keywords" :["rjs", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "RJS", "Tệp Ruby Javascript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RJS - Tệp Javascript của Ruby",
  "description":"Tìm hiểu về định dạng tệp RJS là gì và các API có thể tạo và mở tệp RJS.",
  "linktitle" : "RJS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Tệp RJS là gì?

Tệp có phần mở rộng .rjs là sự kết hợp giữa mã Ruby và JavsScript cho phép các nhà phát triển Rails sử dụng Ruby để tạo mã JavaScript động. Mã Ruby được nhúng trong các hàm Java và được biên dịch trên máy chủ web yêu cầu công cụ Ruby phải chạy trên máy chủ. RJS tương tự như [RHTML](/vi/web/rhtml/); điểm khác biệt duy nhất là phần bên chứa mã Ruby trong [HTML](/vi/web/html/) trong khi nó chứa mã Ruby trong các hàm Javascript.

## Định dạng tệp RJS

Các tệp RJS được mã hóa bằng văn bản thuần túy giống như bất kỳ ngôn ngữ lập trình hoặc tập lệnh nào khác. Khi khách hàng yêu cầu một trang như vậy, mã Ruby được thực thi trên máy chủ và chỉ mã HTML và Javascript được trả về trình duyệt của khách hàng. Cú pháp của tệp RJS tương tự như cú pháp kết hợp cú pháp của Ruby và JavaScript sao cho chỉ mã Ruby được nhúng trong các hàm JavaScript.

### Ví dụ RJS

Ví dụ sau hiển thị một mã Ruby đơn giản một cách độc lập và sau đó được nhúng vào một hàm JavaScript.

```Ruby
### Default Ruby Functions

def foo
  "bar"
end
```

```JavaScript
# JS style which looks like JS

foo = -> { return "bar" }
```
và sau đây là RubyJS:
```Ruby
# here you go!

foo = -> { "bar" }
```
## Người giới thiệu

* [RJS](https://github.com/makevoid/rjs)

