{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "tệp", "phần mở rộng", "định dạng tệp", "triển khai erb", "Hướng dẫn lập trình", "ví dụ erb", "eRuby", "định dạng tệp eRuby", "tập lệnh ngôn ngữ eRuby", " mẫu eRuby", "ngôn ngữ erb", "ngôn ngữ ERB Ruby", "ngôn ngữ eRuby" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - Tệp ngôn ngữ eRuby",
  "description":"Tìm hiểu về định dạng tệp ERB và các API có thể tạo và mở tệp ERB.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## Tệp ERB là gì?

Ngôn ngữ eRuby là một hệ thống khuôn mẫu nhúng Ruby vào một tài liệu văn bản. Hệ thống tạo khuôn mẫu của eRuby kết hợp mã ruby và văn bản đơn giản để cung cấp khả năng kiểm soát luồng và thay thế có thể thay đổi, do đó giúp dễ dàng bảo trì. Nó thường được sử dụng để nhúng mã Ruby vào một tài liệu [HTML](/vi/web/html/), tương tự như АSР, [JSР](/vi/programming/jsp/) và [РHР](/vi/programming/php/) và máy chủ khác -side sсripting ngôn ngữ. ERB Ruby thường tạo các trang Web.

Mô-đun chế độ xem của Ruby on Rails chịu trách nhiệm hiển thị phản hồi hoặc đầu ra trên một trình duyệt. Ở dạng đơn giản nhất, một chế độ xem có thể là một đoạn mã HTML có một số nội dung thống kê. Đối với hầu hết các ứng dụng, chỉ có nội dung thống kê có thể không đủ. Nhiều ứng dụng Rails sẽ yêu cầu nội dung động do bộ điều khiển tạo ra để được hiển thị trong chế độ xem của họ. Điều này có thể thực hiện được bằng cách sử dụng Embedded Ruby để tạo các mẫu có thể chứa nội dung động.

Embedded Ruby cho phép mã ruby được nhúng trong một tài liệu dạng xem. Mã này được thay thế bằng giá trị phù hợp do việc thực thi mã trong thời gian chạy. Tuy nhiên, bằng cách có khả năng nhúng mã vào một tài liệu xem, chúng tôi có nguy cơ bắc cầu cho sự phân tách rõ ràng hiện có trong khung MVС. Do đó, trách nhiệm của nhà phát triển là đảm bảo rằng có sự phân chia trách nhiệm rõ ràng giữa mô hình, chế độ xem và bộ điều khiển mô-đun của ứng dụng.



## Lược Sử ##

Ruby được thiết kế vào giữa những năm 1990 bởi Yukihiro Matsumоtо. Yukihirо Matsumоtо là cha đẻ của Ruby và trong cộng đồng Ruby, ông nổi tiếng với cái tên Matz'. Tập lệnh Ruby lần đầu tiên được giới thiệu vào năm 1995 và phiên bản đầu tiên của Ruby là Ruby 95 được phát hành vào năm 1995.

Yukihirо Matsumоtо muốn có một ngôn ngữ lập trình hướng đối tượng đầy đủ có thể dễ dàng sử dụng như một ngôn ngữ viết kịch bản. Vì vậy, anh ấy đã thiết kế ngôn ngữ eRuby. Trong một phiên trò chuyện của Yukihirо Matsumоtо và Keiju Ishitsukа, hai cái tên đã được gia nhập vì ngôn ngữ lập trình là "Соral" và "Ruby", sau đó Yukihirо Matsumоtо đã chọn tên là "Ruby".


## Đặc điểm kỹ thuật ##

Định dạng tệp eRuby hỗ trợ các khái niệm khác nhau về lập trình hướng đối tượng theo hướng đối tượng như lớp, tính kế thừa, tính trừu tượng, tính toán và mã hóa, v.v. Tính năng của chương trình lập trình hướng đối tượng giúp cho việc bảo trì và phát triển trở nên dễ dàng. Tập lệnh ngôn ngữ eRuby cũng hỗ trợ tính năng của một chương trình lập trình thủ công. Trong lập trình theo thủ tục, có các bước cụ thể cho mỗi chương trình để giải quyết một vấn đề cụ thể.

Các mẫu eRuby cung cấp một phạm vi rộng lớn gồm các thư viện tích hợp phong phú với các lớp mà các lập trình viên có thể phát triển bất kỳ ứng dụng web hoặc chương trình nào một cách dễ dàng và nhanh chóng. eRuby là một ngôn ngữ lập trình có mục đích chung hoặc đa mục đích, có nghĩa là nó có thể được các lập trình viên sử dụng để phát triển các loại ứng dụng và chương trình khác nhau.

Ngôn ngữ ERB Ruby là ngôn ngữ lập trình mã nguồn đơn giản và mã nguồn mở và bạn cũng có thể sửa đổi nó theo yêu cầu của dự án. Nó cung cấp nhiều loại tính năng và công cụ tích hợp sẵn phong phú. Ngôn ngữ cũng cung cấp tính năng của bộ thu gom rác tự động.

Viết mã trong eRuby rất nhanh so với các ngôn ngữ lập trình khác. Và nó cũng là một ngôn ngữ lập trình linh hoạt vì nó cho phép mọi người dùng sửa đổi các phần của nó theo yêu cầu của họ. Nó hỗ trợ tính năng kế thừa và mixin duy nhất, đồng thời cung cấp tính năng gõ động cho người dùng. eRuby là một ngôn ngữ lập trình nhạy cảm và có một cộng đồng hỗ trợ tuyệt vời vì tính nhạy cảm của nó.


## Ví dụ về định dạng tệp ERB ##

Sau đây là các loại thẻ trong mẫu ERB:

### Biểu hiện ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Chấp hành ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### Bình luận ###

```
<%# %>
```

```
<%# ruby code %>
```

### Thẻ khác ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Ví dụ lớp ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## Tài liệu tham khảo ##

* [ERB - theo Wikipedia](https://en.wikipedia.org/wiki/ERuby)



