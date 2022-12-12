{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "phần mở rộng", "tệp", "định dạng", "web", "chứng chỉ", "ngôn ngữ" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Định dạng tệp chứng chỉ",
  "description":"Tìm hiểu về định dạng tệp CER và các API có thể tạo và mở tệp CER.",
  "linktitle" : "CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Tệp CER là gì? ##

Tệp có phần mở rộng .cer chịu trách nhiệm lưu trữ một số thông tin về chứng chỉ chủ sở hữu và khóa chung cụ thể. Định dạng tệp này không thể lưu trữ khóa riêng và chỉ có khả năng lưu trữ một chứng chỉ x509. Cơ quan cấp chứng chỉ được bảo mật cụ thể là những cơ quan thuộc về HTTPS, một giao thức đáng tin cậy và bảo mật để duyệt
CER là chứng chỉ của máy chủ của bạn. Nó thường được nhận bởi cơ quan cấp chứng chỉ cho tên miền. CER hầu hết được coi là giống như [CRT](/vi/web/crt/), mặc dù cả hai đều có cùng định dạng chứng chỉ SSL nhưng là các phần mở rộng tên tệp khác nhau.
Chúng có thể được sử dụng trên các hệ điều hành bằng cách chỉ cần mở trình duyệt và kiểm tra tính bảo mật của trình duyệt hoặc trang web đang được sử dụng.

## Lược Sử ##

Năm 1995, Thawte trở thành cơ quan chứng nhận đầu tiên giải quyết vấn đề chứng chỉ SSL (liên kết ổ cắm bảo mật) công khai bên ngoài Hoa Kỳ. Sau đó là hàng loạt cơ quan chức năng như vậy được thành lập từ năm 1995 đến 2020.

## Định dạng tệp CER ##

Những tập tin này có thể đơn giản
* PKC S#7 bao gồm mã hóa Base64 ASCII
* Phần mở rộng tệp của nó là p7b hoặc p7cZ
* Đối với nội dung nhị phân, chứng chỉ sẽ là DER hoặc pkcs12/pfx.
Có nhiều loại tệp chứng chỉ với một số thông số kỹ thuật riêng:
* .pem, Khi một tổ chức usThawteificate xâu chuỗi định dạng này nổi tiếng để tạo chứng chỉ
* .arm, khi cần có phương pháp trích xuất chứng nhận hỗ trợ tự ký, định dạng được chỉ định cho mục đích này là .arm. Nó được thể hiện trong mã hóa ASCII cơ sở 64.
* .der, Nó bao gồm dữ liệu nhị phân. Điều này có nghĩa là nó chỉ có thể được sử dụng cho một chứng chỉ duy nhất
* .pfx (PKC512), Nó bao gồm một khóa riêng tư tương ứng với chứng chỉ do CA cấp hoặc chứng chỉ tự ký. Định dạng này nổi tiếng với việc chuyển đổi triển khai SSL này sang triển khai SSL khác.


