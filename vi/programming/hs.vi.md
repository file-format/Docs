{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Định dạng tập lệnh Haskell",
  "description":"Tìm hiểu về định dạng tệp HS là gì và các API có thể tạo và mở tệp HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Định dạng tệp bộ trợ giúp Java

## Tệp Java HS là gì?

Tệp có phần mở rộng .hs trong ngôn ngữ lập trình Java là tệp tài liệu trợ giúp được hệ thống Trợ giúp Java sử dụng khi nó được ứng dụng kích hoạt. Nó xác định bộ trợ giúp cho ứng dụng cụ thể được cài đặt và bao gồm nhiều tập hợp con như một phần của trợ giúp hệ thống cho ứng dụng. Chương trình Java phải có khả năng tìm thấy tệp bộ trợ giúp có tên kết thúc bằng phần mở rộng .hs.

## Thông tin bộ trợ giúp Java

Tệp .hs có thể chứa thông tin sau.

|Thông tin|Mô tả|
---|---|
|Tệp bản đồ|Tệp bản đồ được sử dụng để liên kết ID chủ đề với bộ định vị tài nguyên thống nhất hoặc tên đường dẫn của tệp chủ đề ngôn ngữ đánh dấu siêu văn bản.|
|Xem thông tin|Thông tin mô tả các bộ điều hướng đang được sử dụng trong bộ trợ giúp. các bộ điều hướng chất lượng là: mục lục, chỉ mục và tìm kiếm toàn văn. các bộ điều hướng khác bao gồm các bộ điều hướng bóng và cả các bộ điều hướng yêu thích. dữ liệu liên quan đến bộ điều hướng tùy chỉnh được đính kèm thêm ở đây.|
<html>|Tiêu đề bộ trợ giúp|Các \<title> được phác thảo trong tệp trợ giúp (.hs). Tiêu đề này có vẻ ở trên cùng của hầu hết các cửa sổ và bất kỳ cửa sổ phụ nào được nêu trong tệp bộ trợ giúp của bạn.| </html>
|ID nhà|Tiêu đề của ID (mặc định) được hiển thị khi người theo dõi hỗ trợ được gọi mà không cho biết ID.|
|Bài thuyết trình|Các cửa sổ để hiển thị các chủ đề hỗ trợ. Đây là một phiên bản hiện đại của chương trình máy tính JavaHelp 2 được mô tả chi tiết hơn bên dưới \<presentation> .|
|Bộ trợ giúp phụ|Khu vực tùy chọn này kết hợp tĩnh các bộ trợ giúp khác bằng cách sử dụng thẻ. Các bộ trợ giúp được hiển thị bởi thẻ này được kết hợp một cách tự nhiên vào bộ trợ giúp có chứa thẻ. Bạn có thể tìm thấy nhiều điểm thú vị hơn xung quanh việc trộn trong Bộ trợ giúp trộn.|
|Implementation|Phân đoạn tùy ý này tạo sổ đăng ký cung cấp ánh xạ thông tin chính để mô tả lớp HelpBroker để sử dụng trong phương thức HelpSet.createHelpBroker. Hơn nữa, cơ quan đăng ký quyết định trình xem nội dung thành ứng dụng khách cho một loại Mô phỏng nhất định.|

## Định dạng tệp Java HS

Các tệp Java HS ở định dạng tệp XML và dựa trên khuyến nghị được đề xuất về Ngôn ngữ đánh dấu mở rộng của World Wide Web Consortium (W3C) [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Điều này có nghĩa là tệp Java HS ở định dạng tệp XML mà con người có thể đọc được và có thể mở được trong bất kỳ ứng dụng đọc XML nào.

### Ví dụ về định dạng tệp Java HS

Sau đây là một ví dụ về tệp bộ trợ giúp từ [Tài liệu bộ trợ giúp của Oracle](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## Người giới thiệu
* [Tệp bộ trợ giúp Oracle Java](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Định dạng tệp tập lệnh Haskell

## Tệp HS là gì?

Tệp có phần mở rộng .hs là tệp Haskell Script được viết bằng [Haskell](https://wiki.haskell.org/Haskell), một ngôn ngữ lập trình mã nguồn mở hoàn toàn có chức năng nâng cao. Mã được viết trong tệp HS hoàn toàn dựa trên các chức năng, không giống như [C](/vi/programming/c/), [C++](/vi/programming/cpp/) và tương tự, tuân theo các nguyên tắc phát triển nhanh phần mềm mạnh mẽ và ngắn gọn. Haskell cung cấp tính đồng thời và tính song song tích hợp sẵn cùng với các API, trình lược tả và trình gỡ lỗi phong phú để tạo ra các ứng dụng linh hoạt và chất lượng cao.

## Định dạng tệp HS

Giống như bất kỳ ngôn ngữ lập trình nào, các tệp HS được viết ở định dạng văn bản thuần túy mà con người có thể đọc được. Chúng có thể được tạo, chỉnh sửa và xem bằng bất kỳ công cụ văn bản có sẵn nào. Tệp mã nguồn .hs được biên dịch bằng trình biên dịch Haskell, tạo tệp nhị phân thực thi.

### Ví dụ định dạng tệp HS

Mã có thể được viết trong tệp .hs và được biên dịch bằng trình biên dịch Haskell, chẳng hạn như [GHC](https://haskell.org/ghc). Dòng mã sau đây được lưu dưới dạng `HelloWorld.hs` như được hiển thị trong mẫu sau.

```
main = putStrLn "Hello, World!"
```

Điều này được biên dịch bằng lệnh:

```
$ ghc -o hello hello.hs
```
và tệp thực thi kết quả có thể được chạy dưới dạng:

```
$ ./hello
```
Điều này in "Xin chào, Thế giới!" tuyên bố cho đầu ra.

## Người giới thiệu

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell trong 5 bước đơn giản](https://wiki.haskell.org/Haskell_in_5_steps)

