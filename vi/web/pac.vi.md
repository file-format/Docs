{
  "date" : "2021-05-24",
  "keywords" :["pac", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "Cấu hình tự động proxy"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAC - Tệp cấu hình tự động proxy (PAC)",
  "description":"Tìm hiểu về định dạng tệp PAC là gì và các API có thể tạo và mở tệp PAC.",
  "linktitle" : "PAC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-17"
}

## Tệp PAC là gì?

Tệp có phần mở rộng .pac (Cấu hình tự động proxy) là tệp cấu hình chứa các quy tắc gửi yêu cầu web trực tiếp tới internet hoặc định tuyến các yêu cầu này qua máy chủ proxy. Nó chứa hàm [JavaScript](/vi/web/js/) định tuyến các yêu cầu web thông qua một số máy chủ proxy web thay vì gửi chúng trực tiếp đến đích. Máy chủ proxy giống như một người trung gian chấp nhận các yêu cầu từ nhiều khách hàng và phục vụ những yêu cầu này bằng cách chuyển tiếp đến các đích. Chúng được sử dụng để kiểm soát tải trên lưu lượng truy cập internet. Các tệp PAC có thể được mở bằng bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Microsoft Notepad.

## Thông tin thêm về Định dạng tệp PAC

Các tệp PAC lần đầu tiên được đưa vào Netscape Navigator vào năm 1990. Các tệp PAC được viết ở định dạng văn bản JavaScript đơn giản và con người có thể đọc được. Trình duyệt web có tùy chọn chỉ định thông tin URL máy chủ proxy từ nơi danh sách URL proxy được tìm nạp.

Hàm được xác định bên trong PAC bằng JavaScript như sau:

```JavaScript
function FindProxyForURL(url, host) {
  // ...
}
```

### Tệp PAC Ví dụ

```JavaScript
function FindProxyForURL(url, host) {

// If the hostname matches, send direct.
	if (dnsDomainIs(host, "intranet.domain.com") ||
		shExpMatch(host, "(*.abcdomain.com|abcdomain.com)"))
		return "DIRECT";

// If the protocol or URL matches, send direct.
	if (url.substring(0, 4)=="ftp:" ||
		shExpMatch(url, "http://abcdomain.com/folder/*"))
		return "DIRECT";

// If the requested website is hosted within the internal network, send direct.
	if (isPlainHostName(host) ||
		shExpMatch(host, "*.local") ||
		isInNet(dnsResolve(host), "10.0.0.0", "255.0.0.0") ||
		isInNet(dnsResolve(host), "172.16.0.0",  "255.240.0.0") ||
		isInNet(dnsResolve(host), "192.168.0.0",  "255.255.0.0") ||
		isInNet(dnsResolve(host), "127.0.0.0", "255.255.255.0"))
		return "DIRECT";

// If the IP address of the local machine is within a defined
// subnet, send to a specific proxy.
	if (isInNet(myIpAddress(), "10.10.5.0", "255.255.255.0"))
		return "PROXY 1.2.3.4:8080";

// DEFAULT RULE: All other traffic, use below proxies, in fail-over order.
	return "PROXY 4.5.6.7:8080; PROXY 7.8.9.10:8080";

}
```
## Người giới thiệu

* [Tệp PAC là gì?](http://findproxyforurl.com/pac-file-introduction/)

