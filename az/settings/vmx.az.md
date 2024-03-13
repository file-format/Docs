{
  "date": "2023-06-08",
  "keywords": [
"vmx faylı",
"vmx faylı nədir",
"vmx fayl nümunəsi",
"vmx faylını necə açmaq olar",
"vmx faylında nə var",
"vmx faylının formatı nədir",
"fayl",
"vmx fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "VMX Fayl Format - VMware Virtual Maşın Konfiqurasiya Faylı",
  "description": "VMX faylları yarada və aça bilən VMX formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx-az",
      "parent": "settings"
}
},
  "lastmod": "2023-06-08"
}

## VMX faylı nədir?

Virtual maşın konfiqurasiya faylı kimi də tanınan VMX faylı virtual maşının (VM) parametrlərini və konfiqurasiyasını müəyyən etmək üçün VMware virtuallaşdırma proqramı tərəfindən istifadə edilən düz mətn faylıdır. VMX faylları VM-nin aparat konfiqurasiyası, virtual disk xəritələri, şəbəkə parametrləri və digər parametrlər kimi məlumatları ehtiva edir.

## VMX fayl nümunəsi

VMX faylının necə görünə biləcəyinə dair bir nümunə:

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

## VMX faylında nə var?

VMX faylı virtual maşın (VM) üçün müxtəlif konfiqurasiya parametrlərini ehtiva edir. VMX faylında tez-tez tapılan bəzi parametrlər bunlardır:

- `.encoding:` Faylda istifadə olunan simvol kodlamasını təyin edir.
- `config.version:` VMX fayl formatının versiyasını göstərir.
- `virtualHW.version:` VM üçün virtual avadanlığın versiyasını müəyyən edir.
- `qonaqOS:` VM-də quraşdırılmış qonaq əməliyyat sistemini təyin edir.
- `memSize:` VM-ə ayrılmış yaddaşın miqdarını müəyyən edir.
- `displayName:` VM üçün ekran adını və ya etiketini təyin edir.
- `powerType:` Müxtəlif əməliyyatlar üçün güc davranışını müəyyən edir (güc kəsilməsi, yandırılması, sıfırlanması, dayandırılması).
- `floppyX:` Mövcudluq və fayl xəritələri kimi disketlərlə əlaqəli konfiqurasiya parametrləri.
- `numvcpus:` VM-ə təyin edilmiş virtual CPU-ların sayını təyin edir.
- `scsiX:` SCSI nəzarətçiləri və onlarla əlaqəli virtual disklər üçün konfiqurasiya parametrləri.
- `ethernetX:` Şəbəkə adapterləri üçün konfiqurasiya parametrləri, o cümlədən virtual cihaz növü, şəbəkə adı və ünvan növü.
- `ideX:` IDE nəzarətçiləri və onlarla əlaqəli virtual disklər üçün konfiqurasiya parametrləri.
- `usbX:` USB cihazları üçün mövcudluq və əlaqə detalları kimi konfiqurasiya parametrləri.
- `səs:` Virtual səs adapteri üçün konfiqurasiya parametrləri.
- `tools.syncTime:` Host sistemi ilə vaxt sinxronizasiyasının aktiv olub olmadığını göstərir.
- `uuid.bios:` VM-nin BIOS UUID-ni təyin edir.
- `uuid.location:` VM-nin UUID yerini müəyyən edir.

## VMX faylını necə açmaq olar?

VMX faylını əl ilə açmaq tövsiyə edilmir. VMware Fusion istifadə edərək virtual maşını işə saldığınız zaman proqram avtomatik olaraq VMX faylından məlumatları yükləyir.

Bununla belə, VMX faylını əl ilə redaktə etmək istəyirsinizsə, bunu istənilən mətn redaktoru, məsələn, Notepad (Windows) və ya TextEdit (Mac) istifadə edərək edə bilərsiniz.

## VMX faylının formatı nədir?

VMX faylı xüsusi formata malik düz mətn faylıdır. Format hər bir sətir ayrı-ayrı konfiqurasiya seçimini təmsil etdiyi açar-dəyər cütü strukturunu izləyir.

VMX faylının ümumi formatı aşağıdakı kimidir:

```
key1 = value1
key2 = value2
key3 = value3
```

Hər bir sətir açardan sonra bərabər işarə (=) və müvafiq dəyərdən ibarətdir. Açar xüsusi konfiqurasiya parametrini, dəyər isə həmin parametrə təyin edilmiş dəyəri təmsil edir.

Məsələn, VMX faylındakı `memSize = 8192` Virtual Maşın yaddaş limitinin 8192 MB RAM olduğunu göstərir.

VMX faylının formatına sətrin əvvəlində funt işarəsi (#) ilə işarələnən və faylı təhlil edərkən VMware proqramı tərəfindən nəzərə alınmayan şərhlər də ola bilər. Şərhlər çox vaxt xüsusi parametrlər üçün əlavə məlumat və ya izahat vermək üçün istifadə olunur.

## İstinadlar
* [Nümunə VMX Faylı](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)





