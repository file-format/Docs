{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - Tệp trao đổi dữ liệu LIDAR nén",
  "description":"Tìm hiểu về định dạng tệp LAZ và các API có thể tạo và mở tệp LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## Tập tin LAZ là gì?

Định dạng tệp LAZ là phiên bản nén của định dạng tệp LAS (Lidar LASer), được thiết kế đặc biệt để lưu trữ dữ liệu đám mây điểm lidar. Các tệp LAZ giữ lại dữ liệu và cấu trúc giống như các tệp LAS nhưng sử dụng các kỹ thuật nén không mất dữ liệu để giảm kích thước tệp trong khi vẫn giữ được độ trung thực của dữ liệu gốc.

## Định dạng tệp LAZ - Lịch sử tóm tắt

Định dạng tệp LAZ được phát triển để giải quyết nhu cầu ngày càng tăng về lưu trữ và truyền tải hiệu quả các bộ dữ liệu lidar lớn. Bằng cách nén các tệp LAS, các tệp LAZ giảm đáng kể kích thước của chúng, giúp quản lý và chuyển chúng dễ dàng hơn. Việc nén đạt được bằng cách sử dụng kết hợp các thuật toán khác nhau, chẳng hạn như mã hóa entropy và mã hóa có độ dài thay đổi, để biểu diễn các thuộc tính điểm lidar ở dạng nhỏ gọn hơn.

## Định dạng tệp LAZ

Mặc dù bị nén nhưng các tệp LAZ vẫn có khả năng khôi phục hoàn toàn dữ liệu LAS gốc mà không bị mất thông tin. Điều này có nghĩa là khi tệp LAZ được giải nén, nó có thể được xử lý và phân tích theo cách tương tự như tệp LAS không nén. Quá trình nén và giải nén thường được thực hiện bằng phần mềm hoặc thư viện chuyên dụng hỗ trợ định dạng LAZ.

Định dạng tệp LAZ duy trì khả năng tương thích với các tệp LAS, đảm bảo khả năng tương tác giữa các công cụ xử lý và phần mềm lidar. Điều này có nghĩa là các ứng dụng có thể đọc và xử lý tệp LAS thường có thể xử lý các tệp LAZ mà không cần bất kỳ sửa đổi nào. Ngoài ra, các tệp LAZ vẫn bao gồm tiêu đề tệp, bản ghi có độ dài thay đổi (VLR) và bản ghi dữ liệu điểm, giữ nguyên cấu trúc như tệp LAS.

## Ưu điểm của định dạng tệp LAZ

**Kích thước tệp giảm:** Nén LAZ làm giảm đáng kể kích thước tệp của bộ dữ liệu lidar, giúp chúng dễ quản lý hơn, lưu trữ và chuyển giao dễ dàng hơn.

**Tính toàn vẹn dữ liệu:** Nén LAZ không mất dữ liệu, nghĩa là dữ liệu được giải nén là bản sao chính xác của dữ liệu LAS gốc, đảm bảo không mất thông tin hoặc độ chính xác.

**Khả năng tương tác:** Các tệp LAZ tương thích với các tệp LAS, cho phép tích hợp liền mạch với quy trình làm việc và phần mềm lidar hiện có.

**Xử lý hiệu quả:** Do kích thước giảm, các tệp LAZ có thể được tải và xử lý nhanh hơn, cải thiện thời gian xử lý và phân tích tổng thể.

Định dạng tệp LAZ đã được áp dụng rộng rãi trong cộng đồng lidar như một tiêu chuẩn để lưu trữ và trao đổi dữ liệu lidar nén. Nó cung cấp sự cân bằng giữa nén dữ liệu hiệu quả và tính toàn vẹn của dữ liệu, cho phép xử lý dễ dàng hơn các bộ dữ liệu lidar lớn trong khi vẫn duy trì độ chính xác và chất lượng của dữ liệu gốc.

## Người giới thiệu

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
