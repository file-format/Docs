{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "tệp", "phần mở rộng", "định dạng tệp", "triển khai hta", "Hướng dẫn lập trình", "ví dụ hta", "Ứng dụng HTML", "Ứng dụng ngôn ngữ đánh dấu siêu văn bản", "tệp HTA", "Ứng dụng HTML của Microsoft"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - Tệp ứng dụng HTML",
  "description":"Tìm hiểu về định dạng tệp HTA và các API có thể tạo và mở tệp HTA.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## Tệp HTA là gì?

HTMLA là viết tắt của **Ứng dụng ngôn ngữ đánh dấu siêu văn bản** là một chương trình tương thích với Microsoft Windows. Mã nguồn của chương trình này bao gồm nhiều hơn một ngôn ngữ kịch bản chẳng hạn như [HTML](/vi/web/html/) và [JavaScript](/vi/web/js/). Đối với giao diện người dùng, Ứng dụng HTML được ưu tiên hơn trong khi để đáp ứng yêu cầu logic của chương trình, bất kỳ ngôn ngữ kịch bản nào khác đều được sử dụng.

Ứng dụng HTML độc lập với mô hình bảo mật của trình duyệt internet và chạy như một ứng dụng hoàn toàn đáng tin cậy. Phần mở rộng được sử dụng cho các tệp liên quan đến các ứng dụng này là HTA. Các ứng dụng này bao gồm các tính năng của HTML cùng với các thuộc tính của các ngôn ngữ kịch bản khác.


## Lược Sử ##

HTA được Microsoft giới thiệu lần đầu tiên vào năm 1999 cùng với việc phát hành Internet Explorer 5. Nó tương thích với Internet Explorer và do đó chỉ có thể được thực thi trên hệ điều hành Windows. Công nghệ này đã được cấp bằng sáng chế vào năm 2003. Các tệp HTA được thực thi tương tự như bất kỳ tệp .exe nào khác. Các tệp HTA cũng tương thích với phiên bản cập nhật hiện nay của Windows 11.


## Đặc điểm kỹ thuật ##

HTA có định dạng giống như bất kỳ trang HTML nào khác bao gồm, trong khi một số thuộc tính được sử dụng để kiểm soát kiểu đường viền hoặc biểu tượng của chương trình. Hơn nữa, các đối số được cung cấp cho việc khởi chạy HTA. Các ứng dụng này có thể được thực thi bằng chương trình có tên mshta.exe. Nó có thể được truy cập bằng cách nhấp đúp vào tệp. Các chương trình này tự động chạy cùng với Internet explorer. Bên cạnh các thông số kỹ thuật khác, chúng không độc lập với trình duyệt công cụ Trident mà độc lập với Internet Explorer. Điều đó có nghĩa là chúng có thể được thực thi mà không cần sử dụng Internet Explorer.

Các thẻ được sử dụng để tùy chỉnh giao diện của các ứng dụng này. Việc chuyển đổi từ ứng dụng HTML của Microsoft sang định dạng HTA dễ dàng hơn tức là bạn chỉ cần thay đổi phần mở rộng. Như chúng ta biết rằng các ứng dụng này hoàn toàn đáng tin cậy nên chúng bao gồm nhiều tính năng và ưu điểm hơn so với các tệp HTML đơn giản. Trình soạn thảo văn bản có thể được sử dụng để tạo HTA. Microsoft hoặc bất kỳ nguồn đáng tin cậy nào khác có thể mua các trình chỉnh sửa này.


## Ví dụ về định dạng tệp HTA ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Tài liệu tham khảo ##

* [HTA - theo Wikipedia](https://en.wikipedia.org/wiki/HTML_Application)



