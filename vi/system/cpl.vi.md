{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "phần mở rộng", "tệp", "định dạng", "hệ thống", "Tệp bảng điều khiển", "Windows", "chương trình", "máy tính", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Tệp bảng điều khiển",
  "description":"Tìm hiểu về định dạng tệp CPL và các API có thể tạo và mở tệp CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Tệp CPL là gì? ##

Tệp CPL là một loại tệp "hệ thống". Nó được sử dụng bởi hệ điều hành Windows. Tệp CPL là viết tắt của Tệp bảng điều khiển. Các tệp này là tệp nhị phân mở bằng bảng điều khiển trong hệ điều hành Microsoft Windows và được sử dụng để biểu thị và mở các công cụ có sẵn trong bảng điều khiển, chẳng hạn như Chuột, Màn hình, Kết nối mạng, trong số những công cụ khác. Các tệp CPL thường được lưu trữ trong thư mục hệ thống trên thiết bị của bạn. Không nên mở các tệp này theo cách thủ công.


## Định dạng tệp CPL ##

Các tệp CPL khác nhau trong hệ điều hành Windows của bạn được kết nối để đại diện cho các mục bảng điều khiển khác nhau. Tất cả các mục trong bảng điều khiển được liên kết với một tệp CPL và có hậu tố “.cpl” được đính kèm với các mục của chúng.

Một số loại tệp CPL phổ biến với định dạng của chúng là:

* Inetcpl.cpl – Dành cho các thuộc tính Internet trên thiết bị của bạn
* Appwiz.cpl – Để Thêm hoặc Xóa thuộc tính Chương trình trên thiết bị của bạn
* Desk.cpl – Dành cho thuộc tính Hiển thị
* Main.cpl – Dành cho các thuộc tính liên quan đến Chuột, Phông chữ, Bàn phím và Máy in.
* Netcpl.cpl – Dành cho các thuộc tính liên quan đến Mạng
* System.cpl – Đối với các thuộc tính liên quan đến Hệ thống và để Thêm trình hướng dẫn Phần cứng Mới
* TimeDate.cpl – Đối với thuộc tính Ngày hoặc Giờ
* Mlcfg32.cpl – Dành cho thuộc tính Microsoft Exchange hoặc Windows Messaging
* Intl.cpl – Điều này liên quan đến thuộc tính Cài đặt khu vực
* Modem.cpl – Dành cho các thuộc tính liên quan đến Modem
* Themes.cpl – Lưu trữ Chủ đề và thuộc tính của Máy tính để bàn.
* Password.cpl – Đối với thuộc tính Mật khẩu
* Mmsys.cpl – Dành cho thuộc tính Đa phương tiện
* Wgpocpl.cpl – Liên quan đến Microsoft Mail Post Office

## Lược Sử ##

Loại tệp CPL được phát triển bởi Microsoft Windows và là một phần không thể thiếu của hệ điều hành Windows kể từ Windows 1.0. Nó vẫn được sử dụng trong tất cả các phiên bản Windows và tất cả các thuộc tính mục của bảng điều khiển được lưu trữ bằng loại tệp này.

## Ví dụ CPL ##

Một tệp CPL mẫu có thể được xem bên dưới:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
