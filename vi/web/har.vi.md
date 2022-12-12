{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Tệp", "Phần mở rộng", "Định dạng tệp", "Phần mở rộng tệp", "JSON", "Tệp lưu trữ"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - Định dạng tệp lưu trữ HTTP",
  "description" :"Hướng dẫn định dạng tệp của bạn để tìm hiểu tệp HAR là gì và các API có thể tạo và mở tệp HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## Tệp HAR là gì?

Tệp có đuôi .har ([HTTP](/vi/web/http/) Archive) là tệp lưu trữ HTTP lưu trữ dữ liệu phiên truyền qua nhiều trình duyệt (chẳng hạn như Chrome, Safari, IE, Firefox, v.v.) trong [JSON] (/vi/web/json/) định dạng tệp. Dữ liệu được truyền qua internet giữa máy chủ và máy khách (trong trường hợp này là trình duyệt của người dùng) chứa các tiêu đề phản hồi và yêu cầu HTTP được lưu trữ trong tệp HAR. Nó còn chứa thông tin chi tiết về dữ liệu hiệu suất của các trang web được tải trong trình duyệt. Các tệp HAR có thể được mở trong bất kỳ trình soạn thảo văn bản nào, chẳng hạn như Notepad trên Microsoft Windows OS và TextEdit trên Apple MacOS.

## Định dạng tệp HAR - Thông tin khác

Các tệp HAR lưu trữ thông tin phiên trong tệp văn bản thuần bằng định dạng JSON phổ biến. Thông số kỹ thuật cho định dạng tệp HAR do Nhóm Hiệu suất Web của Hiệp hội Web Thế giới (W3C) tạo ra nhưng không thể xuất bản. Tuy nhiên, nó đã xác định thành công định dạng lưu trữ cho các giao dịch HTTP.

Ngoài việc giám sát việc chuyển thông tin yêu cầu và phản hồi, các tệp HAR được các nhà phát triển sử dụng để ghi lại hiệu suất của trình duyệt web về tốc độ tải trang, thời lượng tải nội dung, nội dung được tải, các truy vấn được thực hiện để nhận phản hồi từ trình duyệt và nhiều thông tin khác .

## Tại sao nên sử dụng tệp HAR?

Các tệp HAR có thể hữu ích trong việc cải thiện hiệu suất của trang web bằng cách đánh giá thời gian tải lâu, thời gian hiển thị trang và thời gian phản hồi. Các tệp HAR có thể được phân tích để tìm ra bất kỳ vấn đề nào như vậy và giải quyết mọi vấn đề với trang web để cải thiện hiệu suất.

## Làm cách nào để tạo tệp HAR?

Vậy, làm cách nào để tạo tệp HAR? Chà, điều này phụ thuộc vào loại trình duyệt bạn đang sử dụng để tạo tệp HAR. Trong hướng dẫn này, chúng tôi liệt kê các bước dành cho trình duyệt Google Chrome. Các phương pháp tạo tệp HAR bằng Safari, Firefox, v.v. có thể dễ dàng tìm kiếm trên internet và làm theo.

### Các bước để tạo tệp HAR bằng Google Chrome

Các bước sau đây có thể được thực hiện trên một trang web đang gặp sự cố.

1. Mở trang web trong Google chrome nơi xảy ra sự cố.
1. Mở công cụ dành cho nhà phát triển (kiểm tra phần tử).
1. Chuyển sang bên trái của bảng điều khiển để bắt đầu ghi tập tin. Trong phần này có một nút tròn nhỏ màu đỏ.
1. Nhấp vào biểu tượng “Xóa” để xóa bất kỳ bản ghi nhật ký nào được lưu trong trình duyệt.
1. Để lưu lại nội dung bạn muốn như hình trên, click chuột phải và click “Save as HAR File”

## Người giới thiệu

* [Định dạng tệp HAR - Wikipedia](https://vi.wikipedia.org/wiki/HAR_(file_format))

