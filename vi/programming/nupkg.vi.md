{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp NUPKG - Tệp gói NuGet",
  "description":"Tìm hiểu về định dạng tệp NUPKG và API có thể tạo và mở tệp NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## Tệp NUPKG là gì?

Tệp NUPKG là một tệp gói chứa mã nguồn được phần mềm NuGet sử dụng để tạo các gói được sử dụng trong các dự án .NET. Thành phần Trình quản lý gói NuGet được cài đặt như một phần của Microsoft Visual Studio để tìm nạp các gói từ kho lưu trữ gói trực tuyến. Các tệp NUPKG giúp nhà phát triển tìm nạp các gói mới nhất từ [Nuget.org](https://nuget.org) bằng Trình quản lý gói NuGet thay vì tải xuống và cài đặt các gói phát triển theo cách thủ công. Các tệp NUPKG được tạo từ các tệp NUSPEC và khi được tải xuống, hãy cài đặt gói trên hệ thống người dùng.

## Định dạng tệp NUPKG

Các tệp NUPKG là các tệp lưu trữ [ZIP](/vi/compression/zip/) chứa các thư viện được đóng gói bên trong nó. Khi được tải xuống, nó có thể được đổi tên thành .zip và được giải nén bằng bất kỳ tiện ích zip tiêu chuẩn nào như WinZIP, 7-Zip và Tiện ích lưu trữ của Apple.

## Tài liệu tham khảo

* [Nuget.org](https://nuget.org)
* [Khởi động nhanh: Cài đặt và sử dụng gói trong Visual Studio (chỉ dành cho Windows)](https://learn.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- phòng thu)
* [Cách tạo và xuất bản gói Nuget](https://learn.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- cli)

