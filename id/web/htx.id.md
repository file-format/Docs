{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Berkas HTX - Format Berkas Ekstensi HTML",
  "description" :"Panduan format file Anda untuk mempelajari apa itu file HTX dan API yang dapat membuat dan membuka file HTX.",
  "linktitle" : "HTX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file HTX?

File HTX sebenarnya adalah file HTML yang berisi variabel data untuk menampilkan hasil kueri database sebagai halaman web. Sebagian besar dibuat dengan perangkat lunak pengembangan Web Microsoft FrontPage, file HTX disimpan untuk disimpan di folder yang sama dengan file Internet Database Connector (.IDC) yang sesuai.

File HTX dapat dibuka dengan aplikasi seperti Microsoft FrontPage dan editor teks apapun seperti Notepad, TextEdit, atau Atom.

## Format File HTX

File HTX disimpan sebagai file teks biasa dengan kode untuk mengambil data dari database dan menyimpan variabel untuk ditampilkan.


### Contoh Berkas HTX

Contoh file HTX adalah sebagai berikut yang menentukan header halaman untuk menampilkan batasan kueri dan dokumen yang ditampilkan pada halaman untuk ditampilkan kepada pengguna.

```
<H4>
<%if CiMatchedRecordCount eq 0%>
No documents matched the query "<%EscapeHTMLCiRestriction%>".</H4>
<%else%>
<H4>Documents <%CiFirstRecordNumber%> to <%CiLastRecordNumber%> of
<%if CiMatchedRecordCount eq CiMaxRecordsInResultSet%>
the first
<%endif%>
<%CiMatchedRecordCount%> matching the query
"<%EscapeHTMLCiRestriction%>".
<%endif%>
</H4>
```

Keluaran dari contoh kode ini adalah sebagai berikut.

```
Documents 1 to 10 of the first 150 matching the query "cache".
```

Seperti dapat dilihat, file HTX adalah template yang memformat bagaimana hasilnya dikembalikan dan ditampilkan kepada pengguna akhir. Itu ditulis dalam format HTML dengan beberapa ekstensi IIS dan Layanan Pengindeksan. Ekstensi ini menyertakan nama variabel dan kode lain untuk memproses hasil.

## Referensi

* [Memformat Hasil dalam File .Htx](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/indexsrv/formatting-the-results--htx-file-)

