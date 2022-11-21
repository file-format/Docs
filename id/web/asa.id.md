{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "format file", "tipe file", "apa itu file .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - File Konfigurasi ASP",
  "description" :"Pelajari tentang apa itu file ASA dan API yang dapat membuat dan membuka file ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## Apa itu file ASA?

File ASA adalah file konfigurasi, dibuat untuk proyek [ASP](/id/web/asp/)/ASP.NET. Ini berisi deklarasi variabel, berisi dan fungsi yang dimaksudkan untuk dapat diakses di tingkat Global dalam aplikasi. Semua halaman dalam proyek dapat mengakses variabel dan fungsi ini, sehingga menghindari persyaratan untuk menulis ulang ini. Salah satu contohnya adalah halaman Global.asa yang disimpan di direktori root agar dapat diakses oleh halaman website ASP lainnya. File Global.asa bersifat opsional, tetapi jika digunakan, setiap aplikasi hanya dapat memiliki satu file Global.asa.

## Format File ASA - Informasi Lebih Lanjut

File ASA adalah file teks biasa dengan informasi berikut.

* Acara aplikasi
* Acara sesi
* \<object> deklarasi
* Deklarasi TypeLibrary
* direktif #include

## Contoh File ASA

File Global.asa dapat terlihat seperti ini.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Referensi

* [ASP Global.asa file - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

