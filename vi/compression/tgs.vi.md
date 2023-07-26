{
  "date" : "2019-10-11",
  "keywords" :[ "tệp tgs", "định dạng tệp tgs", "tệp tgs là gì", "tệp", "ví dụ tgs", "phần mở rộng tệp tgs","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGS - Định dạng tệp nhãn dán hoạt hình Telegram",
  "description":"Tìm hiểu về định dạng tệp TGS và các API có thể tạo và mở tệp TGS.",
  "linktitle" : "TGS",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Tệp TGS là gì?

Tệp có phần mở rộng .tgs là tệp hình dán hoạt hình được giới thiệu bởi dịch vụ nhắn tin đa nền tảng, [Telegram](https://core.telegram.org/stickers#animated-stickers). Hình dán hoạt hình được người dùng ứng dụng nhắn tin sử dụng để gửi nội dung sống động và nâng cao hơn trong tin nhắn không giống như đồ họa tĩnh là hình ảnh tĩnh. Telegram ban đầu sử dụng định dạng tệp [WEBP](/vi/image/webp/) cho nhãn dán ảnh tĩnh. Định dạng tệp TGS có thể lưu trữ dữ liệu hoạt hình ở độ phân giải cao hơn và kích thước tệp nhỏ hơn so với nhãn dán WEBP tĩnh. Các tệp TGS có thể được mở bằng các ứng dụng như Telegram, 7-zip, Tiện ích lưu trữ của Apple và Corel WinZip.

## Định dạng tệp TGS

Telegram đã giới thiệu định dạng tệp TGS vào tháng 7 năm 2019 dựa trên thư viện Lottie. Tệp TGS bao gồm văn bản [JSON](/vi/web/json/) được xuất từ hoạt ảnh trong Adobe After Effects. Văn bản JSON đã xuất được nén bằng cách sử dụng nén gzip giúp giảm kích thước tệp. Thông tin JSON về tệp văn bản được lưu trữ trong tệp văn bản trở thành cơ sở của tốc độ nén cao.

### Hình dán TGS Thông số kỹ thuật

Định dạng tệp TGS áp đặt một số hạn chế nhất định đối với việc tạo nhãn dán hoạt hình TGS. Một tệp hoạt hình TGS:

* Kích thước nhãn dán/canvas phải là 512x512 pixel.
* Các đối tượng nhãn dán không được rời khỏi canvas.
* Độ dài hoạt ảnh không được vượt quá 3 giây.
* Tất cả các hoạt ảnh phải được lặp lại.
* Kích thước nhãn dán không được vượt quá 64 KB sau khi hiển thị trong Bodymovin.
* Tất cả hoạt ảnh phải chạy ở 60 khung hình mỗi giây.

### Văn bản JSON TGS mẫu

Một nhãn dán động mẫu, khi được giải nén, chứa nội dung văn bản JSON sau đây.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Người giới thiệu ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)
* [gzip - Wikipedia](https://vi.wikipedia.org/wiki/Gzip)

