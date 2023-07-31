{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "uzantı", "dosya", "format", "sistem", "MemoryDump", "Minidump", "programlar", "bilgisayar", "uygulama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump Dosya Biçimi",
  "description":"DMP dosya formatı ve DMP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## DMP dosyası nedir? ##

DMP dosyası öncelikle MemoryDump veya Minidump dosya biçimiyle ilişkilendirilir. Microsoft Windows işletim sisteminde, bilgisayarın bellek alanından dökülen verileri depolamak için kullanılır. DMP dosyaları genellikle bir dosya çöktüğünde veya bir hata oluştuğunda oluşturulur. Bazen DMP dosyaları, teknik uzmanlar veya ileri düzey bilgisayar kullanıcıları için karşılaştığınız sorunları gidermek ve her türlü uygulama sorununu çözmek için çok önemlidir. DMP dosyaları, işletim sistemi tarafından sistemde yüklü herhangi bir uygulamada hata ayıklamak için kullanılan Microsoft'ta tescilli bir format olarak saklanır.


## DMP Dosya Formatının Teknik Şartnamesi

Windows'ta "savedump.exe" sistem aracı, daha sonra mevcut çeşitli hata ayıklama yardımcı programları tarafından işlenebilen .dmp dosyaları oluşturur. Mini döküm (64/128 Kb), pencereler tarafından '%SystemRoot%\Minidump' dizininde saklanır. Öte yandan, çekirdek belleği ve tam bellek dökümleri sistem kökünde 'Memory.dmp' dosyaları olarak depolanır. Bellek dökümü dosyaları nispeten büyük dosyalardır, dolayısıyla yeterli miktarda depolama alanı kaplayabilir. Bu nedenle, sorun gidermede işinize yaramayacağını düşündüğünüz gereksiz .dmp dosyalarının silinmesi önerilir.

.dmp dosyalarını manuel olarak veya bilgisayarınızdaki varsayılan "diski temizleme sihirbazını" kullanarak silebilirsiniz. DMP uzantıları, Oracle veritabanı ürünleri tarafından oluşturulan ve kullanılan yedekleme ve kurtarma veritabanı dosyalarındaki .dmp dosyalarını kullanmak için kullanılır. Oracle tarafından oluşturulan DMP dosyaları, bir veritabanı sunucusu aracılığıyla çalışan bir veritabanı örneğine içe aktarma veya geri yükleme için kullanılabilen veritabanı yedekleridir. Çoğu durumda, .dmp dosyalarının dosya adları olarak saat ve tarih damgaları vardır.

### DMP Dosyasının İçeriği

Bir bellek dökümü dosyası şunları içerir:

* Stop deyimi ve parametreleri;
* Yüklü sürücülerin listesi;
* Windows'un normal çalışmasını durduran işlemler için işlemci bağlamı (PRCB);
* Durdurulan işlemler için çekirdek bağlamı ve işlemci bilgileri (EPROCESSES);
* Durdurulan iş parçacığı için çekirdek bağlamı ve işlemci bilgisi (ETHREAD);
* İşlemin gerçekleştirilmesini sonlandıran iş parçacığı için çekirdek modu çağrı yığını.


## VYP Örneği

Durma hatası 0XC0000218 (Registry_File_Failure) aşağıdaki gibi bir DMP dosyası oluşturur:

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

## Referans ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

