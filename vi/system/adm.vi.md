{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp ADM - Định dạng tệp mẫu quản trị",
  "description":"Tìm hiểu về định dạng tệp ADM và cách mở tệp ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Một tập tin ADM là gì?

Tệp ADM là tệp mẫu được phần mềm Chính sách nhóm của Microsoft sử dụng để chỉ định vị trí của cài đặt chính sách dựa trên sổ đăng ký trong tệp đăng ký. Nó được quản trị viên hệ thống sử dụng để xác định chính sách quản lý một nhóm máy tính là một phần của nhóm. Thông tin này trở thành một phần của Đối tượng chính sách nhóm (GPO) được tạo để quản lý nhóm.

Bạn có thể mở tệp ADM bằng Trình chỉnh sửa đối tượng chính sách nhóm của Microsoft.

## Định dạng tệp ADM - Thông tin thêm

Các tệp ADM được lưu trữ dưới dạng tệp văn bản có định dạng unicode. Chúng chủ yếu được sử dụng để xác định vị trí của các cài đặt chính sách dựa trên sổ đăng ký trong sổ đăng ký Windows Vista và Windows 7.

Các tệp ADM không còn được hỗ trợ và đã được thay thế bằng các tệp [ADMX](/vi/system/admx/). GPA bỏ qua các tệp ADM mặc định sau trên máy tính chạy Microsoft Windows Vista Service Pack 1 trở lên.

* system.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Người giới thiệu

* [Tệp mẫu quản trị - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Quản lý tệp mẫu quản trị](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

