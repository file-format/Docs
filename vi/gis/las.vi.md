{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - Định dạng tệp Lidar LASer",
  "description":"Tìm hiểu về định dạng tệp LAS và các API có thể tạo và mở tệp LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Tập tin LAS là gì?

Định dạng tệp LAS (Lidar LASer) là định dạng tệp nhị phân được thiết kế đặc biệt để lưu trữ dữ liệu đám mây điểm lidar. Nó được phát triển và duy trì bởi Hiệp hội Đo ảnh và Viễn thám Hoa Kỳ (ASPRS) dưới dạng định dạng tiêu chuẩn hóa để trao đổi dữ liệu lidar và khả năng tương tác.

Tệp LAS lưu trữ thông tin chi tiết về từng điểm lidar, bao gồm tọa độ 3D (x, y và z), giá trị cường độ, mã phân loại và các thuộc tính bổ sung. Định dạng này hỗ trợ cả dữ liệu phản hồi rời rạc và dữ liệu lidar dạng sóng đầy đủ, cho phép lưu trữ nhiều phản hồi trên mỗi xung laser.

## Định dạng tệp LAS

Cấu trúc của tệp LAS bao gồm ba phần chính: tiêu đề tệp, bản ghi có độ dài thay đổi (VLR) và bản ghi dữ liệu điểm.

1. Tiêu đề tệp: Tiêu đề tệp chứa thông tin cần thiết về tệp LAS, chẳng hạn như phiên bản định dạng dữ liệu, định dạng dữ liệu điểm, số điểm, tọa độ hộp giới hạn, hệ quy chiếu tọa độ (CRS) và siêu dữ liệu khác. Nó cung cấp một bản tóm tắt về dữ liệu lidar có trong tệp.

2. Bản ghi độ dài thay đổi (VLR): VLR là tùy chọn và có thể lưu trữ siêu dữ liệu bổ sung và thông tin tùy chỉnh về dữ liệu lidar. VLR cho phép linh hoạt trong việc mở rộng định dạng để đáp ứng các yêu cầu cụ thể của người dùng. Ví dụ về VLR bao gồm thông tin về hệ thống cảm biến, thông số xử lý dữ liệu hoặc sơ đồ phân loại.

3. Bản ghi dữ liệu điểm: Bản ghi dữ liệu điểm lưu trữ các phép đo lidar thực tế. Mỗi bản ghi dữ liệu điểm đại diện cho một điểm lidar duy nhất và chứa các thuộc tính như tọa độ x, y và z, giá trị cường độ, mã phân loại (ví dụ: mặt đất, thảm thực vật, tòa nhà) và các thuộc tính khác do người dùng xác định. Bản ghi điểm cũng có thể lưu trữ dấu thời gian, số lần trả về và góc quét.

Các tệp LAS hỗ trợ các định dạng dữ liệu khác nhau (0 đến 10) để chứa nhiều loại dữ liệu lidar khác nhau và mức độ thông tin cần thiết. Ví dụ: định dạng 0 biểu thị định dạng điểm đơn giản với thông tin cơ bản, trong khi định dạng 1 đến 3 cung cấp dữ liệu toàn diện hơn bao gồm thông tin dạng sóng cho mỗi lần trả về.

Các tệp LAS được hỗ trợ rộng rãi bởi phần mềm lidar và các công cụ xử lý, khiến chúng trở thành định dạng tiêu chuẩn để trao đổi và phân tích dữ liệu lidar. Ngoài ra, các tệp LAS có thể được nén bằng kỹ thuật nén không mất dữ liệu để giảm kích thước tệp trong khi vẫn giữ được độ trung thực của dữ liệu gốc. Phiên bản nén của tệp LAS thường được gọi là LAZ, cung cấp khả năng lưu trữ và truyền dữ liệu hiệu quả.

## Người giới thiệu

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
