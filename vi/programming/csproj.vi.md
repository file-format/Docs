{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Tìm hiểu về định dạng tệp CSPROJ và API có thể tạo và mở tệp CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Tệp CSProj là gì?
Các tệp có phần mở rộng CSPROJ đại diện cho một tệp dự án C# chứa danh sách các tệp có trong một dự án cùng với các tham chiếu đến các cụm hệ thống. Khi một dự án mới được bắt đầu trong Microsoft VIiual Studio, bạn sẽ nhận được một tệp .csproj cùng với tệp giải pháp chính ([.sln](/vi/programming/sln/)). Nếu có nhiều hơn một tập hợp trong một dự án, thì cũng sẽ có số lượng tệp dự án bằng nhau trong đó tệp .sln liên kết tất cả chúng lại với nhau như một phần của dự án. Nội dung của tệp này xác định tất cả các yêu cầu bắt buộc để xây dựng dự án, chẳng hạn như nội dung cần đưa vào, yêu cầu nền tảng, thông tin phiên bản, cài đặt máy chủ web hoặc máy chủ cơ sở dữ liệu và các tác vụ phải được thực hiện. Nội dung của tệp dự án được sắp xếp ở định dạng tệp XML và có thể được mở trong bất kỳ trình soạn thảo văn bản nào để chỉnh sửa cũng như xem. Nó cũng cung cấp một cái nhìn hợp lý cho các tệp dự án để sắp xếp hợp lý.

## Định dạng tệp CSPROJ #

Các nhà phát triển có thể tự tạo các tệp dự án cũng như tôn trọng [Lược đồ XML MSBuild](https://msdn.microsoft.com/library/5dy88c2e.aspx). Cấu trúc mở và minh bạch của các tệp dự án cho phép các nhà phát triển ứng dụng áp đặt quyền kiểm soát tinh vi và chi tiết đối với cách các dự án được xây dựng và triển khai. Nội dung của một hồ sơ dự án như vậy có mối quan hệ rất rõ ràng với nhau. Hình dưới đây cho thấy các yếu tố chính và mối quan hệ giữa các yếu tố này đối với một tệp dự án như vậy.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Các phần sau xây dựng các thành phần định dạng tệp cho tệp dự án.

### Phần tử dự án ###

Phần tử [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) là phần tử gốc của mọi tệp dự án. Nó xác định lược đồ XML cho tệp dự án và có thể bao gồm các thuộc tính để chỉ định các điểm nhập cho quy trình xây dựng.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Thuộc tính và Điều kiện

Thuộc tính đại diện cho các thông tin cần thiết cần thiết để xây dựng một dự án. Các thuộc tính như vậy được xác định trong phần tử [Nhóm thuộc tính](https://msdn.microsoft.com/library/t4w159bs.aspx). Các thuộc tính này bao gồm các cặp khóa-giá trị trong đó tên phần tử thuộc tính xác định khóa thuộc tính và nội dung của phần tử xác định giá trị thuộc tính. Ví dụ: bạn có thể xác định các thuộc tính có tên ServerName và ConnectionString để lưu trữ tên máy chủ tĩnh và chuỗi kết nối.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Có thể xác định điều kiện thông qua phần tử để quy định tiêu chí đánh giá phần tử. Điều này được chỉ định bởi từ Điều kiện trong khi xác định thuộc tính như hình bên dưới:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Khi MSBuild xử lý định nghĩa thuộc tính này, trước tiên, nó sẽ kiểm tra xem giá trị thuộc tính **$(OutputRoot)** có khả dụng hay không. Nếu giá trị thuộc tính trống—nói cách khác, người dùng chưa cung cấp giá trị cho thuộc tính này—điều kiện ước tính là **true** và giá trị thuộc tính được đặt thành **..\Publish\Out.**

### Mặt hàng và Nhóm mặt hàng

Tệp dự án xác định các đầu vào cho quá trình xây dựng thực sự là các loại tệp khác nhau. Trong danh pháp MSBuild, các đầu vào này được đại diện bởi các phần tử Mục và được xác định trong một phần tử [Nhóm mục](https://msdn.microsoft.com/library/646dk05y.aspx). Cũng giống như phần tử **Property**, bạn có thể đặt tên cho phần tử **Item** theo cách bạn muốn. Tuy nhiên, bạn phải chỉ định thuộc tính **Bao gồm** để xác định tệp hoặc ký tự đại diện mà mục đó đại diện.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Mục tiêu và Nhiệm vụ

Phần tử [Tác vụ](https://msdn.microsoft.com/library/77f2hx1s.aspx) đại diện cho một lệnh (hoặc tác vụ) xây dựng riêng lẻ. MSBuild bao gồm vô số tác vụ được xác định trước. Ví dụ:

* Tác vụ **Sao chép** sao chép các tệp vào một vị trí mới.
* Tác vụ **Csc** gọi trình biên dịch Visual C#.
* Tác vụ **Vbc** gọi trình biên dịch Visual Basic.
* Tác vụ **Exec** chạy một chương trình cụ thể.
* Tác vụ **Thông báo** ghi thông báo tới bộ ghi nhật ký.

Các tác vụ phải luôn nằm trong phần tử [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Phần tử **Target** là một tập hợp gồm một hoặc nhiều tác vụ được thực hiện tuần tự và một tệp dự án có thể chứa nhiều mục tiêu.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Người giới thiệu

* [Hiểu tệp dự án - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/under hiểu-the-project- tập tin)

