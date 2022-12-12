{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Maya Embedded language","file", "extension", "file format", "Maya 3D", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Định dạng tệp ngôn ngữ nhúng Maya",
  "description":"Tìm hiểu về định dạng tệp MEL và API có thể tạo và mở tệp MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## Tệp MEL là gì?

Tệp có phần mở rộng .mel (Ngôn ngữ nhúng Maya) là ngôn ngữ kịch bản được Autodesk Maya sử dụng để tạo giao diện đồ họa. Nó cho phép bạn tự động hóa việc tạo các yếu tố đồ họa bằng cách sử dụng các tập lệnh thực thi ngoài giao diện đồ họa của Maya. MEL cho phép bạn tạo giao diện đồ họa mà không cần học lập trình. Điều này đạt được bằng cách tạo Macro và các hành động tùy chỉnh giúp tăng tốc các tác vụ lặp đi lặp lại. Các quy trình và tập lệnh này cho phép bạn tạo mô hình tùy chỉnh, hoạt ảnh, động lực học và hiển thị tác vụ. Autodesk Maya 2020 có thể được sử dụng để mở và xem nội dung của tệp EML.

## Định dạng tệp MEL - Thông tin khác

[Hướng dẫn tham khảo](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) của lập trình viên hiện có sẵn cho các nhà phát triển trên phần tài liệu của Maya. MEL dựa trên các lệnh shell scripting, tương tự như UINX, để đạt được mọi thứ. Các lệnh dựa trên tập lệnh làm cho nó không liên quan đến lập trình hướng đối tượng và thông thường (OOP), dẫn đến việc không sử dụng cấu trúc dữ liệu, gọi hàm hoặc sử dụng OOP như trong các ngôn ngữ khác.

Một số điểm chính về MEL như sau.

`Nhận xét` - Mọi câu lệnh trong MEL phải kết thúc bằng dấu chấm phẩy (;), ngay cả ở cuối khối.

`Trả về giá trị` - Cho biết biểu thức trả về giá trị không tự động in giá trị trong MEL. Thay vào đó, nó gây ra lỗi.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Lệnh để tạo, chỉnh sửa và xóa` - Lệnh tương tự được sử dụng để tạo đối tượng, chỉnh sửa đối tượng hoặc truy vấn thông tin về đối tượng hiện có. Tuy nhiên, một cờ kiểm soát những gì (tạo, chỉnh sửa hoặc truy vấn) mà lệnh thực hiện.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Trả về Giá trị từ Hàm` - Cú pháp hàm tự động trả về một giá trị. Để nhận giá trị trả về bằng cú pháp lệnh, bạn phải đặt lệnh trong dấu ngoặc kép.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Người giới thiệu

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

