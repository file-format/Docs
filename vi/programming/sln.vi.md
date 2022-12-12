{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"Tìm hiểu về định dạng tệp SLN và các API có thể tạo và mở tệp SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## Tập tin SLN là gì?
Tệp có phần mở rộng .SLN đại diện cho tệp **Giải pháp Visual Studio** lưu thông tin về tổ chức dự án trong tệp giải pháp. Nội dung của tệp giải pháp như vậy được viết bằng văn bản thuần túy bên trong tệp và có thể được quan sát/chỉnh sửa bằng cách mở tệp trong bất kỳ trình soạn thảo văn bản nào. Thông tin chứa trong tệp giải pháp vẫn tồn tại lâu dài và được sử dụng để tải thông tin liên quan đến giải pháp, chẳng hạn như [dự án ](/vi/programming/csproj/) và bất kỳ thông tin bắt buộc nào khác. Các tệp dự án được tham chiếu bởi tệp giải pháp chứa thông tin bổ sung để kích hoạt môi trường để phổ biến cấu trúc phân cấp với các mục của dự án đó. Không có dữ liệu nào được lưu trữ trong tệp .sln, mặc dù thông tin dự án có thể được ghi vào tệp .sln nếu cần.

## **Lịch sử Phiên bản SLN** ##

Phiên bản định dạng giải pháp đã phát triển cùng với từng giải pháp Microsoft Visual Studio theo thời gian. Các chi tiết về những điều này như sau.


|Phiên bản Visual Studio|Phiên bản Định dạng Giải pháp
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Nội dung của tệp giải pháp** ###

Một tệp giải pháp bao gồm một số phần được môi trường đọc để tải dự án. Nội dung tệp .sln mẫu như bên dưới.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Tuyên bố dự án** ###

Một tệp giải pháp có thể chứa nhiều hơn một khai báo dự án và đó cũng là các loại dự án khác nhau. Ví dụ: một tệp giải pháp duy nhất có thể chứa CSharp cũng như dự án VB.NET. Các loại này được phân biệt trong một giải pháp sử dụng [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Tuyên bố dự án trên có thể được khái quát như sau để hiểu rõ ràng.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID là duy nhất cho các loại dự án khác nhau và được trình đọc giải pháp sử dụng để xác định loại dự án. Trong trường hợp này, F184B08F-C81C-45F6-A57F-5ABD9991F28F cho thấy đây là một dự án VB.NET.

`GUID dự án:` GUID duy nhất của dự án giúp phân biệt nó với các dự án khác trong giải pháp. ID duy nhất của một dự án trong giải pháp giúp các dự án khác trong giải pháp có thể truy cập vào nó.

Dựa trên thông tin có trong phần dự án của tệp .sln, môi trường sẽ tải từng tệp dự án. Bản thân dự án sau đó chịu trách nhiệm điền vào hệ thống phân cấp dự án và tải bất kỳ dự án lồng nhau nào. Mọi thay đổi đối với giải pháp đều được lưu trở lại tệp giải pháp khi lưu hoặc đóng dự án.

## Giải pháp Visual Studio VS dự án

**Dự án:** Theo logic, khi bạn bắt đầu tạo một ứng dụng hoặc phần mềm bằng cách sử dụng Visual Studio, bạn sẽ bắt đầu một dự án mới. Một dự án chứa tất cả các tệp cần thiết như mã nguồn, biểu tượng, hình ảnh, tệp dữ liệu, v.v. sẽ được biên dịch thành một ứng dụng, trang web hoặc thư viện có thể thực thi được.

**Giải pháp:** Một giải pháp chứa một hoặc nhiều dự án. Vì vậy, giải pháp giống như một thùng chứa cho các dự án Visual Studio. Theo logic, chúng ta có thể nói ai đó muốn có một giải pháp hoàn chỉnh cho doanh nghiệp của mình bao gồm trang web, ứng dụng dành cho máy tính để bàn, dịch vụ nghỉ ngơi và ứng dụng dành cho thiết bị di động.

### **Người giới thiệu** ###

* [Tệp giải pháp - Bởi MSDN](https://docs.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [GUID loại dự án](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

