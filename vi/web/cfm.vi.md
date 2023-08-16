{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "extension", "file", "format", "system", "Cold Fusion Markup Language", "language", "CFM web pages", "CFML engine", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Đánh dấu kết hợp lạnh",
  "description":"Tìm hiểu về định dạng tệp CFM và API có thể tạo và mở tệp CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Tệp CFM là gì? ##

Các trang web và tệp được sử dụng trong **Ngôn ngữ đánh dấu kết hợp lạnh** chứa các phần mở rộng của CFM và được đặt tên là các trang web CFM. Ngôn ngữ kịch bản phát triển web này chạy trên Google App Engine, .NET framework và JVM. Nó có thể chứa ngôn ngữ lập trình hoặc mã của ngôn ngữ đó. Khi người dùng truy cập bất kỳ trang nào của nó, máy chủ web của ColdFusion sẽ thực thi nó. CFScript (gần với JavaScript) hoặc các thẻ có thể được sử dụng để viết CFML. CFML có thể được sử dụng để tạo các ngôn ngữ khác ngoài [HTML](/vi/web/html/) như [CSS](/vi/web/css/), [JavaScript](/vi/web/js/), [XML](/vi/web/ xml/), v.v.

Việc sử dụng ngôn ngữ này và các thẻ mà nó hỗ trợ chủ yếu là để phát triển các ứng dụng web động. Các tệp có thể được chạy trực tiếp trong trình duyệt trực tuyến nếu có bất kỳ lỗi nào xảy ra trong quá trình sử dụng ngoại tuyến nền tảng phát triển ứng dụng.
 

CFML hoạt động theo cách các phần mở rộng tệp máy chủ cụ thể (.cfc, .cfm) được cung cấp để xử lý cho công cụ CFML. Nếu các công cụ dựa trên Java, thì nó đạt được bằng cách sử dụng các máy chủ Java. Công cụ của CFML chỉ xử lý các chức năng và thẻ và nó trả về các chức năng và văn bản bên ngoài các thẻ CFML cho máy chủ web mà không có bất kỳ thay đổi nào.


## Lược Sử ##

Năm 1995, lần đầu tiên nó được tạo ra bởi một tập đoàn tên là Allaire. Vào năm 2005, Adobe đã mua lại nó và nó vẫn cung cấp các dịch vụ để phát triển ColdFusion cho đến tận bây giờ. Trong những năm qua, nó đã được phát triển và nâng cấp bởi nhiều người và công ty. Vào năm 2012, một nền tảng có tên OpenCFML đã được ra mắt. Sau đó, vào năm 2015, Railo trước đây đã cung cấp dịch vụ của mình để cải thiện hiệu suất của CFM và giảm tài nguyên để có chức năng tốt hơn. Bản cập nhật gần đây nhất của nó đã được ra mắt vào năm 2020, được thông báo sẽ tiếp tục cho đến năm 2028.

## Định dạng tệp CFM ##

Mã của các tệp CFM và trang web chủ yếu bao gồm các thẻ giống như HTML nhưng có một chút khác biệt. Các tệp này chịu trách nhiệm thực hiện các hoạt động khác nhau mà các tập lệnh ColdFusion cho phép chạy.
* Các tệp này có thể được truy cập và chạy trực tiếp trên cả Windows và macOS bằng trình duyệt của bất kỳ hệ điều hành nào.
* Adobe ColdFusion cung cấp nền tảng để phát triển các trang web và ứng dụng động trên PC.
* Bất kỳ trình soạn thảo văn bản nào như NotePad hoặc bất kỳ trình soạn thảo văn bản nào khác trong hệ điều hành đều có thể được sử dụng để mở các tệp này vì các tệp này dựa trên văn bản.
* Khi bất kỳ tệp CFM nào được mở trong trình soạn thảo văn bản, nó sẽ hiển thị mã bao gồm các thẻ và tập lệnh mà một người sẽ không hiểu trừ khi anh ta là nhà phát triển web.

## Ví dụ sử dụng CFM ##

Phần sau đây trình bày một ví dụ sử dụng đơn giản tệp CFM.

### Tài liệu CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Người giới thiệu ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

