{
  "date" : "2021-08-17",
  "keywords" :[ "tệp udf", "định dạng tệp udf", "tệp udf là gì", "tệp", "ví dụ udf", "phần mở rộng tệp udf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp UDF và API có thể tạo và mở tệp UDF.",
  "title" :"UDF - Tệp định dạng đĩa chung",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Tệp UDF là gì?
Tệp có phần mở rộng .udf là định dạng hình ảnh đĩa thường được sử dụng để lưu tệp trên phương tiện quang học; có thể được sử dụng để ghi đĩa DVD, CD và các phương tiện quang học khác; lưu trữ một tập hợp các tệp bằng cấu trúc thư mục được chỉ định trong tiêu chuẩn UDF; cho phép xóa và sửa đổi các tệp trên đĩa đích ngay cả sau khi chúng đã được ghi. Hiệp hội Công nghệ Lưu trữ Quang học đặt hệ thống tệp UDF làm tiêu chuẩn để tạo thành một hệ thống tệp chung cho tất cả các phương tiện quang học, chẳng hạn như phương tiện quang học có thể ghi lại và phương tiện chỉ đọc.

## Định dạng tệp UDF
Định dạng tệp UDF là một hệ thống tệp mở trung lập với nhà cung cấp để lưu trữ dữ liệu máy tính cho nhiều loại phương tiện. Nó đã được sử dụng phổ biến cho DVD và các định dạng đĩa quang mới hơn. Thông thường, phần mềm làm chủ một hệ thống tệp UDF trong một quy trình hàng loạt và ghi nó vào phương tiện quang học trong một lần chạy. Tuy nhiên, khi nó ghi các gói vào phương tiện có thể ghi lại, UDF cho phép các tệp được tạo, xóa và thay đổi trên đĩa tương tự như hệ thống tệp có mục đích chung trên phương tiện di động như ổ đĩa flash hoặc đĩa mềm.
### Thông số UDF
Tiêu chuẩn UDF xác định ba biến thể hệ thống tệp sau:

- **Bản dựng thuần túy**: Đây là định dạng ban đầu được hỗ trợ trong tất cả các phiên bản UDF. Nó được giới thiệu trong phiên bản đầu tiên của tiêu chuẩn, định dạng này có thể được sử dụng trên bất kỳ loại đĩa nào cho phép truy cập đọc hoặc ghi ngẫu nhiên, chẳng hạn như DVD+RW, đĩa cứng và phương tiện DVD-RAM.
- **VAT build**: Được sử dụng riêng để ghi vào phương tiện ghi một lần. VAT là một cấu trúc bổ sung trên đĩa cho phép ghi gói tin; nghĩa là ánh xạ lại các khối vật lý khi các tệp hoặc dữ liệu khác trên đĩa bị sửa đổi hoặc bị xóa. Đối với phương tiện ghi một lần, toàn bộ đĩa được ảo hóa, làm cho tính chất ghi một lần trong suốt đối với người dùng; đĩa có thể được xử lý giống như cách người ta xử lý đĩa ghi lại.
- **Bản dựng Spared (RW)**: Được sử dụng riêng để ghi vào phương tiện có thể ghi lại. Nó bổ sung thêm một Sparing Table để quản lý các lỗi cuối cùng sẽ xảy ra trên các phần của đĩa đã được ghi lại nhiều lần. Bảng này lưu dấu vết của các khu vực bị hao mòn và sắp xếp lại chúng cho những khu vực đang hoạt động. Quản lý lỗi của UDF không áp dụng cho các hệ thống đã triển khai một hình thức quản lý lỗi khác, chẳng hạn như Mount Rainier (MRW) cho đĩa quang hoặc bộ điều khiển đĩa cho ổ cứng.
 




## Người giới thiệu


* [Định dạng hình ảnh Windows - theo Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


