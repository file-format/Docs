{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "Thiết bị sách điện tử Rocket của Nuvo Media", "file", "extension", "format", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp RB cho thiết bị Sách điện tử Rocket của Nuvo Media và các API có thể tạo và mở tệp RB.",
  "title" :"RB - Tệp sách điện tử tên lửa",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## Tệp RB là gì?

Tệp có phần mở rộng .rb chứa nội dung Sách điện tử Rocket. Sách điện tử Rocket thực sự là một thiết bị do Nuvo Media sản xuất; họ đã phát hành thiết bị này vào năm 1998. Mặc dù Rocket eBook có khả năng hiển thị hình ảnh nhưng chỉ ở dạng hiển thị đen trắng. Nó có màn hình 106 dpi hoặc 480 x 320 pixel trên màn hình cảm ứng 4,5 x 3 inch. Sách điện tử Rocket kết nối với máy tính thông qua kết nối cổng nối tiếp để tải xuống sách điện tử ở định dạng tệp RB. Các tệp RB có khả năng sử dụng DRM nhưng công nghệ này không được sử dụng trong Sách điện tử hiện đại. Tệp RB thông thường chứa tệp HTML chứa hình ảnh và tệp giả OPF chứa tất cả siêu dữ liệu (.info).

## Thông số Kỹ thuật của Định dạng Tệp RB ##

Một số ma thuật (ở dạng hex) xuất hiện trong 4 byte đầu tiên của tệp: B0 0C B0 0C.

Có vẻ như hai byte tiếp theo là số phiên bản, chẳng hạn như "02 00", viết tắt của phiên bản chính 2 và phiên bản phụ 0.

Bốn byte tiếp theo chứa văn bản "NUVO", tiếp theo là 4 byte 00h.

4 byte tiếp theo là ngày tạo sách, được mã hóa dưới dạng int16. Điều này đặt chúng ta ở offset 0Eh. Phiên bản cũ của ORocketLibrary đã mã hóa giá trị đầy đủ của năm (nghĩa là năm 1999 là "CF 07", năm 2000 là "D0 07"). Trong phiên bản gần đây, tm_year được lưu trữ nguyên văn, tức là 100 cho năm 2000 ("64 00"). Sau năm đến, int8 đại diện cho số 1 tháng tương đối và int8 đại diện cho ngày trong tháng.

6 byte tiếp theo là 00h. Đối với cài đặt thời gian, chúng có thể được đặt trước.

Phần bù tuyệt đối của "Mục lục" được chứa trong một int32 ở phần bù 18h.

Sau đây là int32 chứa độ dài của tệp .rb. Điều này được sử dụng để xác định xem các tập tin đã hoàn thành hay chưa.

Toàn bộ đoạn byte này (20h đến 128h) dường như chỉ cần thiết cho một tiêu đề được mã hóa. Trong các tiêu đề không được mã hóa, chúng luôn bằng không.

Trong hầu hết các trường hợp, mục lục theo sau (ở độ lệch 128). Nó bắt đầu với số lượng int32 số lượng mục nhập "trang" (phần tệp .rb) trong ToC. Mỗi mục bao gồm một tên (không đệm đến 32 byte), theo sau là 3 int32: độ dài của đoạn dữ liệu, vị trí trong tệp .rb và một cờ cho mục này. Tính đến hôm nay, các giá trị đã biết là: 1 (được mã hóa), 2 (trang thông tin) và 8 (xì hơi). Tất cả các tên đều được điều chỉnh, nếu cần, để đảm bảo tất cả chúng đều là duy nhất.

## Người giới thiệu

* [E-Reader - By MobileRead](https://vi.wikipedia.org/wiki/E-reader)

