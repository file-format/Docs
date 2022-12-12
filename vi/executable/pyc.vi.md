{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Tìm hiểu về định dạng tệp PYC và API có thể tạo và mở tệp PYC.",
  "title" :"Định dạng tệp PYC- Tệp được biên dịch bằng Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Tệp PYC là gì?

Tệp PYC là tệp đầu ra được biên dịch được tạo từ mã nguồn được viết bằng ngôn ngữ lập trình Python. Khi tệp PY được chạy bằng trình thông dịch Python, nó sẽ được chuyển đổi thành mã byte để thực thi. Đồng thời, mã byte đã biên dịch cũng được lưu dưới dạng tệp .pyc để sử dụng lại từ bộ đệm sau này nếu có.

## Cấu trúc của định dạng tệp PYC

Các tệp PYC ở dạng mã byte và thông số định dạng tệp của chúng không có sẵn công khai. Tuy nhiên, điều tra của một số nguồn cho thấy rằng [cấu trúc của tệp PYC](https://nedbatchelder.com/blog/200804/the_struct_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) bao gồm:

* `Một số ma thuật bốn byte`r - Chỉ đơn giản là hai byte thay đổi với mỗi thay đổi đối với mã sắp xếp và sau đó là hai byte 0d0a.
* `Dấu thời gian sửa đổi bốn byte` - Dấu thời gian sửa đổi Unix của tệp nguồn đã tạo ra .pyc, để nó có thể được biên dịch lại nếu nguồn thay đổi.
* `Đối tượng mã được sắp xếp theo thứ tự` - đầu ra của marshal.dump của đối tượng mã là kết quả của việc biên dịch tệp nguồn.

## Người giới thiệu

* [Cấu trúc của tệp .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)

