{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Tệp APPX là gì?",
  "description":"Tìm hiểu về định dạng tệp APPX và API có thể tạo và mở tệp APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Tệp APPX là gì?

Tệp APPX là định dạng tệp gói có thể phân phối được sử dụng để phân phối và cài đặt ứng dụng. Nó đã được giới thiệu với Windows 8 để được xuất bản trên Microsoft Windows Store. Nó chứa tất cả các tệp cần thiết để cài đặt ứng dụng Windows. Chúng bao gồm siêu dữ liệu, tệp và thông tin đăng nhập. Định dạng tệp đóng gói hiện đại hơn là MSIX hiện được sử dụng phổ biến hơn so với APPX.

## Định dạng tệp APPX - Thông tin khác

Các tệp APPX được lưu dưới dạng tệp nén ở định dạng tệp [ZIP](/vi/compression/zip/). Điều này làm cho toàn bộ gói dưới dạng một tệp lưu trữ với kích thước tệp được giảm để dễ dàng tải lên Microsoft Store.

## Làm cách nào để xem các tệp trong tệp APPX?

Để xem nội dung hoặc tệp bên trong tệp APPX, cần thực hiện theo các bước sau.

1. Vì các tệp APPX được lưu trữ dưới dạng tệp ZIP nén, hãy đổi tên tệp thành phần mở rộng .zip
1. Sử dụng bất kỳ công cụ giải nén nào như 7-Zip, WinZip hoặc WinRAR để giải nén các tệp có trong tệp APPX

## Làm cách nào để tạo tệp APPX?

Có hai phương pháp có thể được sử dụng để tạo tệp APPX.

1. Sử dụng MakeApp.exe - [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) được sử dụng để tạo cả hai gói ứng dụng (.msix hoặc .appx) và tệp gói gói ứng dụng .msixbundle hoặc .appxbundle). Ngoài ra, nó có thể trích xuất các tệp từ gói ứng dụng. MakeApp.exe khả dụng với Windows 10 SDK và có thể được sử dụng từ dấu nhắc lệnh.
1. Sử dụng Microsoft Visual Studio - Nhà phát triển thường [tạo tệp APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) bằng Microsoft Visual Studio. Khi quá trình phát triển ứng dụng hoàn tất và ứng dụng đã sẵn sàng để xuất bản, tệp gói APPX có thể được tạo bằng cách xuất bản tệp từ bên trong Visual Studio.

## Người giới thiệu

* [Tạo gói hoặc gói MSIX với MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Tạo tệp APPX bằng Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

