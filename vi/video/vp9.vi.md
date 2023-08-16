{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Tệp", "Phần mở rộng", "Định dạng tệp", "Định dạng video", "Video TrueMotion", "VPX", "Công nghệ On2"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - Tệp Video TrueMotion",
  "description":"Tìm hiểu về định dạng tệp VP9 và các API có thể tạo và mở tệp VP9.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Tệp VP9 là gì?

Google đã phát triển codec VP9 dưới dạng tiêu chuẩn mã hóa video mã nguồn mở, miễn phí bản quyền với tư cách là người kế thừa VP8. Ban đầu, nó được thiết kế để nén nội dung siêu HD trên YouTube vì nó mở rộng và nâng cao hiệu quả mã hóa của phiên bản tiền nhiệm. Nếu chúng ta nói về codec VPX ban đầu, thì chúng đến từ On2 Technologies, được Google đồng hóa vào năm 2010. Sau đó, Google đã cung cấp mã nguồn mở cho codec. Cả hai định dạng VP8 và VP9 đều có sẵn theo giấy phép BSD miễn phí cho phép các nhà khai thác tổ chức mã hóa hoặc giải mã thành thạo cả phần mềm độc quyền và phần mềm nguồn mở mà không tiết lộ mã nguồn của họ.

## Tính năng kỹ thuật của VP9

* VP9 cung cấp độ phân giải tối đa 8192x4352 với tốc độ lên tới 120 khung hình/giây và nhiều không gian màu, với Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 và sRGB
* Toàn bộ các trường hợp sử dụng web và thiết bị di động từ nén tốc độ bit thấp đến siêu HD chất lượng cao, với hỗ trợ bổ sung cho mã hóa 10/12-bit và HDR đều được định dạng này hỗ trợ đầy đủ
* Nó có thể giảm tốc độ bit của video tới 50% so với các loại khác
* Nó được chuẩn bị để phát trực tuyến thích ứng và được sử dụng bởi YouTube và các nhà cung cấp video trên web nổi tiếng khác
* Các thiết bị Chrome, Opera, Edge, Firefox và Android cũng như hàng triệu TV thông minh hỗ trợ giải mã codec này
* Độ phân giải video lớn hơn 1080p được sửa đổi thông qua VP9 và cho phép nén không mất dữ liệu
* Không gian màu khác nhau như Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 và sRGB được VP9 hỗ trợ
* Video HDR sử dụng Hybrid Log-Gamma và Perceptual Quantizer cũng có thể được hỗ trợ bởi VP9


## Tóm tắt lịch sử

* Quá trình phát triển codec video VP9 đã bắt đầu vào năm 2011 và bộ giải mã của nó đã được thêm vào trình duyệt web Chromium vào tháng 12 năm 2012
* Phiên bản trình duyệt web Google Chrome đầu tiên của nó được phát hành vào tháng 2 năm 2013 và phát hành giải mã vào thời điểm đó
* Google đã phát hành Chrome 29.0.1547 với sự hỗ trợ cuối cùng của VP9 vào tháng 8 năm 2013
* Vào tháng 10 năm 2013, bộ giải mã VP9 bản năng đã được thêm vào FFmpeg
* Mozilla đã thêm nguồn VP9 vào Firefox vào tháng 12 năm 2013 trong phiên bản 2 sau đó được phát hành vào ngày 18 tháng 3 năm 2014
 

## Hoạt động của VP9

Thông thường, video 4K nâng cao chất lượng hình ảnh bằng cách làm cho các pixel cụ thể nhỏ hơn, codec VP9 và HEVC làm cho chúng lớn hơn để thu nhỏ tốc độ bit và kích thước tệp. Mặc dù điều này có vẻ mâu thuẫn, nhưng công cụ mã hóa lấy các pixel lớn hơn và thay đổi chúng thành năng suất có độ phân giải cao hơn. Video nguồn, bao gồm các khung hình video, được mã hóa hoặc nén để tạo ra một luồng bit video nén. Mỗi khung riêng biệt đầu tiên được chia thành các khối pixel. Sau đó, các khối được xem xét kỹ lưỡng để loại bỏ ba chiều và các kết nối tuần tự giữa các khung được đánh giá để tận dụng các khu vực không thể thay đổi. Chúng được mã hóa thông qua các vectơ chuyển động để đảm bảo chất lượng của khối đã cho trên khung hình tiếp theo. Thông tin còn lại được mã hóa bằng cách sử dụng nén nhị phân hiệu quả.

## Người giới thiệu

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9#:~:text=VP9%20is%20an%20open%20and,on%20Google's%20video%20platform%20YouTube)
* [Tài liệu web MDN](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Dừa](https://www.coconut.co/)

