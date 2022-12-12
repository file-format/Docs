{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CDF - Định dạng định nghĩa kênh",
  "description" :"Tìm hiểu về tệp CDF là gì và các API có thể tạo và mở tệp CDF.",
  "linktitle" : "CDF",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-18"
}

## Tệp CDF là gì?

Tệp có phần mở rộng .cdf là định dạng tệp phân phối thông tin dựa trên XLM được sử dụng để xuất bản các bản cập nhật thường xuyên dưới dạng "kênh". Thông tin được xuất bản từ bất kỳ máy chủ web nào và được tự động gửi đến các máy tính có chương trình nhận tương thích như trình duyệt web. Người dùng đăng ký các kênh đang hoạt động và có các bản cập nhật theo lịch trình được gửi đến máy tính để bàn của họ.
Các tệp CDF trước đây được sử dụng cùng với các công nghệ Active Channel, Active Desktop và Smart Offline Favorites của Microsoft.

## Định dạng tệp CDF

Các tệp CDF được lưu dưới dạng tệp XML là định dạng tệp web chung để trao đổi thông tin. Định dạng tệp CDF hiện là định dạng cũ và chưa bao giờ được áp dụng rộng rãi. So với điều này, RSS của Netscape nổi tiếng hơn và được sử dụng rộng rãi hơn.

### Ví dụ về định dạng tệp CDF

Sau đây là ví dụ chung về định dạng tệp CDF.

```
<?xml version="1.0" encoding="UTF-8"?>
<CHANNEL HREF="http://domain/folder/pageOne.extension"
BASE="http://tên miền/thư mục/"
LASTMOD="1998-11-05T22:12"
PRECACHE="CÓ"
CẤP = "0">
<TITLE>Tiêu đề của Kênh</TITLE>
<ABSTRACT>Tổng hợp nội dung của kênh.</ABSTRACT>
<SCHEDULE>
<INTERVALTIME DAY="14"/>
</SCHEDULE>
<LOGO HREF="wideChannelLogo.gif" STYLE="IMAGE-WIDE"/>
<LOGO HREF="imageChannelLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="iconChannelLogo.gif" STYLE="ICON"/>
<ITEM HREF="pageTwo.extension"
    LASTMOD="1998-11-05T22:12"
    PRECACHE="CÓ"
CẤP="1">
<TITLE>Tiêu đề của Trang Hai</TITLE>
<ABSTRACT>Tóm tắt nội dung của Trang Hai.</ABSTRACT>
<LOGO HREF="pageTwoLogo.gif" STYLE="IMAGE"/>
<LOGO HREF="pageTwoLogo.gif" STYLE="ICON"/>
</ITEM>
</CHANNEL>
```

## Người giới thiệu

* [Định dạng định nghĩa kênh - Theo Wikipedia](https://vi.wikipedia.org/wiki/Channel_Definition_Format)

