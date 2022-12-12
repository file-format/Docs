{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma file", "ma file format", "file format", "3d","ma file download", ".ma file", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp MA và API có thể mở và tạo tệp MA.",
  "title" :"Định dạng tệp MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## Tệp MA là gì?

Tệp có phần mở rộng .ma là tệp dự án 3D được tạo bằng ứng dụng Autodesk Maya. Nó chứa danh sách lớn các lệnh văn bản để chỉ định thông tin về tệp. Tệp **.ma** có thể được mở và chỉnh sửa trong bất kỳ trình soạn thảo văn bản nào để khắc phục mọi sự cố với các lệnh trong trường hợp tệp bị hỏng. Các tệp này chứa thông tin để xác định thông tin Cảnh 3D, chẳng hạn như hình học, ánh sáng, hoạt ảnh và hiển thị.

## Định dạng tệp MA

Các tệp MA được lưu vào đĩa ở định dạng văn bản ASCII không giống như các tệp MB được lưu ở định dạng tệp nhị phân vào đĩa. Tham khảo chi tiết về định dạng tệp MA có sẵn trong [Tài liệu Autodesk Maya](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) và có thể được giới thiệu để tham khảo của nhà phát triển.

### Tiêu đề tệp MA

Tiêu đề tệp MA bắt đầu bằng một phần nhận xét cung cấp thông tin tạo tệp và ngày sửa đổi. Trình đọc tệp Maya bỏ qua khối này vì nó chỉ được sử dụng cho mục đích thông tin. Tuy nhiên, tiêu đề phải bắt đầu bằng sáu ký tự đầu tiên là "//Maya".

Tiêu đề tệp ASCII trông giống như sau.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Tham chiếu tệp

Phần tham chiếu tệp của tệp .ma chứa thông tin về tất cả các tệp Maya khác đang được tham chiếu trong tệp này. Mỗi tệp được tham chiếu có thể được đọc bằng một lệnh tệp duy nhất được chứa trong cùng một tệp. Cú pháp của lệnh file khi được sử dụng để tham khảo là:

```
file -r -rpr prefixString fileName;
```
hoặc

```
file -r -ns nameSpace fileName
```
Đây là một chuỗi ví dụ.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Ví dụ này cho thấy rằng đối tượng mặt trời chứa trong tệp `solar` sẽ có thể truy cập được trong tệp này bằng cách sử dụng tên "solar_sun".

### Yêu cầu

Phần Yêu cầu của tệp .ma bao gồm một loạt lệnh bắt buộc và cho biết thông tin May, chẳng hạn như thông tin về phiên bản và phần bổ trợ cần thiết để đọc tệp. Một ví dụ về phần yêu cầu như sau.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


Phần tiếp theo chỉ định các yêu cầu. Điều này bao gồm một loạt các lệnh yêu cầu. Phần này của tệp cho Maya biết phần mềm nào cần thiết để tải tệp đúng cách. Cụ thể là phiên bản Maya nào và plug-in nào.

## tải xuống tệp MA
Hơi khó tìm và tải xuống tệp MA của mô hình 3d. Do đó, bạn có thể tải xuống tệp MA mẫu từ đây:

- [Sample.ma](../sample.ma)


## Người giới thiệu

* [Tổ chức tệp Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

