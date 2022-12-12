{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","tệp rhtml", "định dạng tệp rhtml", "loại tệp rhtml", "tệp", "loại", "tệp rhtml là gì" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Trang HTML Ruby",
  "description":"Tìm hiểu về định dạng tệp RHTML và các API có thể tạo và mở tệp RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Tệp RHTML là gì?

Tệp có phần mở rộng .rhtml là tệp [HTML](/vi/web/html/) phía máy chủ chứa mã Ruby hoặc tập lệnh. Mã được thực thi trên máy chủ bằng cách sử dụng Ruby on Rails chạy ở phần phụ trợ. Đối với những người chưa biết về Ruby on Rails, đây là một khung công tác đầy đủ để phát triển các ứng dụng web với cơ sở dữ liệu phụ trợ dựa trên mẫu Model-View-Control. Nói một cách đơn giản, RHTML là sự kết hợp giữa HTML và Ruby, trong đó sức mạnh của lập trình/tập lệnh Ruby có sẵn cho các nhà phát triển web sử dụng các thẻ HTML.

## Định dạng tệp RHTML

Các tệp RHTML được viết ở định dạng văn bản thuần túy giống như bất kỳ tệp web dựa trên văn bản nào khác. Mã được thực thi được đặt trong `<% %>` trong khi đối với đầu ra, mã được viết bên trong các câu lệnh `<%= %>`.

## Ví dụ RHTML

Ví dụ sau sử dụng sự kết hợp đơn giản nhất giữa HTML và Ruby on Rails để xuất tên của từng sản phẩm từ danh sách sản phẩm.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Người giới thiệu

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

