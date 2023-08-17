{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp WMV",
  "description":"Tìm hiểu về định dạng tệp WMV và các API có thể tạo và mở tệp WMV.",
  "linktitle" : "WMV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2019-09-16"
}

## Tệp WMV là gì?

Định dạng Hệ thống Nâng cao (ASF) là một bộ chứa đa phương tiện kỹ thuật số được thiết kế chủ yếu để lưu trữ và truyền các luồng phương tiện. Microsoft Windows Media Video (WMV) là định dạng video nén và Microsoft Windows Media Audio (WMA) là định dạng âm thanh nén cùng với siêu dữ liệu bổ sung trong bộ chứa ASF do Microsoft phát triển. Khi các tệp WMV hoặc WMA được mã hóa bằng codec Windows Media Video và Windows Media Audio thì chúng được thể hiện bằng phần mở rộng .asf. WMV nén các tệp lớn để có tốc độ truyền tốt hơn qua mạng trong khi vẫn duy trì chất lượng của video. WMV được thiết kế đặc biệt để chạy trên tất cả các thiết bị Windows. Sau khi được Hiệp hội Kỹ sư Điện ảnh và Truyền hình (SMPTE) chuẩn hóa, WMV hiện được coi là một định dạng chuẩn mở.

## Lịch sử ##

Với sự trợ giúp của các codec độc quyền của Microsoft, định dạng video nén mới được phát triển vào năm 1999 có tên là WMV7, dựa trên MPEG-4 Phần 2. Các cải tiến đã được thêm vào trong hai phiên bản khác, tức là WMV8 và 9. Microsoft đã gửi phiên bản thứ 9^^th^^ của WMV sang SMPTE để chuẩn hóa vào năm 2003, chuẩn này cuối cùng đã được chuẩn hóa vào năm 2006 với tên gọi SMPTE 421M còn được gọi là VC-1. Ý tưởng đằng sau WMV là phát triển một định dạng phương tiện có thể được hỗ trợ bởi tất cả phần cứng và phần mềm do Microsoft hỗ trợ. Hơn nữa, một mục đích chính khác là truyền các luồng video qua internet trong một kịch bản tối ưu. Sau khi tiêu chuẩn hóa từ SMPTE, WMV cũng trở thành định dạng video cho đĩa Blu-ray.

## Thông số kỹ thuật định dạng tệp

### Thùng đựng hàng

Nói chung, WMV được đóng gói vào bộ chứa ASF nhưng ngoài ra, bộ chứa Matroska hoặc AVI cũng có thể hỗ trợ nó với các phần mở rộng tương ứng là .mkv và .avi.

### Windows Media Video 9

Mặc dù có sẵn nhiều codec âm thanh và video khác nhau trong sê-ri Windows Media Video 9 để tạo và phát lại phương tiện kỹ thuật số, nhưng codec WMV-9 là codec video mới nhất và tốt nhất vì nó có thể đạt được mức nén tối ưu từ tốc độ bit rất thấp, tức là 160 x. 120 ở tốc độ 10 Kb/giây đến 1920 x 1080 ở tốc độ 4-8 Mb/giây cho nhiều loại video HD.

### Cấu trúc của Codec

WMV-9 có định dạng màu bên trong 8 bit 4:2:0. Giống như tất cả các tiêu chuẩn nén video phổ biến khác MPEG-1 và H.261, WMV-9 sử dụng sơ đồ biến đổi không gian và bù chuyển động dựa trên khối. Nói chung, chúng ta có thể nói rằng các tiêu chuẩn này thực hiện bù chuyển động theo từng khối từ khung được tái tạo trước đó với sự trợ giúp của một đại lượng 2 chiều được gọi là vectơ chuyển động (MV) để báo hiệu sự dịch chuyển không gian. Khối hiện tại được hình thành với sự trợ giúp của việc dự đoán các giá trị từ khung được tạo lại trước đó có cùng kích thước được dịch chuyển khỏi vị trí hiện tại bởi vectơ chuyển động. Cuối cùng, lỗi còn lại được tính là sự khác biệt giữa khối dự đoán được bù chuyển động và khối thực tế. Sai số dư này được biến đổi bằng cách sử dụng biến đổi nén năng lượng tuyến tính sau đó được lượng tử hóa và mã hóa entropy.

Các hệ số biến đổi lượng tử hóa được giải mã entropy, khử lượng tử hóa và biến đổi nghịch đảo để tạo ra giá trị gần đúng của sai số dư ở phía bộ giải mã, sai số này sau đó được thêm vào dự đoán bù chuyển động để tạo ra sự tái tạo. Mô tả cấp cao của codec được hiển thị trong hình ảnh sau đây.

Phần còn lại của phần này sẽ thảo luận về những cải tiến mới trong WMV-9 giúp phân biệt nó với phần còn lại của các giải pháp mã hóa video như tiêu chuẩn MPEG. WMV-9 có các khung bên trong (I), dự đoán (P) và dự đoán hai chiều (B). Khung bên trong là những khung được mã hóa độc lập và không phụ thuộc vào các khung khác. Các khung dự đoán là các khung phụ thuộc vào một khung trong quá khứ. Việc giải mã khung dự đoán chỉ có thể xảy ra sau khi tất cả các khung tham chiếu trước khung hiện tại bắt đầu từ khung (I) gần đây nhất đã được giải mã. Khung B là khung có hai tham chiếu—một trong quá khứ tạm thời và một trong tương lai tạm thời. Các khung B được truyền sau các tham chiếu của chúng, điều đó có nghĩa là các khung B được gửi không theo thứ tự để đảm bảo rằng các tham chiếu của chúng có sẵn tại thời điểm giải mã. Khung B trong WMV-9 không được sử dụng làm tham chiếu cho các khung tiếp theo. Điều này đặt các khung B bên ngoài vòng giải mã, cho phép thực hiện các phím tắt trong quá trình giải mã các khung B mà không bị trôi hoặc tạo tác trực quan trong thời gian dài. Định nghĩa trên của các khung I, P và B áp dụng cho cả trình tự lũy tiến và xen kẽ.

Hiệu suất của codec video được so sánh với đồ thị tỷ lệ biến dạng (RD) của chúng. Đó là một đường cong 2-D cho thấy sự biến dạng do quá trình nén tạo ra ở một tốc độ bit nhất định.

WMV-9 đã giải quyết vấn đề này bằng việc giới thiệu nhiều kỹ thuật được liệt kê dưới đây:

1. Chuyển đổi kích thước khối thích ứng

2. Bộ biến đổi chính xác hạn chế

3. Bù chuyển động

4. Lượng tử hóa và khử lượng tử

5. Mã hóa entropy nâng cao

6. Lọc vòng lặp

7. Mã hóa khung B nâng cao

8. Mã hóa xen kẽ

9. Làm mịn chồng chéo

10. Công cụ tỷ lệ thấp

11. Bù mờ dần

## Người giới thiệu ##

* [https://bytescout.com/blog/2018/02/windows-media-video-format.html](https://bytescout.com/blog/2018/02/windows-media-video-format.html)
* [https://vi.wikipedia.org/wiki/Windows_Media_Video](https://en.wikipedia.org/wiki/Windows_Media_Video)


