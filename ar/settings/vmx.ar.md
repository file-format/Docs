{
"التاريخ": "08-06-2023",
  "keywords": [
"ملف vmx",
"ما هو ملف vmx",
"مثال لملف vmx",
"كيفية فتح ملف vmx",
"ماذا يحتوي ملف vmx",
"ما هو تنسيق ملف vmx",
"ملف",
"امتداد الملف vmx",
"امتداد"
],
  "author": {
"display_name": "شكيل فايز"
},
"draft": "false",
"toc": true,
"title": "تنسيق ملف VMX - ملف تكوين الجهاز الظاهري لبرنامج VMware",
  "description":"تعرف على تنسيق VMX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات VMX وفتحها.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent" : "settings"
}
},
"آخر مود": "08-06-2023"
}

## ما هو ملف VMX؟

ملف VMX, المعروف أيضًا باسم ملف تكوين الجهاز الظاهري, هو ملف نصي عادي يستخدمه برنامج المحاكاة الافتراضية VMware لتحديد إعدادات وتكوين الجهاز الظاهري (VM). تحتوي ملفات VMX على معلومات مثل تكوين أجهزة VM وتعيينات القرص الظاهري وإعدادات الشبكة والمعلمات الأخرى.

## مثال على ملف VMX

فيما يلي مثال لما قد يبدو عليه ملف VMX:

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

## ماذا يحتوي ملف VMX؟

يحتوي ملف VMX على إعدادات تكوين مختلفة للجهاز الظاهري (VM). فيما يلي بعض الإعدادات الشائعة في ملف VMX:

- `.encoding:` يحدد ترميز الأحرف المستخدم في الملف.
- `config.version:` يشير إلى إصدار تنسيق ملف VMX.
- `virtualHW.version:` يحدد إصدار الجهاز الظاهري للجهاز الافتراضي.
- `guestOS:` يحدد نظام التشغيل الضيف المثبت في الجهاز الافتراضي.
- `memSize:` يحدد مقدار الذاكرة المخصصة للجهاز الافتراضي.
- `displayName:` يضبط اسم العرض أو التسمية الخاصة بجهاز VM.
- `powerType:` يحدد سلوك الطاقة للعمليات المختلفة (إيقاف التشغيل, التشغيل, إعادة الضبط, التعليق).
- `floppyX:` إعدادات التكوين المتعلقة بمحركات الأقراص المرنة, مثل التواجد وتعيينات الملفات.
- `numvcpus:` يحدد عدد وحدات المعالجة المركزية الافتراضية المخصصة للجهاز الافتراضي.
- `scsiX:` إعدادات التكوين لوحدات تحكم SCSI والأقراص الافتراضية المرتبطة بها.
- `ethernetX:` إعدادات التكوين لمحولات الشبكة, بما في ذلك نوع الجهاز الظاهري واسم الشبكة ونوع العنوان.
- `ideX:` إعدادات التكوين لوحدات تحكم IDE والأقراص الافتراضية المرتبطة بها.
- `usbX:` إعدادات التكوين لأجهزة USB, مثل تفاصيل التواجد والاتصال.
- `الصوت:` إعدادات التكوين لمحول الصوت الافتراضي.
- `tools.syncTime:` يشير إلى ما إذا تم تمكين مزامنة الوقت مع النظام المضيف.
- `uuid.bios:` يحدد BIOS UUID الخاص بالجهاز الظاهري.
- `uuid.location:` يحدد موقع UUID الخاص بالجهاز الظاهري.

## كيفية فتح الملف VMX؟

لا يوصى بفتح ملف VMX يدويًا. عند تشغيل جهاز افتراضي باستخدام VMware Fusion, يقوم البرنامج تلقائيًا بتحميل المعلومات من ملف VMX.

ومع ذلك, إذا كنت تريد تحرير ملف VMX يدويًا, فيمكنك القيام بذلك باستخدام أي محرر نصوص, مثل Notepad (Windows) أو TextEdit (Mac).

## ما هو تنسيق ملف VMX؟

ملف VMX هو ملف نصي عادي بتنسيق محدد. يتبع التنسيق بنية زوج المفتاح والقيمة حيث يمثل كل سطر خيار تكوين منفصل.

التنسيق العام لملف VMX هو كما يلي:

```
key1 = value1
key2 = value2
key3 = value3
```

يتكون كل سطر من مفتاح متبوعًا بعلامة المساواة (=) والقيمة المقابلة. يمثل المفتاح إعداد تكوين محدد وتمثل القيمة القيمة المخصصة لهذا الإعداد.

على سبيل المثال, يحدد `memSize = "8192"` في ملف VMX أن حد ذاكرة الجهاز الظاهري هو 8192 ميجابايت من ذاكرة الوصول العشوائي.

قد يتضمن تنسيق ملف VMX أيضًا تعليقات, يُشار إليها بعلامة الجنيه (#) في بداية السطر, والتي يتم تجاهلها بواسطة برنامج VMware عند تحليل الملف. تُستخدم التعليقات غالبًا لتوفير معلومات أو توضيحات إضافية لإعدادات معينة.

## مراجع
* [نموذج ملف VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




