{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "file", "extension", "file format", "VB Project File", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Tìm hiểu về định dạng tệp VBPROJ và API có thể tạo và mở tệp VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp VBPROJ là gì?

Tệp có phần mở rộng .vbproj là tệp dự án Microsoft Visual Basic được công cụ MSBuild của Microsoft sử dụng để xây dựng các dự án trong giải pháp Visual Studio. Nó tương tự như tệp [CSPROJ](/vi/programming/csproj/) cho các dự án .NET được viết bằng [C#](/vi/programming/cs/). Công cụ MSBuild đọc thông tin chứa trong các nhóm khác nhau từ tệp VBPROJ và tạo tệp đầu ra. Tệp VBPROJ có thể chứa thông tin liên quan đến số nhận dạng toàn cầu, lớp và thuộc tính xác định dự án. Các tệp VBPROJ có thể được mở và chỉnh sửa bằng Microsoft Visual Studio và bất kỳ trình soạn thảo văn bản phổ biến nào, chẳng hạn như Notepad trên Hệ điều hành Windows và MacOS.

## Định dạng tệp VBPROJ - Thông tin khác

Tệp VBPROJ là tệp văn bản được viết ở định dạng tệp [XML](/vi/web/xml/) dựa trên [Lược đồ XML MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild- project-file-schema-reference?view=vs-2019). Tệp VBPROJ chứa thông tin ở dạng thẻ XML xác định thông tin liên quan đến nhóm cài đặt cụ thể đó. Bạn nên mở và chỉnh sửa các tệp cài đặt này trong Microsoft Visual Studio IDE.

### Phần tử VBPROJ

Các thành phần cấu thành của tệp Cài đặt VB như trong hình sau.

{{< figure src="../vbproj.png" alt="Định dạng tệp VBPROJ" >}}

Bảng sau đây mô tả ngắn gọn về các yếu tố này.

|Phần tử|Mô tả|
---|---|
|Dự án| Phần tử gốc của mọi tệp dự án và có thể bao gồm các thuộc tính để chỉ định các điểm nhập cho quy trình xây dựng ngoài việc xác định lược đồ XML cho tệp dự án|
|Thuộc tính và Điều kiện| Các thuộc tính bao gồm các cặp Khóa-giá trị và được xác định bằng phần tử Nhóm thuộc tính. Tên phần tử thuộc tính đại diện cho khóa thuộc tính và nội dung của phần tử xác định giá trị thuộc tính.|
|Các mục và Nhóm mục|Các mục trong tệp dự án là đầu vào cho quy trình xây dựng, chẳng hạn như tệp mã tệp, tệp cấu hình, tệp lệnh và các tệp khác được yêu cầu như một phần của quy trình xây dựng. Các mục đang và phải được xác định trong một phần tử Nhóm mục.|
|Mục tiêu và Nhiệm vụ| Phần tử Tác vụ đại diện cho một hướng dẫn xây dựng riêng lẻ (hoặc tác vụ). MSBuild bao gồm vô số tác vụ được xác định trước như Copy, CSC, VBC, Exec. Các tác vụ phải luôn được chứa trong Phần tử `Target` là một tập hợp gồm một hoặc nhiều tác vụ được thực hiện tuần tự và một tệp dự án có thể chứa nhiều mục tiêu.|

## Người giới thiệu

* [Hiểu tệp dự án](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/under Hiểu-the-project-file)
* [Các thành phần lược đồ MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

