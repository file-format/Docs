{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "file", "extension", "file format", "Visual C++ Project", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Tìm hiểu về định dạng tệp VCXPROJ và API có thể tạo và mở tệp VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Tệp VCXPROJ là gì?

Tệp có phần mở rộng .vcxproj là tệp dự án Microsoft Visual C++ lưu trữ thông tin dự án [C++](/vi/programming/cpp/). Nó chứa thông tin được sử dụng bởi hệ thống dự án MSBuild để biên dịch và xây dựng đầu ra cuối cùng. VCXPROJ của các dự án Visual C++ giống như VCXPROJ của [CSPROJ](/vi/programming/csproj/) cho các dự án .NET. Các tệp VCXPROJ không chứa bất kỳ mã nào nhưng đề cập đến tất cả các lớp, mục tiêu và thuộc tính được xác định cho dự án để xây dựng dự án. Chúng có thể được mở trong trình soạn thảo văn bản thuần túy hoặc tốt hơn là trong Microsoft Visual Studio IDE.


## Định dạng tệp VCXPROJ - Thông tin khác

Tệp VCXPROJ là tệp văn bản được tạo ở định dạng tệp [XML](/vi/web/xml/). Những tệp này có thể được mở trong bất kỳ trình soạn thảo văn bản nào nhưng bạn nên sử dụng Microsoft Visual Studio IDE để mở và chỉnh sửa các tệp này. Chúng không được thiết kế để chỉnh sửa thủ công. Các lỗi có thể khiến IDE gặp sự cố hoặc hoạt động theo những cách không mong muốn.

Nội dung của tệp VCXPROJ mẫu như sau.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Thành phần tệp VCXPROJ

Một tệp VCXPROJ điển hình chứa một số thành phần như có thể thấy trong ví dụ XML ở trên. [Cấu trúc VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) của Microsoft giải thích chi tiết từng thành phần tệp và có thể tham khảo từ quan điểm của nhà phát triển.

#### Phần tử dự án

Đây là nút gốc của tệp VCXPROJ. MSBuild sử dụng phần tử này để đọc phiên bản xây dựng và mục tiêu mặc định để biên dịch.

#### ProjectConfigurations Phần tử nhóm mục

Nó chứa thông tin cấu hình dự án có thể bao gồm phương pháp xây dựng (Gỡ lỗi hoặc Phát hành), biên dịch 32 hoặc 64 bit, các tùy chọn tối ưu hóa và các tùy chọn khác. Thông tin trong nhóm này được IDE sử dụng để tải dự án.

#### Các yếu tố cấu hình dự án

Các phần tử ProjectConfiguration trong tệp VCXPROJ chứa thông tin về bản dựng và nền tảng mà dự án được tải. Tên của nó phải tuân theo định dạng `$(Cấu hình)|$(Nền tảng)`.

#### Phần tử nhóm thuộc tính toàn cầu

Phần này chứa các cài đặt cung cấp thông tin cho cấp độ dự án, chẳng hạn như:

* Hướng dẫn dự án
* Không gian gốc
* ApplicationType hoặc ApplicationTypeRevision


## Người giới thiệu

* [Cấu trúc VCXPROJ - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Tệp dự án C++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

