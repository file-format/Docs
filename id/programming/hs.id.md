{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Format File Skrip Haskell",
  "description":"Pelajari tentang apa itu format file HS dan API yang dapat membuat dan membuka file HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Format File HelpSet Java

## Apa itu file Java HS?

File dengan ekstensi .hs dalam bahasa pemrograman Java adalah file dokumentasi bantuan yang digunakan oleh sistem JavaHelp saat diaktifkan oleh suatu aplikasi. Ini mendefinisikan helpset untuk aplikasi tertentu yang diinstal dan terdiri dari beberapa subset sebagai bagian dari bantuan sistem untuk aplikasi tersebut. Program Java harus dapat menemukan file helpset yang namanya diakhiri dengan ekstensi .hs.

## Informasi Bantuan Java

File .hs mungkin berisi informasi berikut.

|Informasi|Deskripsi|
---|---|
|File Peta|File peta digunakan untuk mengasosiasikan ID topik dengan pencari sumber daya seragam atau nama path dari file topik bahasa mark-up hiperteks.|
|Lihat Informasi|Informasi yang menggambarkan navigator yang digunakan dalam helpset. navigator kualitas adalah: daftar isi, indeks, dan pencarian teks lengkap. navigator lebih lanjut termasuk gloss dan juga navigator favorit. data mengenai navigator khusus terlampir di sini lebih lanjut.|
<html>|Judul Bantuan|\<title> diuraikan dalam file helpset (.hs). Judul ini muncul di jendela paling atas dan jendela sekunder mana pun yang diuraikan dalam file bantuan Anda.| </html>
|Home ID|Judul ID (default) yang ditampilkan saat pengawas bantuan dipanggil tanpa menunjukkan ID.|
|Presentasi|Jendela untuk menampilkan mata pelajaran bantuan. Ini adalah versi modern dari program komputer JavaHelp 2 yang digambarkan lebih detail di bawah \<presentation> .|
|Sub-helpsets|Area diskresioner ini menggabungkan helpet lain secara statis dengan menggunakan tag. Kumpulan bantuan yang ditampilkan oleh tag ini digabungkan secara alami ke dalam kumpulan bantuan yang berisi tag tersebut. Lebih banyak tempat menarik seputar pencampuran dapat ditemukan di Blending Helpets.|
|Implementasi|Segmen diskresioner ini membuat registri yang memberikan pemetaan informasi kunci untuk mencirikan kelas HelpBroker untuk digunakan dalam metode HelpSet.createHelpBroker. Registri juga menentukan penampil konten ke klien untuk jenis Emulasi tertentu.|

## Format File JavaHS

File Java HS dalam format file XML dan berdasarkan rekomendasi yang diajukan oleh World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Ini berarti file Java HS dalam format file XML yang dapat dibaca manusia yang dapat dibuka di aplikasi pembaca XML apa pun.

### Contoh Format File Java HS

Berikut adalah contoh file helpset dari [dokumentasi Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

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

## Referensi
* [File Bantuan Oracle Java](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Format File Skrip Haskell

## Apa itu file HS?

File dengan ekstensi .hs adalah file Skrip Haskell yang ditulis dalam [Haskell](https://wiki.haskell.org/Haskell), bahasa pemrograman open-source canggih yang berfungsi murni. Kode yang ditulis dalam file HS murni didasarkan pada fungsi, tidak seperti [C](/id/programming/c/), [C++](/id/programming/cpp/) dan sejenisnya, yang mengikuti prinsip perkembangan pesat perangkat lunak yang kuat dan ringkas. Haskell menyediakan konkurensi dan paralelisme bawaan bersama dengan API, profiler, dan debugger yang kaya untuk menghasilkan aplikasi yang fleksibel dan berkualitas tinggi.

## Format File HS

Seperti bahasa pemrograman lainnya, file HS ditulis dalam format teks biasa yang dapat dibaca manusia. Ini dapat dibuat, diedit, dan dilihat dengan alat teks apa pun yang tersedia. File kode sumber .hs dikompilasi dengan kompiler Haskell, menghasilkan file biner yang dapat dieksekusi.

### Contoh Format File HS

Kode dapat ditulis dalam file .hs dan dikompilasi menggunakan kompiler Haskell seperti [GHC](https://haskell.org/ghc). Baris kode berikut disimpan sebagai `HelloWorld.hs` seperti yang ditunjukkan pada contoh berikut.

```
main = putStrLn "Hello, World!"
```

Ini dikompilasi menggunakan perintah:

```
$ ghc -o hello hello.hs
```
dan file yang dapat dieksekusi yang dihasilkan dapat dijalankan sebagai:

```
$ ./hello
```
Ini mencetak "Halo, Dunia!" pernyataan ke output.

## Referensi

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell Dalam 5 Langkah Mudah](https://wiki.haskell.org/Haskell_in_5_steps)

