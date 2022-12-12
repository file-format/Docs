{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "phần mở rộng", "tệp", "định dạng", "hệ thống", "cấu hình", "cài đặt", "chương trình", "máy tính", "ứng dụng" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Định dạng tệp",
  "description":"Tìm hiểu về định dạng tệp CFG và API có thể tạo và mở tệp CFG.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Tệp CFG là gì? ##

Tệp có phần mở rộng .cfg là một loại tệp "cài đặt". Nó là một loại tệp được sử dụng phổ biến và được sử dụng để lưu trữ thông tin liên quan đến cấu hình và cài đặt cho các chương trình máy tính. Hầu hết các loại tệp CFG được lưu trữ ở định dạng văn bản và không nên mở theo cách thủ công, thay vào đó, chúng nên được mở bằng trình chỉnh sửa văn bản. Tuy nhiên, có nhiều loại tệp CFG khác nhau, khác nhau ở định dạng lưu trữ thông tin. Các tính năng mà tệp CFG cung cấp khác nhau tùy theo ứng dụng. Một số ứng dụng máy tính cho phép người dùng sửa đổi hoặc phát triển cú pháp tệp cấu hình của họ bằng cách sử dụng các can thiệp đồ họa, trong khi những ứng dụng khác chỉ cho phép sửa đổi bằng trình soạn thảo văn bản. Sau khi sửa đổi các tệp này, người dùng có thể hướng dẫn ứng dụng đọc lại các tệp này và áp dụng các sửa đổi cho hệ thống.


## Định dạng tệp CFG ##

Các tệp CFG được hỗ trợ bởi nhiều hệ điều hành khác nhau, chẳng hạn như hệ điều hành giống Unix và Unix, MS-DOS, macOS, Microsoft Windows và IBM OS/2. Định dạng mà các tệp này được lưu trữ và sử dụng trong mỗi hệ điều hành này khác nhau. Hầu hết các hệ thống đã sử dụng và lưu trữ các tệp này ở định dạng văn bản thuần túy mà con người có thể đọc và chỉnh sửa được, trong khi các hệ thống khác lưu trữ ở định dạng phức tạp hơn, tùy thuộc vào việc sử dụng tệp và yêu cầu của hệ điều hành.

Trong Unix và các hệ điều hành tương tự Unix, hầu hết các tệp CFG đều sử dụng một số kiểu định dạng khác nhau cho tệp CFG, tuy nhiên, định dạng phổ biến nhất là định dạng văn bản thuần dễ đọc và hầu như tất cả các định dạng đều cho phép tạo và chỉnh sửa nhận xét. Các phần mở rộng tệp phổ biến nhất cho tệp CFG trong các hệ điều hành này là CNF, CONF, CF và INI.

Trong hệ điều hành MS-DOS ban đầu chỉ có một định dạng tệp cấu hình, cụ thể là văn bản thuần túy, tuy nhiên, MS-DOS 6, đã mang theo sự ra đời của định dạng tệp cấu hình INI.

macOS sử dụng tệp cấu hình kiểu định dạng danh sách thuộc tính tiêu chuẩn.

Trong Microsoft Windows, các tệp cấu hình kiểu INI văn bản thuần túy là một nguồn quan trọng để lưu trữ và chỉnh sửa thông tin, tuy nhiên, một hệ thống cơ sở dữ liệu mới đã được giới thiệu vào năm 1993, dẫn đến việc giảm sử dụng các tệp cấu hình trong Microsoft Windows sau năm 1993.


## Ví dụ về CFG ##

Một tệp CFG mẫu có thể được xem bên dưới:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
