{
  "date" : "2021-28-05",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAR - Tệp Báo cáo Microsoft Access",
  "keywords" :[ "mar", "mar file", "mar file format", "what is access report", "access report", "microsoft access report"],
  "description":"Tìm hiểu về định dạng tệp Báo cáo Acess (MAR) được phần mềm Microsoft Access sử dụng để tạo lối tắt hoặc liên kết đến Báo cáo Microsoft Access.",
  "linktitle" : "MAR",
  "menu" : {
    "docs" : {
    "identifier": "reporting-mar",
      "parent" : "reporting"
}
},
  "lastmod" : "2021-28-05"
}

## Báo cáo truy cập (tệp MAR) là gì? ##
Một tệp do Microsoft Access tạo dưới dạng lối tắt của báo cáo được lưu với phần mở rộng tệp .mar. **Báo cáo Microsoft Access** cung cấp một cách để định dạng, xem và tóm tắt thông tin trong cơ sở dữ liệu Microsoft Access. Các báo cáo này cho phép bạn định dạng dữ liệu của mình theo bố cục chính xác và đầy đủ thông tin để xem trên màn hình hoặc in ấn. Báo cáo chỉ hiển thị dữ liệu tĩnh, nghĩa là chúng tôi không thể thay đổi dữ liệu trong bảng khi xem báo cáo Access. Báo cáo hiển thị dữ liệu gần đây nhất khi được mở.

## Định dạng tệp Báo cáo Microsoft Access (MAR)

Định dạng tệp MAR được phần mềm Microsoft Access sử dụng để tạo lối tắt hoặc liên kết đến Báo cáo Microsoft Access, một đối tượng cơ sở dữ liệu sẽ trở nên hữu ích khi bạn cần trình bày thông tin trong cơ sở dữ liệu của mình cho bất kỳ mục đích sử dụng nào sau đây:

- Hiển thị tóm tắt dữ liệu.
- Lưu trữ ảnh chụp nhanh của dữ liệu.
- Hiển thị thông tin chi tiết về hồ sơ cá nhân.
- Tạo nhãn.

## Các phần của Báo cáo truy cập
Thiết kế của báo cáo Access được chia thành các phần khác nhau có thể được xem trong dạng xem Thiết kế. Bảng sau đây giải thích cách mỗi phần hoạt động và có thể giúp bạn tạo báo cáo.
| Mục | Phần được hiển thị như thế nào khi được in | Phần có thể được sử dụng ở đâu |
---------|----|------|
| Tiêu đề báo cáo | Ở phần đầu của báo cáo. | Sử dụng tiêu đề báo cáo cho thông tin thường có thể xuất hiện trên trang bìa, chẳng hạn như logo, tiêu đề hoặc ngày tháng. Khi bạn đặt một điều khiển được tính toán sử dụng hàm tổng hợp Sum trong tiêu đề báo cáo, tổng được tính cho toàn bộ báo cáo. Tiêu đề báo cáo được in trước tiêu đề trang. |
| Đầu trang | Ở đầu mỗi trang. | Sử dụng tiêu đề trang để lặp lại tiêu đề báo cáo trên mỗi trang. |
| Tiêu đề nhóm | Ở đầu mỗi nhóm bản ghi mới. | Sử dụng tiêu đề nhóm để in tên nhóm. Ví dụ: trong một báo cáo được nhóm theo sản phẩm, hãy sử dụng tiêu đề nhóm để in tên sản phẩm. Khi bạn đặt một điều khiển được tính toán sử dụng hàm tổng hợp Sum trong tiêu đề nhóm, tổng sẽ dành cho nhóm hiện tại. Bạn có thể có nhiều phần tiêu đề nhóm trên một báo cáo, tùy thuộc vào số lượng cấp độ nhóm mà bạn đã thêm. Để biết thêm thông tin về cách tạo đầu trang và chân trang của nhóm, hãy xem phần Thêm nhóm, sắp xếp hoặc tổng. |
| Chi tiết | Xuất hiện một lần cho mỗi hàng trong nguồn bản ghi. | Đây là nơi bạn đặt các điều khiển tạo nên phần chính của báo cáo. |
| Chân trang nhóm | Cuối mỗi nhóm hồ sơ. | Sử dụng chân trang nhóm để in thông tin tóm tắt cho một nhóm. Bạn có thể có nhiều phần chân nhóm trên một báo cáo, tùy thuộc vào số lượng cấp độ nhóm mà bạn đã thêm. |
| Chân trang | Ở cuối mỗi trang. | Sử dụng chân trang để in số trang hoặc thông tin trên mỗi trang. |
| Chân báo cáo | Ở cuối báo cáo. Lưu ý: Trong dạng xem Thiết kế, chân trang báo cáo xuất hiện bên dưới chân trang. Tuy nhiên, trong tất cả các dạng xem khác (ví dụ: dạng xem Bố cục hoặc khi báo cáo được in hoặc xem trước), chân trang báo cáo xuất hiện phía trên chân trang, ngay sau chân trang nhóm cuối cùng hoặc dòng chi tiết trên trang cuối cùng. | Sử dụng chân trang báo cáo để in tổng số báo cáo hoặc thông tin tóm tắt khác cho toàn bộ báo cáo. |






## Người giới thiệu ##

- [Giới thiệu về báo cáo trong Access](https://support.microsoft.com/en-us/office/introduction-to-reports-in-access-e0869f59-7536-4d19-8e05-7158dcd3681c)
- [Thiết kế báo cáo trong Access](https://github.com/prijuly2000/DBMS/blob/master/DesigningReportsinAccess2010.pdf)

