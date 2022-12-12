{
  "date" : "2021-08-11",
  "keywords" :[ "tệp wim", "định dạng tệp wim", "tệp wim là gì", "tệp", "ví dụ wim", "phần mở rộng tệp wim","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp WIM và các API có thể tạo và mở tệp WIM.",
  "title" :"WIM - Tệp định dạng hình ảnh Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Tệp WIM là gì?
Các tệp có phần mở rộng .wim lần đầu tiên được nhìn thấy trong Windows Vista. WIM thuộc về định dạng hình ảnh dựa trên tệp thường được giới thiệu trong Microsoft Windows Vista. Nó cho phép một hình ảnh đĩa duy nhất được triển khai trên nhiều nền tảng máy tính khác nhau. Các tệp WIM được sử dụng để quản lý các tệp như bản cập nhật, trình điều khiển và các thành phần mà không cần khởi động lại hình ảnh hệ điều hành. Tệp AQ WIM chứa một tập hợp các tệp và siêu dữ liệu được liên kết rất giống với các định dạng tệp đĩa khác.

## Định dạng tệp WIM
Định dạng tệp WIM không giống như các định dạng dựa trên ngành như VHD hoặc IS, trên thực tế, nó dựa trên tệp có nghĩa là đơn vị thông tin cơ bản trong WIM là một tệp. Lợi ích cơ bản của việc dựa trên tệp là lưu trữ một phiên bản tệp được tham chiếu nhiều lần trong cây hệ thống tệp và độc lập với phần cứng. Nó giảm chi phí mở và đóng các tệp khác nhau riêng lẻ vì các tệp được lưu trữ bên trong một WIM duy nhất tập tin. Các tệp WIM có thể lưu trữ nhiều ảnh đĩa, được tham chiếu bằng tên duy nhất hoặc theo chỉ số số của chúng.
### Hỗ trợ thuật toán nén
WIM hỗ trợ các họ thuật toán nén sau theo tốc độ giảm dần và tỷ lệ tăng dần:
- XPRESS
- LZX
- LZMS
- Nén rắn.
Ba họ đầu tiên dựa trên LZ77 trong khi Nén rắn được giới thiệu cùng với LZMS trong WIMGAPI Windows 8 và DISM Windows 8.1.
### Công cụ cho định dạng tệp WIM
Các công cụ sau đây thường hỗ trợ định dạng tệp WIM:

- **ImageX**: Một công cụ dòng lệnh được sử dụng để chỉnh sửa, tạo và triển khai ảnh đĩa Windows ở Định dạng Hình ảnh Windows. Cùng với WIMGAPI có liên quan, Nó được phân phối như một phần của Bộ cài đặt tự động Windows miễn phí. Bắt đầu với Windows Vista, Thiết lập Windows sử dụng API WAIK để cài đặt Windows.
- **DISM**: Một công cụ được giới thiệu trong Windows 7 và Windows Server 2008 R2 có thể thực hiện các tác vụ liên quan đến dịch vụ trên ảnh cài đặt Windows, có thể là ảnh trực tuyến hoặc ảnh ngoại tuyến trong một thư mục hoặc tệp WIM. công cụ này có khả năng gắn và ngắt kết nối hình ảnh, thêm trình điều khiển thiết bị vào hình ảnh ngoại tuyến và truy vấn trình điều khiển thiết bị đã cài đặt trong hình ảnh ngoại tuyến.
 




## Người giới thiệu


* [Định dạng hình ảnh Windows - theo Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


