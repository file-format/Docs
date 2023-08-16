{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp PDF/X",
  "description":"Tìm hiểu về định dạng tệp PDF/X và API có thể tạo và mở tệp PDF/X.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Tập tin PDF/X là gì? #

PDF/X là một tiêu chuẩn ISO 15930 được xuất bản vào năm 2001 với một tập hợp con các chức năng PDF. Tiêu chuẩn được thiết lập và công bố dựa trên các yêu cầu cụ thể của ngành in ấn và xuất bản. Tất cả các yêu cầu đối với tiêu chuẩn này đều được xây dựng theo nhu cầu đa dạng của ngành in ấn và xuất bản. PDF/X yêu cầu các tệp tuân thủ phải hoàn chỉnh, nghĩa là phải độc lập. Điều này yêu cầu các yếu tố như phông chữ được sử dụng trong trang phải là một phần của tài liệu. Các nội dung như 3D hoặc video không thể là một phần của tài liệu PDF/X. Thông tin chứa trong tài liệu PDF/X yêu cầu phải chính xác.

## Các tiêu chuẩn và sửa đổi PDF/X ##

Nhóm tiêu chuẩn PDF/X bao gồm một số phiên bản, mỗi phiên bản được thiết kế cho một kết quả chuyên biệt. Sự phát triển của các tiêu chuẩn này nhằm giải quyết nhiều nhu cầu đa dạng của ngành in ấn và xuất bản.

* `PDF/X-1a` - Còn được gọi là tiêu chuẩn đầu tiên của dòng PDF/X, PDF/X-1a yêu cầu tất cả nội dung phải là một phần của tài liệu PDF để có thể in được. Không được phép sử dụng các thành phần tài liệu như phông chữ, biểu mẫu, mật khẩu bảo vệ và chú thích hiển thị. PDF/X-1a có các yêu cầu cụ thể của riêng nó cũng như những yêu cầu liên quan đến độ trong suốt và các lớp được cho phép. Những điều này cũng yêu cầu các thành phần in chỉ sử dụng CMYK, thang độ xám hoặc màu vết, dẫn đến không sử dụng RGB hoặc không gian màu độc lập với thiết bị. dành cho các trao đổi trong đó tất cả các tệp sẽ được phân phối ở CMYK (và/hoặc màu vết), không có dữ liệu RGB hoặc được quản lý màu. PDF/X-1a còn được gọi là Trao đổi hoàn chỉnh do tính đầy đủ của thông tin được yêu cầu bởi
* `PDF/X-3` - được giới thiệu vào năm 2002 và loại bỏ nhiều hạn chế của PDF/X-1a. Điều này cho phép đồ họa trong PDF/X-3 sử dụng các không gian màu dựa trên CMYK, grescale, RGB, Lab và ICC. Nó thực sự dựa trên tiêu chuẩn PDF 1.3 với [ICC profile](https://en.wikipedia.org/wiki/ICC_Profile). Nó còn được gọi là Quản lý màu do tính linh hoạt và các quy tắc mà nó đưa ra liên quan đến màu sắc có trong tài liệu PDF.
* `PDF/X-4` - hỗ trợ trong suốt, vì vậy PDF-X/4 chứa tất cả dữ liệu cần thiết cho đầu ra mà không làm phẳng.
* `PDF/X-5` - dựa trên PDF/X-4, thêm hỗ trợ cho đồ họa bên ngoài thông qua các XObject tham chiếu, cũng như các cấu hình n-colorant bên ngoài cho mục đích hiển thị. Sử dụng nó để trao đổi một phần dữ liệu in bằng PDF phiên bản 1.6

## Người giới thiệu ##

* [PDF/X - Theo Wikipedia](https://en.wikipedia.org/wiki/PDF/X)

