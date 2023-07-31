{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "ekstensi", "file", "format", "sistem", "MemoryDump", "Minidump", "program", "komputer", "aplikasi" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Format Berkas MemoryDump",
  "description":"Pelajari tentang format file DMP dan API yang dapat membuat dan membuka file DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## Apa itu file DMP? ##

File DMP terutama terkait dengan format file MemoryDump atau Minidump. Ini digunakan dalam sistem operasi Microsoft Windows untuk menyimpan data yang telah dibuang dari ruang memori komputer. Biasanya, file DMP dibuat saat file mogok atau terjadi kesalahan. Terkadang file DMP sangat penting bagi pakar teknis atau pengguna komputer tingkat lanjut untuk memecahkan masalah yang Anda hadapi dan menyelesaikan masalah aplikasi apa pun. File DMP disimpan sebagai format berpemilik di Microsoft yang digunakan oleh sistem operasi untuk men-debug aplikasi apa pun yang diinstal pada sistem.


## Spesifikasi Teknis Format File DMP

Di Windows, alat sistem "savedump.exe" menghasilkan file .dmp yang kemudian dapat diproses oleh berbagai utilitas debug yang tersedia. Mini dump (64/128 Kb) disimpan oleh windows di direktori '%SystemRoot%\Minidump'. Di sisi lain, memori kernel dan dump memori penuh disimpan di root sistem sebagai file 'Memory.dmp'. File dump memori adalah file yang relatif besar, karenanya dapat memakan ruang penyimpanan yang cukup. Jadi disarankan agar file .dmp yang tidak berguna yang menurut Anda tidak akan berguna untuk memecahkan masalah kemudian hapus.

Anda dapat menghapus file .dmp baik secara manual atau dengan menggunakan "wizard disk bersih" default di komputer Anda. Ekstensi DMP digunakan oleh produk database Oracle untuk menggunakan file .dmp dalam file database cadangan dan pemulihan yang dibuat dan digunakan. File DMP yang dibuat oleh Oracle adalah cadangan database yang dapat digunakan untuk mengimpor atau memulihkan ke instance database yang sedang berjalan melalui server database. Dalam kebanyakan kasus, file .dmp memiliki stempel waktu dan tanggal sebagai nama filenya.

### Isi File DMP

File dump memori berisi:

* Pernyataan berhenti dan parameternya;
* Daftar driver yang dimuat;
* Konteks prosesor (PRCB) untuk proses yang menghentikan operasi normal Windows;
* Konteks kernel dan informasi prosesor (EPROCESSES) untuk proses yang telah dihentikan;
* Konteks kernel dan informasi prosesor (ETHREAD) untuk utas yang dihentikan;
* Tumpukan panggilan mode-kernel untuk utas yang mengakhiri proses dari kinerja.


## Contoh DMP

Stop error 0XC0000218 (Registry_File_Failure) membuat file DMP sebagai berikut:

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## Referensi ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

