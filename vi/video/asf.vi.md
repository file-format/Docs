{
  "date" : "2021-02-15",
  "keywords" :[ "tệp asf", "định dạng tệp asf", "tệp asf là gì", "tệp", "ví dụ asf", "phần mở rộng tệp asf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Định dạng tệp hệ thống nâng cao",
  "description":"Tìm hiểu về định dạng tệp ASF và các API có thể tạo và mở tệp ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Tệp ASF là gì?

Tệp có phần mở rộng .asf là định dạng tệp đa phương tiện để lưu trữ và phát các luồng phương tiện kỹ thuật số qua mạng. Đây là định dạng tệp chứa có thể có cả nội dung video và âm thanh để phát trực tuyến. Bạn sẽ hiếm khi tìm thấy các tệp ASF và nhiều khả năng bạn sẽ bắt gặp các tệp Windows Media Audio ([WMA](/vi/audio/wma/)) và Windows Media Video ([WMV](/vi/video/wmv/)) cả hai đều chỉ định các tệp ASF có nội dung được mã hóa bằng codec tương ứng. Các tệp phương tiện Windows có thể được tạo và đọc bằng Windows Media Format SDK.

## Định dạng tệp ASF

Tệp ASF có thể bao gồm nhiều luồng độc lập hoặc phụ thuộc. Điều này có thể bao gồm nhiều luồng âm thanh cho âm thanh đa kênh hoặc nhiều luồng video có tốc độ bit. Nhiều tốc độ bit làm cho các luồng phù hợp để truyền qua các băng thông khác nhau. Ngoài ra, các luồng trong tệp ASF có thể ở định dạng nén hoặc không nén. Khả năng nén tốt nhất đạt được với codec Microsoft Windows Media Audio và Video 9 Series. Thông số kỹ thuật đầy đủ của định dạng tệp ASF hiện có trên [Trang web của Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Cấu trúc tệp cấp cao nhất của ASF

Các tệp ASF về mặt logic chứa ba loại đối tượng cấp cao nhất:

* `Đối tượng tiêu đề` - bắt buộc và phải được đặt ở đầu mỗi tệp ASF
* `Đối tượng dữ liệu` - bắt buộc và phải tuân theo đối tượng tiêu đề
* `(Các) đối tượng chỉ mục` - tùy chọn, nhưng hữu ích trong việc cung cấp quyền truy cập ngẫu nhiên dựa trên thời gian vào các tệp ASF

Hình ảnh sau đây hiển thị cấu trúc tệp cấp cao nhất của tệp ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Đối tượng tiêu đề cấp cao nhất của ASF

Đối tượng Tiêu đề cung cấp một chuỗi byte nổi tiếng ở đầu tệp ASF và có thể tùy chọn chứa siêu dữ liệu, chẳng hạn như thông tin thư mục. Nó chứa tất cả các thông tin cần thiết để diễn giải thông tin trong đối tượng dữ liệu một cách chính xác. Đối tượng Tiêu đề có thể bao gồm một số đối tượng tiêu chuẩn bao gồm, nhưng không giới hạn ở:

* File Properties Object - Chứa các thuộc tính tập tin toàn cục.
* Stream Properties Object - Xác định một luồng phương tiện kỹ thuật số và các đặc điểm của nó.
* Đối tượng mở rộng tiêu đề - Cho phép thêm chức năng bổ sung vào tệp ASF trong khi vẫn duy trì khả năng tương thích ngược.
* Nội dung Mô tả Đối tượng - Chứa thông tin thư mục.
* Script Command Object - Chứa các lệnh có thể được thực hiện trên dòng thời gian phát lại.
* Marker Object - Cung cấp các điểm nhảy được đặt tên trong một tệp.

Đối tượng Header được biểu diễn bằng cấu trúc sau:

|Tên trường |Loại trường |Kích thước (bit)|
---|---|---|
|ID đối tượng| HƯỚNG DẪN| 128|
|Kích thước Đối tượng| QWORD| 64|
|Số đối tượng tiêu đề| DWORD| 32|
|Dành riêng1| BYTE| 8|
|Dành riêng2| BYTE| 8|

#### Đối tượng dữ liệu cấp cao nhất của ASF

Tất cả dữ liệu phương tiện kỹ thuật số cho tệp ASF được chứa trong đối tượng dữ liệu và được lưu trữ dưới dạng gói dữ liệu ASF. Mỗi gói dữ liệu có độ dài cố định và chứa dữ liệu cho một hoặc nhiều luồng phương tiện kỹ thuật số.

#### Đối tượng chỉ mục cấp cao nhất của ASF

Các đối tượng chỉ mục cấp cao nhất của ASF có hai loại sau:

* `Đối tượng Chỉ mục Đơn giản` - Chứa chỉ mục dựa trên thời gian của dữ liệu video trong tệp ASF. Khoảng thời gian giữa các mục nhập chỉ mục là hằng số và được lưu trữ trong Đối tượng Chỉ mục Đơn giản.
* `Đối tượng chỉ mục` - Đề cập đến Đối tượng chỉ mục, Đối tượng chỉ mục đối tượng phương tiện và Đối tượng chỉ mục mã thời gian, có định dạng tương tự nhau. Giống như Đối tượng chỉ mục đơn giản, Đối tượng chỉ mục lập chỉ mục theo thời gian với khoảng thời gian cố định nhưng không giới hạn đối với các luồng video.

## Người giới thiệu

* [Định dạng tệp ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [Định dạng tệp QuickTime - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

