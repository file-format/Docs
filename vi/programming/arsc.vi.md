{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","tệp arsc là gì","cách mở tệp arsc", "phần mở rộng", "tệp", "tệp arsc","định dạng tệp arsc", "phần mở rộng tệp arsc", "ví dụ tệp arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Tệp bảng tài nguyên gói Android",
  "description":"Tìm hiểu về định dạng tệp ARSC và các API có thể tạo và mở tệp ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Tệp ARSC là gì?

Tệp ARSC là tệp bảng Tài nguyên Android chứa danh sách tài nguyên của ứng dụng ở định dạng bảng. Điều này chứa thông tin như tên tài nguyên, thuộc tính và ID. Các tệp ARSC là một phần của gói APK được sử dụng để cài đặt các ứng dụng Android này. Tất cả các tài nguyên như hình ảnh, bố cục, kiểu và chuỗi trong ứng dụng Android được chuyển đổi thành tệp nhị phân khi tệp APK được tạo. Tệp ARSC cũng được tạo cùng lúc, chứa danh sách tất cả các tài nguyên đã biên dịch của chương trình và ID của chúng.

## Định dạng tệp ARSC

Các tệp có đuôi .arsc là các tệp nhị phân được tạo sau khi trình biên dịch, chẳng hạn như ANT (Eclipse) hoặc Gradle (AS), biên dịch mã ứng dụng Android để tạo tệp [APK](/vi/compression/apk/). Bạn có thể giải nén tệp APK bằng bất kỳ tiện ích lưu trữ nào, chẳng hạn như WinZip để xem nội dung của nó, đó là các tệp lớp java đã biên dịch, tức là classes.dex. Ngoài những thứ này, nó còn chứa tệp ARSC này chứa thông tin meta về:

* Các nút XML
* Các thuộc tính
* ID tài nguyên

Tài nguyên trong tệp APK được gọi bằng ID tài nguyên, trong khi các thuộc tính được phân giải thành một giá trị trong thời gian chạy. Công cụ aapt của Android thu thập tất cả tài nguyên được xác định trong tệp tại thời điểm xây dựng và gán ID tài nguyên cho chúng. Sau khi các mã định danh được gán cho các tài nguyên đã biên dịch, tệp R.java được tạo từ mã nguồn cũng như resource.arsc.

## Người giới thiệu

* [Cấu trúc bảng tài nguyên nhị phân](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

