{
"ngày": "2023-06-08",
  "keywords": [
"tệp crx",
"tệp crx là gì",
"cách cài đặt tệp crx trong google chrome",
"cách mở tệp crx",
"tệp crx chứa gì",
"định dạng của tệp crx là gì",
"tài liệu",
"phần mở rộng tập tin crx",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp CRX - Tiện ích mở rộng của Google Chrome",
  "description":"Tìm hiểu về định dạng CRX và các API có thể tạo và mở tệp CRX.",
"linktitle":"CRX",
  "menu": {
    "docs": {
      "identifier": "misc-crx",
      "parent": "misc"
}
},
"lastmod": "2023-06-08"
}

## Một tập tin CRX là gì?

Định dạng tệp CRX được liên kết với tiện ích mở rộng của trình duyệt Google Chrome. Tệp CRX về cơ bản là một gói nén chứa các tệp và siêu dữ liệu cần thiết để tiện ích mở rộng được cài đặt và chạy trong Google Chrome. Nó nâng cao chức năng hoặc giao diện của trình duyệt web bằng cách cung cấp một tính năng hoặc chủ đề bổ sung.

Khi tệp CRX được tải xuống và cài đặt trong Google Chrome, trình duyệt sẽ xác minh tính toàn vẹn của tiện ích mở rộng bằng khóa và chữ ký chung. Nếu xác minh thành công, Chrome sẽ trích xuất nội dung của tệp CRX và cài đặt tiện ích mở rộng, cung cấp tiện ích này để sử dụng. Người dùng có thể quản lý các tiện ích mở rộng của mình thông qua trang Tiện ích mở rộng của Chrome, cho phép bật, tắt hoặc xóa các tiện ích mở rộng đã cài đặt.

## Làm cách nào để cài đặt tệp CRX trong Google Chrome?

Để cài đặt tệp CRX trong Google Chrome, bạn có thể làm theo các bước sau:

1. Mở trình duyệt Chrome.
2. Nhập `chrome://extensions` vào thanh địa chỉ và nhấn Enter.
3. Bật nút chuyển đổi "Chế độ nhà phát triển" nằm ở góc trên bên phải của trang Tiện ích mở rộng.
4. Nhấp vào nút "Tải đã giải nén".
5. Xác định vị trí và chọn thư mục chứa nội dung được trích xuất của tệp CRX (hoặc chỉ cần chọn chính tệp CRX).
6. Nhấp vào "Mở" để cài đặt tiện ích mở rộng.

## Tệp CRX chứa gì?

Tệp CRX chứa các tệp và siêu dữ liệu cần thiết cần thiết cho tiện ích mở rộng của Google Chrome. Dưới đây là bảng phân tích các nội dung điển hình được tìm thấy trong tệp CRX:

- **Tệp kê khai (manifest.json):** Tệp này là tệp có định dạng JSON bao gồm thông tin về tiện ích mở rộng như tên, phiên bản, mô tả, quyền và tập lệnh nền. Nó xác định cấu trúc và hành vi của phần mở rộng.
- **Tệp JavaScript:** Những tệp này chứa mã xác định chức năng của tiện ích mở rộng. Chúng có thể bao gồm các tập lệnh để xử lý sự kiện, sửa đổi trang web hoặc tương tác với API của Chrome.
- **Tệp HTML, CSS và hình ảnh:** Tiện ích mở rộng thường bao gồm các thành phần giao diện người dùng, chẳng hạn như cửa sổ bật lên hoặc trang tùy chọn. Các tệp HTML xác định cấu trúc của các giao diện này, trong khi các tệp CSS kiểm soát giao diện của chúng. Tệp hình ảnh được sử dụng cho các biểu tượng hoặc nội dung đồ họa khác.
- **Tệp tài nguyên tùy chọn:** Tiện ích mở rộng có thể bao gồm các tài nguyên bổ sung, chẳng hạn như tệp bản địa hóa để hỗ trợ nhiều ngôn ngữ. Các tệp này chứa bản dịch văn bản được sử dụng trong giao diện người dùng của tiện ích mở rộng.
- **Tập lệnh nền:** Nếu tiện ích mở rộng có các quy trình nền hoặc tập lệnh chạy độc lập với trang web đang hoạt động thì các tập lệnh này sẽ được đưa vào tệp CRX.
- **Tập lệnh nội dung:** Tập lệnh nội dung là tập lệnh có thể được đưa vào các trang web để sửa đổi hành vi hoặc tương tác với nội dung của chúng. Nếu tiện ích mở rộng sử dụng tập lệnh nội dung thì các tệp cần thiết cho các tập lệnh đó sẽ có trong tệp CRX.
- **Nội dung khác:** Tùy thuộc vào yêu cầu cụ thể của tiện ích mở rộng, các tệp bổ sung như tệp âm thanh hoặc video, phông chữ hoặc tệp dữ liệu có thể được bao gồm.

Định dạng tệp CRX về cơ bản là một gói nén chứa tất cả các tệp và thư mục này theo cách có cấu trúc. Khi tệp CRX được cài đặt trong Google Chrome, trình duyệt sẽ trích xuất nội dung và đặt chúng vào các vị trí thích hợp, cho phép tải và chạy tiện ích mở rộng trong trình duyệt.

## Định dạng của tệp CRX là gì?

Định dạng tệp CRX là định dạng cụ thể để đóng gói và phân phối các tiện ích mở rộng của Google Chrome. Về cơ bản nó là một kho lưu trữ ZIP nén với phần mở rộng tệp khác nhau. Cấu trúc cơ bản của tệp CRX như sau:

- **Chữ ký tệp:** 4 byte đầu tiên của tệp chứa số ma thuật "Cr24" (thập lục phân: 43 72 32 34) dùng làm chữ ký để xác định tệp là tệp CRX.
- **Số phiên bản:** 4 byte tiếp theo biểu thị số phiên bản của định dạng CRX.
- **Độ dài khóa công khai:** 4 byte sau cho biết độ dài khóa chung được mã hóa được sử dụng để xác minh chữ ký tiện ích mở rộng.
- **Độ dài chữ ký:** 4 byte tiếp theo chỉ định độ dài chữ ký của phần mở rộng.
- **Khóa công khai:** Phần này chứa khóa chung được mã hóa dùng để xác minh tính toàn vẹn của tiện ích mở rộng.
- **Chữ ký:** Phần này chứa chữ ký của tiện ích mở rộng, được tạo bằng cách ký vào nội dung của tiện ích mở rộng bằng khóa riêng tương ứng với khóa chung được đề cập ở trên.
- **Kho lưu trữ ZIP:** Các byte còn lại của tệp CRX bao gồm một kho lưu trữ ZIP được nén. Kho lưu trữ này chứa tất cả các tệp và thư mục tiện ích mở rộng cần thiết, bao gồm tệp kê khai, tệp JavaScript, tệp HTML, tệp CSS, hình ảnh và bất kỳ tài nguyên nào khác.

## Người giới thiệu
* [Đặc tả định dạng CRX](https://groups.google.com/a/chromium.org/g/chromium-extensions/c/K3YIsNL_Et4)

