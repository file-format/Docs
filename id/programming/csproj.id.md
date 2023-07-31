{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Pelajari tentang format file CSPROJ dan API yang dapat membuat dan membuka file CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Apa itu file CSProj?
File dengan ekstensi CSPROJ mewakili file proyek C# yang berisi daftar file yang disertakan dalam proyek beserta referensi ke rakitan sistem. Saat proyek baru dimulai di Microsoft VIiual Studio, Anda mendapatkan satu file .csproj bersama dengan file solusi utama ([.sln](/id/programming/sln/)). Jika ada lebih dari satu rakitan dalam sebuah proyek, akan ada jumlah file proyek yang sama juga di mana file .sln mengikat semuanya sebagai bagian dari proyek. Isi file ini menentukan semua persyaratan yang diperlukan untuk membangun proyek seperti konten yang akan disertakan, persyaratan platfrom, informasi versi, pengaturan server web atau server basis data, dan tugas yang harus dilakukan. Konten file proyek diatur dalam format file XML dan dapat dibuka di editor teks apa pun untuk diedit dan juga dilihat. Ini juga memberikan pandangan logis ke file proyek untuk pengaturan yang tepat.

## Format File CSPROJ #

Pengembang dapat membuat file proyek sendiri serta menghormati [Skema MSBuild XML](https://msdn.microsoft.com/library/5dy88c2e.aspx). Struktur file proyek yang terbuka dan transparan memungkinkan pengembang aplikasi memaksakan kontrol yang canggih dan halus atas bagaimana proyek dibangun dan disebarkan. Isi file proyek semacam itu memiliki hubungan yang sangat jelas satu sama lain. Gambar berikut menunjukkan elemen kunci dan hubungan antara elemen tersebut untuk file proyek tersebut.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Bagian berikut menguraikan elemen format file untuk file proyek.

### Elemen Proyek ###

Elemen [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) adalah elemen akar dari setiap file proyek. Ini mengidentifikasi skema XML untuk file proyek dan dapat menyertakan atribut untuk menentukan titik masuk untuk proses pembangunan.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Properti dan Ketentuan

Properti mewakili informasi yang diperlukan yang diperlukan untuk membangun sebuah proyek. Properti tersebut ditentukan dalam elemen [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Properti ini terdiri dari pasangan kunci-nilai di mana nama elemen properti menentukan kunci properti dan konten elemen menentukan nilai properti. Misalnya, Anda dapat menentukan properti bernama ServerName dan ConnectionString untuk menyimpan nama server statis dan string koneksi.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Kondisi dapat ditentukan melalui elemen untuk menentukan kriteria untuk mengevaluasi elemen. Ini ditentukan oleh kata Kondisi saat mendefinisikan properti seperti yang ditunjukkan di bawah ini:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Saat MSBuild memproses definisi properti ini, pertama-tama MSBuild akan memeriksa apakah nilai properti **$(OutputRoot)** tersedia. Jika nilai properti kosong—dengan kata lain, pengguna belum memberikan nilai untuk properti ini—kondisi dievaluasi ke **true** dan nilai properti disetel ke **..\Publish\Out.**

### Item dan Grup Item

File proyek menentukan input ke proses pembangunan yang sebenarnya merupakan tipe file yang berbeda. Dalam nomenklatur MSBuild, input ini diwakili oleh elemen Item dan ditentukan dalam elemen [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Sama seperti elemen **Properti**, Anda dapat menamai elemen **Item** sesuka Anda. Namun, Anda harus menentukan atribut **Sertakan** untuk mengidentifikasi file atau karakter pengganti yang diwakili item tersebut.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Target dan Tugas

Elemen [Tugas](https://msdn.microsoft.com/library/77f2hx1s.aspx) mewakili instruksi build individual (atau tugas). MSBuild menyertakan banyak tugas yang telah ditentukan sebelumnya. Sebagai contoh:

* Tugas **Salin** menyalin file ke lokasi baru.
* Tugas **Csc** memanggil kompiler Visual C#.
* Tugas **Vbc** memanggil kompiler Visual Basic.
* Tugas **Exec** menjalankan program tertentu.
* Tugas **Message** menulis pesan ke logger.

Tugas harus selalu berada di dalam elemen [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Elemen **Target** adalah sekumpulan satu atau beberapa tugas yang dijalankan secara berurutan, dan file proyek dapat berisi beberapa target.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referensi

* [Memahami File Proyek - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- mengajukan)

