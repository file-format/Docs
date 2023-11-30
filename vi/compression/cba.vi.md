{
"ngày": "24-05-2023",
  "keywords": [
"tệp cba",
"tệp cba là gì",
"cách tạo tệp CBA",
"tệp CBA chứa gì",
"định dạng của tệp cba là gì",
"tài liệu",
"phần mở rộng tập tin cba",
"sự mở rộng"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Định dạng tệp CBA - Lưu trữ truyện tranh",
  "description":"Tìm hiểu về định dạng CBA và các API có thể tạo và mở tệp CBA.",
"linktitle":"CBA",
  "menu": {
    "docs": {
      "identifier": "compression-cba",
      "parent": "compression"
}
},
"lastmod": "24-05-2023"
}

## Một tập tin CBA là gì?

Tệp Lưu trữ Truyện tranh (CBA), còn được gọi là tệp Lưu trữ Truyện tranh hoặc Trình đọc Truyện tranh, là định dạng phổ biến được sử dụng để lưu trữ và phân phối truyện tranh kỹ thuật số. Nó thường chứa tập hợp các trang truyện tranh riêng lẻ hoặc hình ảnh được nhóm lại với nhau trong một tệp duy nhất để dễ dàng sắp xếp và đọc.

Một trong những định dạng phổ biến để tạo tệp Lưu trữ Truyện tranh là định dạng TAR (Lưu trữ băng). TAR là định dạng lưu trữ tệp được sử dụng trong môi trường Unix và Linux. Nó kết hợp nhiều tệp thành một tệp duy nhất thường được sử dụng cho mục đích sao lưu.

## Làm cách nào để tạo tệp CBA?

Để tạo tệp Lưu trữ Truyện tranh bằng công cụ lưu trữ TAR, bạn thường làm theo các bước sau:

1. Tập hợp tất cả các trang hoặc hình ảnh truyện tranh mà bạn muốn đưa vào kho lưu trữ.
2. Mở dấu nhắc lệnh hoặc cửa sổ terminal.
3. Điều hướng đến thư mục chứa các trang/hình ảnh truyện tranh.
4. Sử dụng lệnh TAR với các tùy chọn thích hợp để tạo kho lưu trữ. Ví dụ: lệnh có thể trông như thế này:

```
tar -cf comicbook.cbt page1.jpg page2.jpg page3.jpg
```

Trong ví dụ này, tùy chọn -c yêu cầu TAR tạo kho lưu trữ mới và tùy chọn -f chỉ định tên tệp đầu ra (comicbook.cbt trong trường hợp này). Sau khi chỉ định các tùy chọn, bạn cung cấp tên của các tệp bạn muốn đưa vào kho lưu trữ (page1.jpg, page2.jpg, page3.jpg).

5. Sau khi thực hiện lệnh, công cụ TAR sẽ tạo tệp Lưu trữ Truyện tranh (comicbook.cbt trong ví dụ này) trong thư mục hiện tại.

Sau khi có tệp Lưu trữ Truyện tranh, bạn có thể sử dụng nhiều phần mềm hoặc ứng dụng đọc truyện tranh khác nhau để mở và đọc truyện tranh trên máy tính hoặc thiết bị của mình. Các ứng dụng này thường cung cấp các tính năng như điều hướng trang, thu phóng và đánh dấu trang để nâng cao trải nghiệm đọc.

## Tệp CBA chứa gì?

Tệp Lưu trữ Truyện tranh (CBA) được tạo bằng công cụ lưu trữ TAR chứa một tập hợp các trang hoặc hình ảnh truyện tranh riêng lẻ được nhóm lại với nhau thành một tệp duy nhất. Nội dung cụ thể của kho lưu trữ phụ thuộc vào cuốn truyện tranh được đóng gói.

Thông thường, tệp Lưu trữ Truyện tranh bao gồm các nội dung sau:

- **Các trang truyện tranh:** Nội dung chính của kho lưu trữ là chính các trang truyện tranh. Các trang này thường được lưu dưới dạng tệp hình ảnh riêng lẻ, chẳng hạn như JPEG hoặc PNG, đại diện cho từng trang của truyện tranh. Các trang được sắp xếp theo một thứ tự cụ thể để duy trì dòng tường thuật của truyện tranh.
- **Siêu dữ liệu:** Một số định dạng Lưu trữ Truyện tranh có thể bao gồm siêu dữ liệu về truyện tranh, chẳng hạn như tiêu đề, tác giả, nhà xuất bản, ngày xuất bản và mô tả. Thông tin này giúp xác định và phân loại truyện tranh.
- **Các tệp bổ sung:** Ngoài các trang truyện tranh và siêu dữ liệu, kho lưu trữ có thể chứa các tệp bổ sung khác liên quan đến truyện tranh. Các tệp này có thể bao gồm ảnh bìa, hình ảnh quảng cáo, nội dung bổ sung hoặc tệp văn bản cung cấp thông tin hoặc bình luận bổ sung.

## Định dạng của tệp CBA là gì?

Định dạng tệp Lưu trữ Truyện tranh (CBA) được tạo bằng công cụ lưu trữ TAR thường ở định dạng TAR. TAR, viết tắt của Tape Archive, là định dạng lưu trữ tệp thường được sử dụng trong hệ thống Unix và Linux. Nó không dành riêng cho truyện tranh mà là một định dạng lưu trữ có mục đích chung.

Định dạng TAR là cách đơn giản để gộp nhiều tệp vào một tệp lưu trữ duy nhất. Nó không tự cung cấp tính năng nén nên tệp TAR thu được có thể có kích thước lớn so với các định dạng nén khác như ZIP hoặc RAR. Tuy nhiên, tệp TAR có thể được nén bằng các công cụ bổ sung hoặc kết hợp với các thuật toán nén như gzip hoặc bzip2 để giảm kích thước tệp.

Định dạng TAR giữ nguyên cấu trúc tệp, quyền truy cập tệp và dấu thời gian của các tệp được bao gồm. Nó lưu trữ các tệp một cách tuần tự trong kho lưu trữ, cho phép dễ dàng trích xuất từng tệp riêng lẻ hoặc toàn bộ kho lưu trữ.

## Người giới thiệu
* [Kho lưu trữ truyện tranh](https://en.wikipedia.org/wiki/Comic_book_archive)

