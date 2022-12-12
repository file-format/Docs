{
  "date" : "2022-05-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp OBML - Tệp trang web đã lưu của Opera Mini",
  "description" :"Tìm hiểu về tệp OBML là gì và các API có thể tạo và mở tệp OBML.",
  "linktitle" : "OBML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-05-19"
}

## Tệp OBML là gì?

Tệp OBML (Ngôn ngữ đánh dấu nhị phân Opera) là phiên bản ngoại tuyến của trang web được lưu bởi trình duyệt web di động Opera Mini. Đây là phiên bản nhỏ gọn, khép kín của các tệp [HTML](/vi/web/html/) chứa tất cả các thành phần của trang để hiển thị trên các thiết bị cụ thể khi ngoại tuyến. Định dạng tệp OBML đã được nâng cấp lên một số phiên bản với OBML15 và OBML16 đang được sử dụng rộng rãi. Một điểm quan trọng cần lưu ý là mỗi phiên bản Opera Mini chỉ tương thích với một định dạng OBML. Do đó, việc nâng cấp Opera Mini sẽ khiến các trang đã lưu trước đó có thể đọc được. Các tệp OBML có thể được chuyển đổi thành HTML và [PDF](/vi/pdf/).

## Định dạng tệp OBML

Định dạng tệp OBML được lưu ở định dạng tệp độc quyền của Opera và thông số kỹ thuật định dạng tệp của nó không có sẵn công khai. Tuy nhiên, [Định dạng OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md) đã được thiết kế ngược để giải mã cấu trúc của nó như sau.

### Các kiểu dữ liệu OBML

Theo kết quả được thiết kế ngược, OBML sử dụng các kiểu nguyên thủy sau:

* `byte` – số nguyên không dấu (1 byte)
* `short` – số nguyên có dấu (2 byte, big-endian)
* `medium` – số nguyên có dấu (3 byte, big-endian)
 * `blob` – { length: short, data: byte[length] }
* `char` – một byte chứa ký tự ASCII
* `string` – một đốm màu chứa văn bản được mã hóa UTF-8

### Tiêu đề OBML

```
header := {
	(if version >= 15) {
		fake_file_size: medium = 0x02d355
		fake_version: byte     = 16
	}
	file_size: medium
	version: byte
	page_size: coords
	(if version == 16) {
		unknown: byte[3]      // always S\x00\x00
	}
	unknown: short                // always -1
	page_title: string
	unknown: blob
	page_url_base: string
	page_url: url
	(if version >= 15) {
		unknown: byte[6]
	}
	(if 6 < version <= 13) {
		unknown: byte[5]
	}
	(if version == 6) {
		unknown: byte[1]
	}
	metadata: chunk[]
	content: chunk[]
}
```
## Người giới thiệu

* [Định dạng OMBL](https://github.com/grawity/obml-parser/blob/master/obml.md)

