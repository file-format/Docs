{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Tệp MP - Tệp LaTeX MetaPost",
  "description":"Tìm hiểu về định dạng tệp MP và API có thể tạo và mở tệp MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Tập tin MP là gì?

Tệp MP là tệp hình ảnh vector được tạo bởi ngôn ngữ lập trình MetaPost để tạo ảnh. Hình ảnh vector được tạo bằng định dạng tệp MP được lưu dưới dạng tệp [EPS](/vi/page-description-language/eps/) (PostScript được đóng gói). Ngoài ra, MetaPost được phân phối cùng với các khung công tác TeX và Metafont và các tệp MP có thể được tạo từ bên trong các tệp TEX và LTX được các ứng dụng này sử dụng. Các tệp MP chứa các câu lệnh vẽ và bản vẽ thuật toán toán học để hiển thị tệp EPS đầu ra. Công cụ PDFTex có thể sử dụng EPS đã tạo để tạo tệp [PDF](/vi/pdf/) trực tiếp.

## Định dạng tệp MP

Các tệp MP được lưu vào đĩa dưới dạng tệp nhị phân và tạo đầu ra EPS khi xuất sang định dạng tệp hình ảnh vector đầu ra. Các bản vẽ được tạo bằng MetaPost được bao gồm ở dạng được định dạng bên trong các tài liệu kỹ thuật và ấn phẩm tạp chí được tạo bằng LaTex.

### Ví dụ về tệp MetaPost MP

Sau đây là một ví dụ, được tham khảo từ [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), có chứa một mũi tên và chữ "A" ngay phía trên giữa mũi tên.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Người giới thiệu ##

* [MetaPost của Wikipedia](https://vi.wikipedia.org/wiki/MetaPost)
* [Metapost mẫu latex của Wiki giáo dục Berkeley](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

