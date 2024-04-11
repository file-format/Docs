{
  "date" : "2019-10-11",
  "keywords" :[ "tệp rtf", "định dạng tệp rtf", "tệp rtf là gì", "tệp", "ví dụ rtf", "phần mở rộng tệp rtf","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Định dạng văn bản có định dạng",
  "description":"Tìm hiểu về định dạng tệp RTF và các API có thể tạo và mở tệp RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Tệp RTF là gì?

Được Microsoft giới thiệu và ghi lại, Định dạng văn bản có định dạng (**RTF**) đại diện cho một phương pháp mã hóa văn bản và đồ họa được định dạng để sử dụng trong các ứng dụng. Định dạng tạo điều kiện trao đổi tài liệu đa nền tảng với các Sản phẩm khác của Microsoft, do đó phục vụ mục đích tương tác. Khả năng này làm cho nó trở thành tiêu chuẩn truyền dữ liệu giữa phần mềm xử lý văn bản và do đó, nội dung có thể được chuyển từ hệ điều hành này sang hệ điều hành khác mà không làm mất định dạng tài liệu. Thông số định dạng tệp được Microsoft cung cấp để tải xuống công khai và có thể được tham khảo từ quan điểm của nhà phát triển.

## Lịch sử tóm tắt về định dạng tệp RTF ##

Định dạng tệp RTF đã trải qua một số sửa đổi kể từ khi xuất bản. Phiên bản chính thức của nó để đọc/ghi đã được xuất bản như một phần của Microsoft Word 3.0 cho Macintosh với thông số kỹ thuật của phiên bản 1.0. Phiên bản cuối cùng của thông số kỹ thuật, 1.9.1 đã được Microsoft xuất bản vào tháng 3 năm 2008. Không có thêm cải tiến nào đối với thông số kỹ thuật sau phiên bản này. Hiện tại, hầu hết tất cả các hệ điều hành đều có nhiều ứng dụng giàu tính năng hơn đã giảm thiểu/xóa bỏ việc sử dụng định dạng tệp RTF.

## Thông số kỹ thuật định dạng tệp RTF ##

RTF đóng vai trò là tiêu chuẩn truyền dữ liệu giữa phần mềm xử lý văn bản và truyền nội dung từ hệ điều hành này sang hệ điều hành khác. Điều này đạt được bằng cách sử dụng các từ điều khiển được giới thiệu bởi Microsoft Office Word cho đến năm 2007. Tệp RTF tiêu chuẩn bao gồm ASCII để biểu thị văn bản có định dạng và với các ký tự không phải ASCII được chuyển đổi thành các giá trị mã thích hợp. Các phiên bản Word mới hơn có thể đọc các tệp RTF được tạo bằng các phiên bản trước, trong khi các phiên bản cũ hơn bỏ qua các từ và nhóm điều khiển mà chúng không hiểu.

### Tìm hiểu nền tảng của RTF ###

Các tệp RTF sử dụng văn bản thuần ASCII 7 bit, bao gồm:

* kiểm soát từ
* ký hiệu điều khiển, và
* các nhóm.

Chúng hoạt động như các khối xây dựng để biểu diễn dữ liệu RTF dưới dạng mã hóa ký tự và văn bản dễ hiểu.

#### Từ điều khiển ####

Chúng đại diện cho lệnh được định dạng đặc biệt được sử dụng để đánh dấu các ký tự để hiển thị và không thể dài hơn 32 chữ cái. Một từ điều khiển được xác định bởi:

\<ASCII Letter Sequence> //<//Delimiter//> //

Mỗi từ điều khiển phân biệt chữ hoa chữ thường và bắt đầu bằng dấu gạch chéo ngược. Dãy chữ cái ASCII có thể chứa các bảng chữ cái ASCII (a đến z và A đến Z). Các<Delimite> đánh dấu phần cuối của tên của từ điều khiển và có thể là một trong những từ sau:

* Một không gian. Điều này chỉ phục vụ để phân định một từ điều khiển và được bỏ qua trong quá trình xử lý tiếp theo.
* Một chữ số hoặc dấu trừ ASCII, cho biết rằng một tham số số được liên kết với từ điều khiển. Chuỗi số tiếp theo sau đó được phân định bằng bất kỳ ký tự nào không phải là chữ số ASCII (thường là một từ điều khiển khác bắt đầu bằng dấu gạch chéo ngược). Tham số có thể là số thập phân dương hoặc âm. Phạm vi giá trị của số trên danh nghĩa là –32768 đến 32767, tức là số nguyên 16 bit có dấu. Một số lượng nhỏ các từ điều khiển nhận các giá trị trong phạm vi‌ −2.147.483.648 đến 2.147.483.647 (số nguyên có dấu 32 bit). Các từ điều khiển này bao gồm **\binN**, **\revdttmN//**, **\rsidN** các từ điều khiển liên quan và một số thuộc tính hình ảnh như **\bliptagN**. Ở đây **N** là viết tắt của tham số số. Trình phân tích cú pháp RTF phải cho phép tối đa 10 chữ số tùy ý đứng trước dấu trừ. Nếu dấu phân cách là một khoảng trắng, thì dấu phân cách đó sẽ bị loại bỏ, nghĩa là nó không được đưa vào quá trình xử lý tiếp theo.
* Bất kỳ ký tự nào không phải là chữ cái hoặc chữ số. Trong trường hợp này, ký tự phân cách kết thúc từ điều khiển và không phải là một phần của từ điều khiển. Chẳng hạn như dấu gạch chéo ngược “\”, có nghĩa là một từ điều khiển mới hoặc ký hiệu điều khiển theo sau.

#### Biểu tượng điều khiển ####

Biểu tượng Kiểm soát biểu thị một sự kiện đặc biệt có ý nghĩa cụ thể tùy thuộc vào nội dung của nó. Nó bao gồm một dấu gạch chéo ngược theo sau bởi một ký tự đặc biệt (ký tự không phải bảng chữ cái) và không có bất kỳ dấu phân cách nào.

#### Tập đoàn ####

Một nhóm có thể bao gồm văn bản, từ điều khiển hoặc ký hiệu điều khiển được đặt trong dấu ngoặc nhọn (**{ }**). Dấu ngoặc mở (**{** ) biểu thị bắt đầu nhóm và dấu ngoặc đóng ( **}**) biểu thị kết thúc nhóm. Mỗi nhóm chỉ định văn bản chịu ảnh hưởng của nhóm và các thuộc tính khác nhau của văn bản đó.

### Cấu trúc tệp RTF ###

Tệp RTF có cú pháp Chuẩn sau:

Được Microsoft giới thiệu và ghi lại, Định dạng văn bản có định dạng (**RTF**) đại diện cho một phương pháp mã hóa văn bản và đồ họa được định dạng để sử dụng trong các ứng dụng. Định dạng tạo điều kiện trao đổi tài liệu đa nền tảng với các Sản phẩm khác của Microsoft, do đó phục vụ mục đích tương tác. Khả năng này làm cho nó trở thành tiêu chuẩn truyền dữ liệu giữa phần mềm xử lý văn bản và do đó, nội dung có thể được chuyển từ hệ điều hành này sang hệ điều hành khác mà không làm mất định dạng tài liệu. Thông số định dạng tệp được Microsoft cung cấp để tải xuống công khai và có thể được tham khảo từ quan điểm của nhà phát triển.

#### Tiêu đề RTF ####

Tiêu đề RTF có biểu diễn sau.

|Trường|Mô tả
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Các bảng tiêu đề phải xuất hiện theo thứ tự này nếu chúng tồn tại. Tệp RTF có thể bao gồm các nhóm phông chữ, kiểu, màu màn hình, ảnh, chú thích cuối trang, nhận xét (chú thích), đầu trang và chân trang, thông tin tóm tắt, trường, dấu trang, tài liệu-, phần-, đoạn văn và thuộc tính định dạng ký tự, toán học, hình ảnh, đối tượng. Nếu phông chữ, tệp, kiểu, màu, dấu sửa đổi và nhóm thông tin tóm tắt cũng như thuộc tính định dạng tài liệu được bao gồm trong tệp thì chúng phải xuất hiện trong tiêu đề RTF, nằm trước phần thân RTF. Nếu không sử dụng nội dung của nhóm nào thì có thể bỏ qua nhóm đó. Bất kỳ nhóm nào sử dụng các thuộc tính được xác định trong một nhóm khác phải xuất hiện sau nhóm xác định các thuộc tính đó. Ví dụ: thuộc tính màu sắc và phông chữ phải đứng trước nhóm kiểu.

#### Phiên bản RTF ####

Một tài liệu RTF phải bắt đầu bằng sáu ký tự sau:

```
{\rtf1
```
trong đó 1 hiển thị số phiên bản RTF.

#### Bộ ký tự ####

Sau {\rtf1, tài liệu sẽ khai báo bộ ký tự mà nó sử dụng. Cách khai báo một bộ ký tự bằng một trong các lệnh sau:

`\ansi` - Tài liệu nằm trong bộ ký tự ANSI, còn được gọi là Mã Trang 1252, bộ ký tự MSWindows thông thường.

`\mac` - Tài liệu nằm trong bộ ký tự MacAscii, bộ ký tự thông thường trong các phiên bản cũ (trước 10) của Mac OS.

`\pc` - Tài liệu nằm trong Mã DOS Trang 437, bộ ký tự mặc định cho MS-DOS. Những người đánh máy có trí nhớ tốt sẽ lưu ý rằng đây là bộ ký tự vẫn được sử dụng để diễn giải các mã “Alt số”—nghĩa là khi bạn giữ phím Alt và nhập “130” trên bàn phím số, nó sẽ tạo ra ký tự é, bởi vì 130 trong CP437 là é. Đó là cách sử dụng duy nhất mà CP437 thấy hiện nay.

`\pca` - Tài liệu nằm trong Trang mã DOS 850, còn được gọi là Trang mã đa ngôn ngữ MS-DOS.

#### Lệnh phông chữ ####

Định nghĩa bộ ký tự được theo sau bởi lệnh `\deffN`. Điều này xác định rằng phông chữ số N là phông chữ mặc định cho tài liệu này. Số phông chữ N được tham chiếu từ bảng phông chữ. Lệnh `\deffN` là tùy chọn về mặt kỹ thuật, nhưng nó phải ở đó để đảm bảo an toàn vì một prolog phổ biến như sau chọn phông chữ 0 làm phông chữ mặc định.

`{\rtf1\ansi\deff0`

#### Bảng phông chữ ####

Tất cả các phông chữ có thể được sử dụng trong tài liệu được liệt kê trong bảng phông chữ trong đó mỗi phông chữ được biểu thị bằng một số phông chữ. Tài liệu phải có bảng phông chữ mặc dù một số chương trình cũng sẽ hoạt động mà không có bảng đó.

Cú pháp của bảng phông chữ là {\fonttbl //...declarations//...}, trong đó mỗi khai báo có cú pháp cơ bản sau:

`{\fnumber\familycommand Tên phông chữ;}`

Một bảng phông chữ với bốn khai báo như sau:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Trong tài liệu có bảng phông chữ đó, `{\f2stuff}` sẽ in “stuff” trong Courier New. Không thể sử dụng phông chữ trong tài liệu cho đến khi nó được liệt kê trong bảng phông chữ.

### Kết thúc tài liệu ###

Mọi tài liệu RTF phải kết thúc bằng }, để đóng nhóm được mở bởi { là ký tự đầu tiên trong tài liệu. Không có gì có thể theo sau } cuối cùng, ngoại trừ có thể là một dòng mới.

## Người giới thiệu ##

* [Định dạng văn bản có định dạng](https://en.wikipedia.org/wiki/Rich_Text_Format)

