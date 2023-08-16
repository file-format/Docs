{
  "date" : "2019-10-11",
  "keywords" :[ "tệp apng", "định dạng tệp apng", "tệp apng là gì", "tệp", "ví dụ apng", "phần mở rộng tệp apng","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp APNG - Tệp đồ họa mạng di động hoạt hình",
  "description":"Tìm hiểu về định dạng tệp APNG và các API có thể tạo và mở tệp APNG.",
  "linktitle" : "APNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp APNG là gì?

Tệp có phần mở rộng .apng (Đồ họa mạng di động hoạt hình) là định dạng đồ họa raster và là phần mở rộng không chính thức của Đồ họa mạng di động ([PNG](/vi/image/png/) ). Nó bao gồm nhiều khung hình (mỗi hình ảnh PNG) đại diện cho một chuỗi hoạt hình. Điều này mang lại hình ảnh trực quan tương tự dưới dạng tệp [GIF](/vi/image/gif/). Các tệp APNG hỗ trợ hình ảnh 24 bit và độ trong suốt 8 bit. APNG tương thích ngược với các tệp GIF không hoạt hình. Các tệp APNG sử dụng cùng một phần mở rộng .png và có thể được mở bằng các ứng dụng như Mozilla Firefox, Chrome có hỗ trợ APNG, ứng dụng iMessage cho iOS 10.

## Tóm tắt lịch sử

* Thông số kỹ thuật APNG đã được tạo vào năm 2004 để cung cấp hỗ trợ cho Hình ảnh PNG động
* Bộ giải mã APNG được phát triển với kích thước nhỏ hơn nhiều và sử dụng mặt sau của bộ giải mã PNG
* Sau khi cân nhắc liên tục, một hình ảnh/apng loại MIME mới đã được tạo trong khi vẫn giữ nguyên phần mở rộng là .png thay vì .apng
* APNG đã chính thức bị nhóm PNG từ chối vào ngày 20 tháng 4 năm 2007 do tính đồng nhất của nó với hình ảnh PNG đồng thời có các thông số kỹ thuật khác nhau

## Định dạng tệp APNG

Các tệp APNG được lưu trữ dưới dạng tệp nhị phân trên đĩa và sử dụng các thông số kỹ thuật mở rộng của PNG cho hình ảnh động. Khung đầu tiên của tệp APNG là luồng PNG bình thường mà bộ giải mã PNG có thể đọc được để hiển thị. Định dạng tệp APNG tuân theo các thông số kỹ thuật của PNG và dữ liệu được lưu trữ trong các phân đoạn được gọi là khối. Tuy nhiên, APNG đã giới thiệu các đoạn mới sau:

`Khối điều khiển hoạt hình (acTL)` - Cho biết rằng tệp này là tệp PNG động chứ không phải tệp PNG thông thường. Nó hoạt động như một điểm đánh dấu và xuất hiện trước đoạn mã IDAT. Nó cũng chứa số lượng khung hình và thông tin về thời gian để lặp lại hoạt ảnh

`Phân đoạn điều khiển khung` - Xảy ra ở đầu mỗi và thông tin siêu dữ liệu như kích thước, vị trí, ứng dụng trong suốt và thông tin thay thế theo khung trước đó hoặc khung tiếp theo khi nó kết thúc.

`Khối dữ liệu khung` - Lưu trữ nội dung của khung và bắt đầu bằng một số thứ tự. Số thứ tự này có cấu trúc giống như đoạn IDAT của hình ảnh mặc định.

{{< figure src="../APNG.png" alt="Định dạng tệp PNG - APNG hoạt hình" >}}

APNG tương thích ngược với PNG vì các thông số kỹ thuật của bên được thiết kế theo cách mà ứng dụng đọc tệp PNG được cho là đơn giản bỏ qua các đoạn mà nó không hiểu. Các thông số kỹ thuật liên quan đến độ sâu bit, loại màu, độ nén, bộ lọc, phương pháp xen kẽ và thông tin bảng màu được sử dụng giống như thông số kỹ thuật của định dạng PNG mặc định.

## APNG so với GIF

Với GIF đã có sẵn và được sử dụng trong một thời gian dài, bạn có thể tự hỏi APNG khác với GIF như thế nào. Sau đây là tập hợp so sánh giữa APNG và GIF cung cấp ý tưởng ngắn gọn về cả hai định dạng tệp.

||APNG|GIF|
---|---|---|
|Đã xuất bản|2004|1987|
|Độ sâu màu|24 bit|8 bit|
|Tốc độ khung hình|Không giới hạn|10 khung hình mỗi giây|
|Tính minh bạch|Toàn bộ và một phần|Hoàn thành|
|Nén|Rất tốt|Tốt|

## Người giới thiệu

* [Định dạng tệp APNG](https://en.wikipedia.org/wiki/APNG)
* [Thông số định dạng PNG chính thức](https://www.w3.org/TR/PNG/)

