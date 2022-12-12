{
  "date" : "2019-12-16",
  "keywords" :[ "NB", "file", "extension", "file format", "Mathematica", "Spreadsheet" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Tìm hiểu về API tệp NB có thể tạo và mở tệp NB là gì.",
  "title" :"NB - Định dạng tệp sổ tay Mathematica",
  "linktitle" : "NB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2021-07-16"
}

## Tệp NB là gì?

Tệp có phần mở rộng .nb là định dạng tệp sổ ghi chép Wolfram lưu hướng dẫn cho các hướng dẫn toán học trong tệp văn bản. Nó có thể chứa nhiều loại dữ liệu khác nhau như tính toán trực tiếp, giao diện động tùy ý, đầu vào sắp chữ đầy đủ, đầu vào hình ảnh, chú thích mã tự động, giao diện lập trình cấp cao hoàn chỉnh và hàng nghìn chức năng và tùy chọn được tổ chức cẩn thận. Các hướng dẫn bằng văn bản là đầu vào và đầu ra Mathematica được tạo và cập nhật khi các câu lệnh đầu vào được đưa vào tệp.

## Định dạng tệp NB của Máy tính xách tay Wolfram - Thông tin khác

Các tệp NB của Wolfram Notebook được lưu ở định dạng văn bản thuần túy, đây là định dạng tệp mà con người có thể đọc được. Nội dung của sổ ghi chép được sắp xếp theo các phần dưới dạng văn bản thuần túy trong đó mỗi phần được biểu thị bằng các nhóm ô, tương tự như Bảng tính. Phạm vi của các nhóm này được xác định bởi một dấu ngoặc ở cuối mỗi ô. Kiểu được gán cho một ô xác định vai trò của nó trong sổ ghi chép như chi tiết bên dưới.

### Notebook dưới dạng Ngôn ngữ Wolfram

Khi dự định lưu Notebook bao gồm các hướng dẫn toán học để thực thi bởi Wolfram Language Kernal, các ô trong tài liệu sẽ tự động được gán kiểu văn bản `Input`. Điều này yêu cầu kernel coi đây là các hướng dẫn được thực thi khi người dùng thực hiện kết hợp các phím `Shift+Return`. Một Mathematica Notebook được hiển thị như trong ví dụ sau.

{{< figure src="../Wolfram Notebook.jpeg" alt="Định dạng tệp máy tính xách tay Wolfram" >}}

### Sổ ghi chép dưới dạng Tài liệu

Sổ tay Mathematica có thể ở định dạng tài liệu để cung cấp cái nhìn về những gì bạn thấy những gì bạn nhận được (WYSIWYG). Những tài liệu này giống như được xem trên màn hình hoặc trên giấy in và có tính tương tác. Đối với điều này, `Kiểu văn bản` được gán cho ô để hiển thị nội dung mà không cần Kernel thực thi các câu lệnh.

## Xuất sổ tay Mathematica

Mathematica Notebooks có thể được xuất sang nhiều định dạng tệp khác nhau như PDF, đồ họa, GIS, Nén và Bảng tính.

## Người giới thiệu

* [Thông tin cơ bản về Mathematica Notebook](https://reference.wolfram.com/lingu/guide/NotebookBasics.html)

