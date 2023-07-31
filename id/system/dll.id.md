{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "ekstensi", "file", "format", "sistem", "Perpustakaan Tautan Dinamis", "pengaturan", "program", "komputer", "aplikasi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Perpustakaan Tautan Dinamis",
  "description":"Pelajari tentang format file DLL dan API yang dapat membuat dan membuka file DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Apa itu file DLL? ##

File DLL atau Dynamic Link Library adalah jenis file yang dapat dieksekusi. Ini adalah salah satu file ekstensi yang paling sering ditemukan di perangkat Anda dan biasanya disimpan di folder System32 di Windows Anda. File ekstensi DLL dikembangkan oleh Microsoft dan populer digunakan oleh mereka. Ini memiliki peringkat pengguna popularitas tinggi. DLL berfungsi sebagai rak yang berisi *driver/prosedur/fungsi/properti* yang dirancang dan diterapkan untuk program/aplikasi oleh server windows. Satu file DLL juga dapat dibagikan di antara berbagai program windows. File ekstensi ini sangat penting untuk kelancaran program Windows di perangkat Anda karena mereka bertanggung jawab untuk mengaktifkan dan menjalankan berbagai fungsi pada program seperti menulis dan membaca file, menghubungkan dengan perangkat lain yang berada di luar pengaturan Anda.
Namun File-file ini hanya dapat dibuka pada perangkat yang mendukung versi Windows apa pun (windows 7/windows 10/dll.) dan karenanya tidak dapat dibuka langsung pada perangkat yang mendukung Mac OS. (Jika Anda ingin membuka file DLL di Mac OS, berbagai aplikasi eksternal dapat membantu membukanya.)


## Format Berkas DLL ##

File DLL dikembangkan oleh Microsoft dan memiliki ekstensi ".dll" yang mewakili jenisnya. Itu telah menjadi bagian integral dari server Windows 1.0, dan seterusnya. Ini adalah jenis file biner dan didukung oleh semua versi Microsoft Windows. Jenis file ini dibuat sebagai sarana untuk membuat sistem pustaka bersama dalam program Windows, untuk memungkinkan pengeditan atau perubahan terpisah dan independen dalam pustaka program tanpa perlu menautkan ulang program.


## Contoh DLL ##

Kode contoh untuk titik masuk DLL dapat ditemukan di bawah:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Referensi ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
