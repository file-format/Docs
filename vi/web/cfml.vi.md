{
  "date" : "2021-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFML - Tệp ngôn ngữ đánh dấu ColdFusion",
  "description" :"Tìm hiểu về tệp CFML là gì và các API có thể tạo và mở tệp CFML.",
  "linktitle" : "CFML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-19"
}

## Tệp CFML là gì?

Tệp có phần mở rộng .cfml là tệp Ngôn ngữ đánh dấu ColdFusion được sử dụng để tạo trang web. Nó đề cập đến một bộ quy tắc được sử dụng để xác định cách lập trình viên sẽ phát triển ứng dụng ColdFusion. ColdFusion là ngôn ngữ lập trình được sử dụng để tạo các ứng dụng web phía máy chủ một cách nhanh chóng và tốn ít công nghệ hơn các công nghệ khác như [ASP](/vi/web/asp/), [PHP](/vi/web/php/), v.v. Một số trong số các ứng dụng có thể mở tệp CML bao gồm Adobe ColdFusion 2018, Adobe ColdFusion Builder và Adobe Dreamweaver.

## Định dạng tệp CFML - Thông tin khác

Các tệp CFML là các tệp đánh dấu và chứa các phần tử web ở dạng thẻ. Đây là những tệp văn bản có thể được mở và chỉnh sửa trong bất kỳ trình soạn thảo văn bản nào. Tệp CFML bao gồm một số thẻ tương tự như [HTML](/vi/web/html/) và thường bao gồm thẻ mở và thẻ đóng. Các thẻ này cũng có thể chứa một hoặc nhiều thuộc tính.

### Cú pháp thẻ

Sau đây là cú pháp tổng quát của các thẻ CFML.

```
<tagname>
  Code/text that is affected by the surrounding tags.
</tagname>
```

Hầu hết các thẻ chấp nhận các thuộc tính và được định nghĩa như sau.

```
<tagname attribute="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

Một số thẻ này cũng chấp nhận nhiều thuộc tính với cú pháp sau.

```
<tagname attribute1="value" attribute2="value">
  Code/text that is affected by the surrounding tags.
</tagname>
```

## Ví dụ mã CFML

Đây là một ví dụ sử dụng thẻ CFML thực tế - thẻ `cfoutput`:

```
<cfoutput>
  #firstname#
</cfoutput>
```

## Người giới thiệu

* [ColdFusion](https://www.quackit.com/coldfusion/tutorial/)

