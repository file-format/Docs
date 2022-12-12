{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "partial", "extension", "file", "format", "web", "Really Simple Syndication","Userland Software" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Cung cấp thông tin thực sự đơn giản",
  "description":"Tìm hiểu về định dạng tệp RSS và API có thể tạo và mở tệp RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## Tệp RSS là gì? ##

Một tệp có phần mở rộng .rss được gọi là Cung cấp thông tin thực sự đơn giản. RSS là một loại tệp dễ đọc hoặc dễ đọc bởi máy tính, tệp XML. Các tệp XML này được cập nhật tự động với bất kỳ thay đổi nào về dữ liệu hoặc cập nhật của trang web hoặc trang web. Thông tin cập nhật cùng với siêu dữ liệu (tên tác giả, tên nhà xuất bản, ngày xuất bản, v.v.) và nội dung web khác của trang web được trích xuất bởi các tệp RSS của người dùng và được trình bày ở định dạng dễ đọc. Tính năng tốt nhất của các tệp RSS này là nó hoạt động trong thời gian thực và các cập nhật, tin tức, xuất bản, tức là mới nhất, được hiển thị trên đầu tệp. Sử dụng tệp RSS, bạn có thể dễ dàng tạo một tệp chứa các bản cập nhật mới nhất của bất kỳ chủ đề nào mà bạn quan tâm, bằng cách lấy nội dung liên quan từ trang web và đọc nó bằng tệp RSS.

## Lược Sử ##

Về bản chất, tệp RSS được tạo ra lần đầu tiên bởi Netscape, họ đã phát minh ra phiên bản đầu tiên của tệp RSS nhưng sau đó đã bỏ ý tưởng đó và không tiếp tục với các phiên bản mới hơn. Sau đó, **Phần mềm Userland** đã hoạt động trên định dạng tệp RSS và tiếp tục đổi mới nó bằng một phiên bản mới hơn, đây là cách RSS v2 xuất hiện trên thị trường. Tuy nhiên, việc phát minh ra RSS có thể được liên kết trở lại Khung mô tả tài nguyên, bởi Ramanathan V vào năm 1997. Hoạt động của hai tệp khá giống nhau và có thể giả định rằng khái niệm RSS được hình thành dựa trên hoạt động của RDF, một trình đọc tệp được sử dụng để thu thập siêu dữ liệu.

## Đặc điểm kỹ thuật ##

Tệp RSS là một loại tệp XML và tất cả các tệp RSS phải tuân theo các tiêu chuẩn của XML 1.0. Có nhiều phiên bản khác nhau của các tệp RSS khác nhau, chẳng hạn như 0,91, 0,92, 2.0, trong số các phiên bản khác. Tệp của mỗi phiên bản tuân theo các thông số kỹ thuật và tiêu chuẩn của phiên bản cụ thể đó.

## RSS Ví dụ ##

Sau đây là một ví dụ đơn giản của RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## Tài liệu tham khảo ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
