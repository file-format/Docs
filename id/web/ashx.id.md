{
  "date" : "2019-10-11",
  "keywords" :[ "ashx", "file", "extension", "file format", "ASHX", "ASP.NET Web Handler File" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Ekstensi File ASHX - File Handler Web ASP.NET",
  "description" :"Pelajari tentang apa itu file ASHX dan API yang dapat membuat dan membuka file ASHX.",
  "linktitle" : "ASHX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## Apa itu file ASHX?

File ASHX adalah halaman web yang digunakan oleh ASP.NET HTTP Handler untuk melayani pengguna dengan halaman yang direferensikan di dalam file ini. ASP.NET HTTP Handler memproses permintaan yang masuk, mereferensikan halaman dari file .ashx, dan mengirimkan kembali halaman yang telah dikompilasi ke browser pengguna. Metode pemrosesan sebagian besar mirip dengan file ASPX dengan perbedaan bahwa dalam hal ini, halaman/dokumen yang direferensikan diproses dan dikirim kembali.

## Format File ASHX

File .ashx disimpan dalam format file teks biasa dan berisi referensi ke halaman atau dokumen lain yang dikirim kembali ke browser pengguna berdasarkan permintaan. Ini dapat dibuka di editor teks dan IDE pengembang apa pun seperti Xamarin Studio, Microsoft Notepad, Notepad ++, dan banyak lagi. File ASHX berguna jika Anda memiliki:
* File biner
* Tampilan gambar dinamis
* Halaman web yang kritis terhadap kinerja
* File XML
* Minimal halaman web

## Bagaimana cara mengkompilasi file ASHX secara dinamis?

Langkah-langkah berikut dapat digunakan untuk menambah dan mengkompilasi file ASHX menggunakan Microsoft Visual Studio.

* tambahkan penangan Generik - Handler1.ashx di studio visual
* hapus file cs yang dibuat secara otomatis.
*buka ashx lagi,
** hapus CodeBehind="Handler1.ashx.cs"
** tambahkan kode c# di bawah ini

```c++
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web;

public class Handler1 : IHttpHandler
{
    public void ProcessRequest(HttpContext context)
    {
        context.Response.ContentType = "text/plain";
        context.Response.Write("Hello World2");
}

    public bool IsReusable
    {
        get
        {
            return false;
    }
}
}
```
### Contoh ASHX

Kode ASHX berikut mengembalikan file gambar ke permintaan pengguna saat file ASHX dipanggil di browser internet.


```C++
<%@ WebHandler Language="C#" Class="QueryStringHandler" %>  


using System;  

using System.Web;  


public class QueryStringHandler : IHttpHandler   

{  

    public void ProcessRequest (HttpContext context)   

    {  

        HttpResponse r = context.Response;  

        r.ContentType = "image/png";  

        string file = context.Request.QueryString["file"];  

        if (file == "Arrow")  

        {  

            r.WriteFile("Arrow.gif");  

        }  

        else  

        {  

            r.WriteFile("Image.gif");  

        }  

    }  


    public bool IsReusable   

    {  

        get  

        {  

            return false;  

        }  

    }  

}  

```

## Referensi

* [Kompilasi File ASHX](https://stackoverflow.com/questions/25510189/how-to-dynamically-compile-a-ashx-file)
 


