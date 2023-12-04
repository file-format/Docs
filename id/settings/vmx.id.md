{
"tanggal": "08-06-2023",
  "keywords": [
"file vmx",
"apa itu file vmx",
"contoh file vmx",
"cara membuka file vmx",
"apa isi file vmx",
"apa format file vmx",
"mengajukan",
"ekstensi file vmx",
"perpanjangan"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Format File VMX - File Konfigurasi Mesin Virtual VMware",
  "description":"Pelajari tentang format VMX dan API yang dapat membuat dan membuka file VMX.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent" : "settings"
}
},
"mod terakhir": "08-06-2023"
}

## Apa itu file VMX?

File VMX, juga dikenal sebagai file konfigurasi mesin virtual, adalah file teks biasa yang digunakan oleh perangkat lunak virtualisasi VMware untuk menentukan pengaturan dan konfigurasi mesin virtual (VM). File VMX berisi informasi seperti konfigurasi perangkat keras VM, pemetaan disk virtual, pengaturan jaringan, dan parameter lainnya.

## Contoh File VMX

Berikut adalah contoh tampilan file VMX:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## Apa isi file VMX?

File VMX berisi berbagai pengaturan konfigurasi untuk mesin virtual (VM). Berikut beberapa pengaturan yang umum ditemukan pada file VMX:

- `.encoding:` Menentukan pengkodean karakter yang digunakan dalam file.
- `config.version:` Menunjukkan versi format file VMX.
- `virtualHW.version:` Menentukan versi perangkat keras virtual untuk VM.
- `guestOS:` Menentukan sistem operasi tamu yang diinstal di VM.
- `memSize:` Menentukan jumlah memori yang dialokasikan untuk VM.
- `displayName:` Menyetel nama tampilan atau label untuk VM.
- `powerType:` Mendefinisikan perilaku daya untuk operasi yang berbeda (mematikan, menghidupkan, mengatur ulang, menangguhkan).
- `floppyX:` Pengaturan konfigurasi yang terkait dengan floppy drive, seperti pemetaan keberadaan dan file.
- `numvcpus:` Menentukan jumlah CPU virtual yang ditetapkan ke VM.
- `scsiX:` Pengaturan konfigurasi untuk pengontrol SCSI dan disk virtual terkait.
- `ethernetX:` Pengaturan konfigurasi untuk adaptor jaringan, termasuk jenis perangkat virtual, nama jaringan, dan jenis alamat.
- `ideX:` Pengaturan konfigurasi untuk pengontrol IDE dan disk virtual terkait.
- `usbX:` Pengaturan konfigurasi untuk perangkat USB, seperti kehadiran dan detail koneksi.
- `suara:` Pengaturan konfigurasi untuk adaptor suara virtual.
- `tools.syncTime:` Menunjukkan apakah sinkronisasi waktu dengan sistem host diaktifkan.
- `uuid.bios:` Menentukan UUID BIOS VM.
- `uuid.location:` Menentukan lokasi UUID VM.

## Bagaimana cara membuka file VMX?

Membuka file VMX secara manual tidak disarankan. Saat Anda menjalankan mesin virtual menggunakan VMware Fusion, perangkat lunak secara otomatis memuat informasi dari file VMX.

Namun, jika Anda ingin mengedit file VMX secara manual, Anda dapat melakukannya menggunakan editor teks apa pun misalnya Notepad (Windows) atau TextEdit (Mac).

## Apa format file VMX?

File VMX adalah file teks biasa dengan format tertentu. Formatnya mengikuti struktur pasangan nilai kunci di mana setiap baris mewakili opsi konfigurasi terpisah.

Format umum file VMX adalah sebagai berikut:

```
key1 = value1
key2 = value2
key3 = value3
```

Setiap baris terdiri dari kunci diikuti dengan tanda sama dengan (=) dan nilai yang sesuai. Kuncinya mewakili pengaturan konfigurasi tertentu dan nilainya mewakili nilai yang ditetapkan ke pengaturan itu.

Misalnya, `memSize = "8192"` dalam file VMX menetapkan bahwa batas memori Mesin Virtual adalah RAM 8192MB.

Format file VMX juga dapat menyertakan komentar, dilambangkan dengan tanda pagar (#) di awal baris, yang diabaikan oleh perangkat lunak VMware saat menguraikan file. Komentar sering kali digunakan untuk memberikan informasi tambahan atau penjelasan untuk pengaturan tertentu.

## Referensi
* [Contoh File VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




