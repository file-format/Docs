{
  "date" : "2019-10-11",
  "keywords" :[ "tệp mpkg", "định dạng tệp mpkg", "tệp mpkg là gì", "tệp", "ví dụ mpkg", "phần mở rộng tệp mpkg","phần mở rộng", "định dạng" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Định dạng tệp MPKG - Tệp gói Meta",
  "description":"Tìm hiểu về định dạng tệp MPKG và các API có thể tạo và mở tệp MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## Tệp MPKG là gì?

Tệp có phần mở rộng .mpkg là tệp trình cài đặt lưu trữ, hầu hết được tìm thấy trên Hệ điều hành MacOS. Nó chứa tất cả các tệp cài đặt cần thiết của ứng dụng mà không cần giữ riêng các tệp liên quan. Một tệp MPKG có thể chứa các tệp gói [PKG](/vi/compression/pkg/) dưới dạng một trong các tệp cài đặt bên cạnh các tệp khác. Không thể mở các tệp MPKG bằng bất kỳ phần mềm chung nào và được thực thi tự động trên MacOS bằng Trình cài đặt của Apple.

## Định dạng tệp MPKG

Tệp MPKG chứa các loại tệp khác nhau được yêu cầu để cài đặt nhiều gói chứa trong đó. Điều này có thể được nhìn thấy từ hình ảnh bên dưới, đây là cấu trúc cây của tệp MPKG mẫu. Cấu trúc cây này được xuất bằng cách sử dụng lệnh `tree` trên thiết bị đầu cuối MacOS.

{{< figure src="../mpkg.png" alt="Định dạng tệp MPKG" >}}

Mô tả của các yếu tố khác nhau trong hình ảnh như sau.

`Thư mục gói` - lưu trữ danh sách các tệp pkg, tức là danh sách các Gói con
`Thư mục tài nguyên` - lưu trữ các tài nguyên được sử dụng bởi pkg, chẳng hạn như tài nguyên và hình ảnh được bản địa hóa, tài liệu Rtf, tài liệu pdf, v.v.
`Tệp Distribution.dist` - Một tài liệu xml chứa thông tin như các gói con sẽ được cài đặt và tập lệnh thời gian chạy

Tệp XML mẫu cho tệp MPKG có thể trông như sau tùy thuộc vào các gói phụ được liên kết.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/vi/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - là gói con sẽ được cài đặt. Nó là một thư mục của cấu trúc Gói ở định dạng pkg. Nó chứa một thư mục con Nội dung.

## Người giới thiệu

* [Gói phẳng OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [Trình quản lý gói C++ MPKG](https://github.com/puellavulnerata/mpkg)

