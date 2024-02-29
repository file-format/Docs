{
  "date": "2023-06-08",
  "keywords": [
"فایل vmx",
"فایل vmx چیست",
"نمونه فایل vmx",
"نحوه باز کردن فایل vmx",
"فایل vmx شامل چه چیزی است",
"فرمت فایل vmx چیست",
"فایل",
"پسوند فایل vmx",
"افزونه"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "فرمت فایل VMX - فایل پیکربندی ماشین مجازی VMware",
  "description": "با فرمت VMX و API هایی که می توانند فایل های VMX ایجاد و باز کنند آشنا شوید.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx-fa",
      "parent": "settings"
}
},
  "lastmod": "2023-06-08"
}

## فایل VMX چیست؟

فایل VMX که به عنوان فایل پیکربندی ماشین مجازی نیز شناخته می شود، یک فایل متنی ساده است که توسط نرم افزار مجازی سازی VMware برای تعریف تنظیمات و پیکربندی ماشین مجازی (VM) استفاده می شود. فایل‌های VMX حاوی اطلاعاتی مانند پیکربندی سخت‌افزار VM، نگاشت‌های دیسک مجازی، تنظیمات شبکه و سایر پارامترها هستند.

## نمونه فایل VMX

در اینجا نمونه ای از شکل ظاهری فایل VMX آورده شده است:

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

## فایل VMX شامل چه چیزی است؟

یک فایل VMX شامل تنظیمات پیکربندی مختلف برای ماشین مجازی (VM) است. در اینجا برخی از تنظیمات رایج در فایل VMX وجود دارد:

- `.encoding:` رمزگذاری کاراکتر مورد استفاده در فایل را مشخص می کند.
- `config.version:` نسخه فرمت فایل VMX را نشان می دهد.
- `virtualHW.version:` نسخه سخت افزار مجازی VM را مشخص می کند.
- `guestOS:` سیستم عامل مهمان نصب شده در VM را مشخص می کند.
- `memSize:` مقدار حافظه اختصاص داده شده به ماشین مجازی را مشخص می کند.
- `displayName:` نام یا برچسب نمایشی ماشین مجازی را تنظیم می کند.
- `PowerType:` رفتار برق را برای عملیات های مختلف (خاموش کردن، روشن کردن، تنظیم مجدد، تعلیق) تعریف می کند.
- 'floppyX:' تنظیمات پیکربندی مربوط به درایوهای فلاپی، مانند نگاشت حضور و فایل.
- `numvcpus:` تعداد CPUهای مجازی اختصاص داده شده به VM را مشخص می کند.
- `scsiX:` تنظیمات پیکربندی برای کنترلرهای SCSI و دیسک های مجازی مرتبط با آنها.
- `ethernetX:` تنظیمات پیکربندی آداپتورهای شبکه، از جمله نوع دستگاه مجازی، نام شبکه و نوع آدرس.
- `ideX:` تنظیمات پیکربندی برای کنترلرهای IDE و دیسک های مجازی مرتبط با آنها.
- «usbX:» تنظیمات پیکربندی دستگاه‌های USB، مانند جزئیات حضور و اتصال.
- `صدا:` تنظیمات پیکربندی آداپتور صدای مجازی.
- `tools.syncTime:` نشان می دهد که آیا همگام سازی زمان با سیستم میزبان فعال است یا خیر.
- `uuid.bios:` BIOS UUID VM را مشخص می کند.
- `uuid.location:` محل UUID VM را مشخص می کند.

## چگونه فایل VMX را باز کنیم؟

باز کردن یک فایل VMX به صورت دستی توصیه نمی شود. هنگامی که یک ماشین مجازی را با استفاده از VMware Fusion اجرا می کنید، نرم افزار به طور خودکار اطلاعات فایل VMX را بارگیری می کند.

با این حال، اگر می خواهید فایل VMX را به صورت دستی ویرایش کنید، می توانید این کار را با استفاده از هر ویرایشگر متنی مانند Notepad (ویندوز) یا TextEdit (Mac) انجام دهید.

## فرمت فایل VMX چیست؟

فایل VMX یک فایل متنی ساده با فرمت خاص است. فرمت از ساختار جفت کلید-مقدار پیروی می کند که در آن هر خط گزینه پیکربندی جداگانه ای را نشان می دهد.

فرمت کلی فایل VMX به شرح زیر است:

```
key1 = value1
key2 = value2
key3 = value3
```

هر خط از کلید و علامت مساوی (=) و مقدار مربوطه تشکیل شده است. کلید یک تنظیمات پیکربندی خاص را نشان می دهد و مقدار نشان دهنده مقدار اختصاص داده شده به آن تنظیم است.

به عنوان مثال، memSize = 8192 در فایل VMX مشخص می کند که محدودیت حافظه ماشین مجازی 8192 مگابایت رم است.

فرمت فایل VMX همچنین ممکن است شامل نظراتی باشد که با علامت پوند (#) در ابتدای خط نشان داده شده است، که توسط نرم افزار VMware هنگام تجزیه فایل نادیده گرفته می شود. نظرات اغلب برای ارائه اطلاعات اضافی یا توضیحات برای تنظیمات خاص استفاده می شود.

## منابع
* [نمونه فایل VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)





