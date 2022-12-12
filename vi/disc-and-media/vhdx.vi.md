{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Tìm hiểu về định dạng tệp VHDX và API có thể tạo và mở tệp VHDX.",
  "title" :"Định dạng tệp VHDX - Tệp VHDX là gì?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Tệp VHDX là gì?

Tệp VHDX là tệp ảnh đĩa ở định dạng tệp Đĩa cứng ảo v2. Nó chứa toàn bộ hệ điều hành có thể được tải và sử dụng như bất kỳ máy thông thường nào để kiểm tra phần mềm hoặc chạy phần mềm yêu cầu một hệ điều hành cụ thể. Một VHDX, mặc dù là một ảnh đĩa đầy đủ, được lưu trữ trong một tệp duy nhất. Phần mềm máy ảo như Parallels Desktop, Windows Virtual Machine và Virtual Box có thể tải và mở ảnh đĩa.

Có thể chuyển đổi tệp VHDX thành [VHD](/vi/disc-and-media/vhd/) bằng Hyper-V Manager hoặc thành [VDI](/vi/disc-and-media/vdi/) bằng VirtualBox.

## Định dạng tệp VHDX - Thông tin khác

Chi tiết về định dạng tệp VHDX được ghi lại đầy đủ và có sẵn trực tuyến dưới dạng [Thông số định dạng tệp VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477 ) trên Tài liệu Microsoft. Nó là một phần mở rộng của định dạng VHD và bao gồm các khả năng nâng cao. Định dạng tệp VHDX cung cấp các tính năng bổ sung có sẵn ở đĩa cứng ảo và các lớp tệp đĩa cứng ảo. Nó được tối ưu hóa hơn và mang lại kết quả tốt hơn cho cấu hình và khả năng của phần cứng lưu trữ. Các tệp VHDX có thể được mở

### Hỗ trợ Đĩa cứng Ảo trong VHDX

Nó hỗ trợ ba loại đĩa cứng ảo.

1. **Ổ cứng ảo cố định** - Đĩa cứng ảo được phân bổ kích thước dữ liệu cố định. Kích thước của đĩa cứng ảo không thay đổi khi thêm hoặc xóa dữ liệu.

1. **Đĩa cứng ảo động** - Đĩa cứng ảo có kích thước đĩa động. Kích thước của nó bất cứ lúc nào cũng lớn bằng dữ liệu thực tế được ghi vào nó và siêu dữ liệu. Kích thước tệp của nó tự động tăng lên khi dữ liệu được thêm hoặc xóa khỏi nó.

1. **Đĩa cứng ảo khác biệt** - Thể hiện dòng điện của đĩa cứng ảo dưới dạng một tập hợp các khối đã sửa đổi so với tệp đĩa cứng ảo gốc.

## Người giới thiệu

* [Thông số định dạng tệp VHDX](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - theo Wikipedia](https://vi.wikipedia.org/wiki/VHD_(file_format))

