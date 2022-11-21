
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - File Kode Byte ActionScript",
  "description":"Pelajari tentang apa itu format file ABC dengan contoh dan API yang dapat membuat dan membuka file ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Apa itu file ABC?

File dengan ekstensi .abc adalah File Kode Byte ActionScript yang dibuat oleh kompiler Flash sebagai hasil kompilasi file skrip ActionScript. Kode byte yang terdapat dalam file ABC dijalankan oleh ActionScript Virtual Machine (AVM dan AVM2). Kode byte terdiri dari data konstan, instruksi dari set instruksi AVM2, dan berbagai jenis metadata. Saat file ABC dimuat ke AVM atau AVM2, file tersebut akan diverifikasi. Jika tidak sesuai dengan Ikhtisar AVM2, maka ditolak. File ABC dapat dibuka di Adobe Flash Player yang sudah lama dihentikan.

## Format File ABC - Informasi Lebih Lanjut

File ABC disimpan ke disk dalam format file biner yang dapat dibaca oleh mesin virtual AVM atau AVM2. Struktur file internalnya mewakili blok kode yang dapat dieksekusi dengan semua data konstan, deskriptor tipe, kode, dan metadata.

## Struktur File ABC

Struktur file ABC adalah seperti yang ditunjukkan di bawah ini.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Kolom File ABC

|Nama Bidang|Deskripsi|
---|---|
|minor_version, major_version|Nilai dari major_version dan minor_version adalah nomor versi mayor dan minor dari format File abc.|
|constant_pool|Constant_pool adalah struktur panjang variabel yang terdiri dari bilangan bulat, ganda, string, ruang nama, set ruang nama, dan multinama.|
|method_count, method|Nilai darimethod_count adalah jumlah entri dalam larik metode. Setiap entri dalam larik metode adalah struktur info_metode dengan panjang variabel.|
|metadata_count, metadata|Nilai dari metadata_count adalah jumlah entri dalam array metadata. Setiap entri metadata adalah struktur metadata_info yang memetakan nama ke sekumpulan nilai string. |
|class_count, instance, class|Nilai class_count adalah jumlah entri dalam instance dan array kelas. |
|script_count, script|Nilai dari script_count adalah jumlah entri dalam larik skrip. Setiap entri skrip adalah struktur script_info yang menentukan karakteristik satu skrip dalam file ini. |
|method_body_count, method_body|Nilai dari method_body_count adalah jumlah entri dalam array method_body. Setiap method_bodyentry terdiri dari struktur method_body_info panjang variabel yang berisi instruksi untuk masing-masing metode atau fungsi.|

## Referensi

* [ABC Kuat (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

