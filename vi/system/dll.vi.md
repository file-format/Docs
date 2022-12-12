{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "phần mở rộng", "tệp", "định dạng", "hệ thống", "Thư viện liên kết động", "cài đặt", "chương trình", "máy tính", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Thư viện liên kết động",
  "description":"Tìm hiểu về định dạng tệp DLL và các API có thể tạo và mở tệp DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Tệp DLL là gì? ##

Tệp DLL hoặc Thư viện liên kết động là một loại tệp thực thi. Đây là một trong những tệp mở rộng thường thấy nhất trên thiết bị của bạn và thường được lưu trữ trong thư mục System32 trên Windows của bạn. Tệp có đuôi DLL được phát triển bởi Microsoft và được họ sử dụng phổ biến. Nó có đánh giá người dùng phổ biến cao. DLL hoạt động như một giá chứa *trình điều khiển/quy trình/chức năng/thuộc tính* được máy chủ windows thiết kế và áp dụng cho một chương trình/ứng dụng. Một tệp DLL duy nhất cũng có thể được chia sẻ giữa các chương trình cửa sổ khác nhau. Các tệp mở rộng này rất quan trọng để các chương trình Windows trên thiết bị của bạn chạy trơn tru vì chúng chịu trách nhiệm kích hoạt và chạy các chức năng khác nhau trên chương trình, chẳng hạn như ghi và đọc tệp, kết nối với các thiết bị khác bên ngoài thiết lập của bạn.
Tuy nhiên, những Tệp này chỉ có thể được mở trên thiết bị hỗ trợ bất kỳ phiên bản Windows nào (windows 7/windows 10/v.v.) và do đó không thể mở trực tiếp trên thiết bị hỗ trợ Mac OS. (Nếu bạn muốn mở tệp DLL trên Mac OS, nhiều ứng dụng bên ngoài có thể giúp mở chúng.)


## Định dạng tệp DLL ##

Tệp DLL được phát triển bởi Microsoft và có phần mở rộng ".dll" đại diện cho loại. Nó đã là một phần không thể thiếu của máy chủ Windows 1.0 và hơn thế nữa. Nó là một loại tệp nhị phân và được hỗ trợ bởi tất cả các phiên bản của Microsoft Windows. Loại tệp này được tạo nhằm mục đích tạo hệ thống thư viện dùng chung trong các chương trình Windows, cho phép chỉnh sửa hoặc thay đổi riêng biệt và độc lập trong thư viện chương trình mà không cần liên kết lại các chương trình.


## Ví dụ DLL ##

Mã ví dụ cho một điểm vào DLL có thể được tìm thấy bên dưới:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Tài liệu tham khảo ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
