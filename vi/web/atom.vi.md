{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp ATOM - Định dạng cung cấp nguyên tử",
  "description" :"Tìm hiểu về tệp ATOM là gì và các API có thể tạo và mở tệp ATOM.",
  "linktitle" : "ATOM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## Tệp ATOM là gì?

Tệp ATOM là định dạng Cung cấp cho cấu trúc của tài liệu nhập và nguồn cấp dữ liệu Atom. Tương tự như tệp .RSS, định dạng tệp ATOM là định dạng cung cấp thông tin dựa trên XML, là tiêu chuẩn để xuất bản nội dung. Tệp ATOM được sử dụng cho các nguồn cấp dữ liệu web cho phép các chương trình phần mềm kiểm tra các bản cập nhật được xuất bản trên trang web. Nó chứa các mục có thể thuộc nhiều loại khác nhau như tiêu đề, bài báo toàn văn, đoạn trích hoặc liên kết đến nội dung trên trang web

Các ứng dụng có thể **mở tệp ATOM** bao gồm **Apple Safari**.

## Định dạng tệp ATOM - Thông tin khác

Các tệp ATOM được lưu trữ và xuất bản ở định dạng tệp XML phổ biến, đây là định dạng phổ biến để trao đổi thông tin. Nó được phát triển như một giải pháp thay thế cho RSS để xem xét các hạn chế và sai sót của định dạng tệp RSS.

### Các loại Tài liệu Atom

1. `Tài liệu mục nhập Atom` - Đây là một tài liệu XML bao gồm một mục thông tin duy nhất, được gọi là mục nhập, cho nguồn cấp dữ liệu Atom. Nó có một atom:entry phần tử chứa một số phần tử con. Nội dung của mục nhập Atom có thể là văn bản thuần túy, HTML, XHTML hoặc loại phương tiện IANA (Cơ quan cấp số được gán Internet) khác.
1. `Tài liệu nguồn cấp dữ liệu Atom` - Đây là tài liệu XML cung cấp siêu dữ liệu về nguồn cấp dữ liệu Atom và một hoặc nhiều mục nhập cho nguồn cấp dữ liệu. Khi khách hàng yêu cầu thông tin từ nguồn cấp dữ liệu, tài liệu nguồn cấp dữ liệu được tạo bởi máy chủ bao gồm một số mục nhập Atom để đáp ứng yêu cầu.
1. `Bộ sưu tập Atom` - Đây là một loại tài liệu nguồn cấp dữ liệu Atom đặc biệt có chứa URL của các mục nhập Atom có sẵn để chỉnh sửa.

## Người giới thiệu

* [Định dạng Atom Syndication - RFC](https://www.rfc-editor.org/rfc/rfc4287.html)
* [Tổng quan về Atom Feeds - IBM](https://www.ibm.com/docs/en/cics-ts/5.4?topic=support-overview-atom-feeds)
* [Atom - Tiêu chuẩn Web](https://en.wikipedia.org/wiki/Atom_(web_standard))

