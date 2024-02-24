{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Tệp XDELTA - Tệp vi sai xdelta - Tệp .xdelta là gì và làm cách nào để mở nó?",
  "description" : "Tìm hiểu về Tệp vi sai xdelta và cách mở tệp đó.",
  "linktitle" : "XDELTA",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-xdelta-vi",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Tệp XDELTA là gì?

Định dạng tệp XDELTA chứa các khác biệt nhị phân giữa hai tệp khác và được tạo bởi công cụ xdelta, một tiện ích dòng lệnh để mã hóa delta, bao gồm việc tính toán sự khác biệt giữa hai tệp và mã hóa những khác biệt đó ở định dạng nhỏ gọn. Tệp XDELTA lưu trữ dữ liệu nhị phân thể hiện những thay đổi hoặc khác biệt giữa tệp gốc và tệp được cập nhật. Dữ liệu nhị phân trong tệp XDELTA thể hiện những thay đổi cần thiết để chuyển đổi một tệp (bản gốc) thành tệp khác (phiên bản cập nhật hoặc bản vá).

Các tệp XDELTA thường được sử dụng trong cộng đồng trò chơi để phân phối các sửa đổi (mod) cho trò chơi điện tử. Những bản mod này có thể bao gồm mọi thứ, từ những thay đổi về mặt thẩm mỹ cho đến những thay đổi đáng kể trong cơ chế chơi trò chơi. Tệp XDELTA cho phép người dùng áp dụng những sửa đổi này cho quá trình cài đặt trò chơi của họ bằng cách vá các tệp trò chơi gốc với những thay đổi được chỉ định trong tệp XDELTA.

## xdelta

`xdelta` là một tiện ích dòng lệnh được sử dụng để mã hóa và giải mã delta; nó chủ yếu được sử dụng để tạo và áp dụng các bản vá nhị phân, thường được gọi là bản vá delta hoặc bản vá xdelta, giữa hai tệp; các bản vá này thể hiện sự khác biệt giữa tệp gốc và phiên bản đã sửa đổi hoặc cập nhật, cho phép phân phối các bản cập nhật một cách hiệu quả, đặc biệt trong các trường hợp băng thông hoặc dung lượng lưu trữ bị hạn chế.

Dưới đây là tổng quan ngắn gọn về các chức năng chính của `xdelta`:

1.  **Creating patches**: `xdelta` can generate a patch file that contains differences between two files. This patch file, often referred to as an "xdelta patch", is relatively small compared to original and updated files, as it only contains the changes between them.
    
2.  **Applying patches**: Once a patch file is created, `xdelta` can apply it to original file to produce updated file. This process involves taking original file and patch file as input and applying changes specified in patch file to generate updated file.
    
3.  **Applying reverse patches**: `xdelta` can also apply reverse patches, which revert changes made to a file. This is useful for rolling back updates or modifications.
    

`xdelta` thường được sử dụng trong nhiều trường hợp khác nhau, chẳng hạn như phân phối các bản cập nhật phần mềm, vá lỗi trò chơi điện tử và cập nhật tệp hệ thống trong các thiết bị nhúng hoặc thiết bị mạng. Nó cung cấp một cách linh hoạt và hiệu quả để quản lý cập nhật tệp trong khi giảm thiểu yêu cầu sử dụng băng thông và lưu trữ.

## xdeltaui

xdeltaui là một ứng dụng giao diện người dùng đồ họa (GUI) để quản lý và áp dụng các bản vá XDELTA. xdelta gui cung cấp giao diện thân thiện với người dùng để người dùng tương tác với các tệp XDELTA và áp dụng chúng cho các tệp gốc tương ứng, vá hoặc cập nhật chúng một cách hiệu quả.

Không giống như phiên bản dòng lệnh của xdelta, hoạt động thông qua các lệnh dựa trên văn bản, xdeltaui cung cấp một cách trực quan hơn để xử lý các tệp XDELTA, đặc biệt đối với những người dùng không quen với giao diện dòng lệnh hoặc thích các công cụ đồ họa.

Với xdeltaui, người dùng thường có thể thực hiện các tác vụ như chọn tệp gốc, chọn tệp bản vá XDELTA và áp dụng bản vá để tạo tệp cập nhật. Điều này có thể đặc biệt hữu ích khi cài đặt các bản mod hoặc bản cập nhật cho trò chơi điện tử hoặc các ứng dụng phần mềm khác.

## Tải xuống xdelta

Trên hệ thống Linux, bạn có thể sử dụng các trình quản lý gói như `apt`, `yum` hoặc `dnf` để cài đặt `xdelta`. Ví dụ: trên Ubuntu, bạn có thể sử dụng lệnh sau:

```
sudo apt-get install xdelta3
```

## Cách sử dụng xdelta

Để sử dụng `xdelta`, bạn thường cần làm theo các bước chung sau:

1.  **Tải xuống và cài đặt**: Trước tiên, hãy đảm bảo rằng bạn đã cài đặt `xdelta` trên hệ thống của mình. Bạn có thể tải xuống từ trang web chính thức, trình quản lý gói hoặc các nguồn đáng tin cậy khác.
    
2.  **Prepare Files**: Prepare original file (often called source or base file) and updated file (target file) that you want to create a patch for or apply a patch to.
    
3.  **Tạo bản vá**:
    
- Mở giao diện dòng lệnh của bạn (thiết bị đầu cuối hoặc dấu nhắc lệnh).
- Sử dụng lệnh `xdelta` với các tùy chọn phù hợp để tạo bản vá. Cú pháp cơ bản là:
               
```
đồng bằng xdelta<original_file><updated_file><patch_output_file>
```
        
Thay thế `<original_file> ` với đường dẫn đến tập tin gốc, `<updated_file> ` với đường dẫn đến tệp được cập nhật và `<patch_output_file> ` với tên mong muốn cho tệp vá.
- Ví dụ:
               
```
xdelta delta original_file đã cập nhật_file patch.xdelta
```
        
4.  **Áp dụng bản vá**:
    
- Đảm bảo bạn có sẵn file gốc và file patch.
- Mở giao diện dòng lệnh của bạn.
- Sử dụng lệnh `xdelta` với các tùy chọn thích hợp để áp dụng bản vá. Cú pháp cơ bản là:
        
      
```
bản vá xdelta<original_file><patch_file><output_file>
```
        
Thay thế `<original_file> ` với đường dẫn đến tập tin gốc, `<patch_file> ` với đường dẫn đến tệp vá và `<output_file> ` với tên mong muốn cho tệp đầu ra.
- Ví dụ:
                
```
bản vá xdelta original_file patch.xdelta update_file
```
        
5.  **Xem trợ giúp**: Nếu bạn cần hỗ trợ với các tùy chọn hoặc lệnh cụ thể, bạn có thể sử dụng lệnh `xdelta` với tùy chọn `--help` để hiển thị thông tin sử dụng và các tùy chọn có sẵn.
    
## Cách mở tệp XDELTA

Các tệp XDELTA không dành cho việc mở trực tiếp. Nếu bạn muốn áp dụng bản vá XDELTA cho trò chơi hoặc tệp khác, bạn có tùy chọn sử dụng xdelta, tương thích trên nhiều nền tảng hoặc giao diện người dùng xdelta, được thiết kế riêng cho người dùng Windows.

## Người giới thiệu
* [xdelta](https://en.wikipedia.org/wiki/Xdelta)


