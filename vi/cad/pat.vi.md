{
  "date" : "2020-03-16",
  "keywords" :[ "Tệp PAT", "Định dạng", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp PAT và các API có thể tạo và mở tệp PAT.",
  "title" :"Định dạng tệp PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Tệp PAT là gì?

Tệp có phần mở rộng .pat là tệp CAD được sử dụng bởi phần mềm AutoCAD. Các ứng dụng có thể mở tệp PAT sử dụng mẫu hatch được lưu trữ trong các tệp này để lấy thông tin về kết cấu/độ đầy của một khu vực. Các mẫu chứa cung cấp thông tin về sự xuất hiện của vật liệu đối với các đối tượng được vẽ. Các tệp PAT có thể được mở trong các ứng dụng như Autodesk AutoCAD, CorelDRAW Graphics Suite và Ketron Software. Các tệp PAT có thể được chuyển đổi sang các định dạng hình ảnh khác nhau như JPG, PNG, BMP, v.v.

## Định dạng tệp PAT

Các tệp PAT được viết ở định dạng văn bản thuần túy và có thể được mở trong bất kỳ trình soạn thảo văn bản nào. Các mẫu nở trong các tệp này dựa trên vectơ và tuân theo cú pháp được nêu trong tài liệu AutoCAD.

Tất cả các mẫu bắt đầu tại điểm 0,0, mẫu được tính toán để bao phủ ranh giới nở.

### Định nghĩa mẫu

Tất cả các định nghĩa mẫu bao gồm các trường sau:
* Một sự dẫn đầu '\*'
* Tên - Tên không được có khoảng trắng, dấu chấm câu, dấu ngoặc đơn hoặc dấu gạch chéo.
* Một sự mô tả

Định dạng chuẩn cho các mẫu hatch là `<\*><name> <, mô tả>`. Tên và mô tả được phân tách bằng dấu phẩy và mô tả không được vượt quá độ dài dòng tám mươi ký tự. Các mẫu nở được xác định sau thông tin này.

### Ví dụ về mẫu nở
Sau đây là một ví dụ về mẫu hình vuông
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Một ví dụ khác cho thấy mô hình hình bình hành như sau.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Người giới thiệu ##

* [Các mẫu băm của Autodesk](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2018/ENU/AutoCAD-LT/files/GUID-A6F2E6FF-1717- 44B6-A476-0CA817ADD77E-htm.html)

