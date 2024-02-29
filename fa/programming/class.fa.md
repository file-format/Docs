{
  "date": "2019-10-11",
  "keywords": [
"کلاس",
".کلاس",
"فایل کلاس چیست",
"نحوه باز کردن فایل کلاس",
"افزونه",
"فایل",
"فایل کلاس",
"فرمت فایل کلاس",
"پسوند کلاس",
"فایل کلاس در جاوا"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "کلاس - فرمت فایل کلاس جاوا",
  "description": "درباره قالب فایل Class و APIهایی که می‌توانند فایل‌های Class را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-clas-fas"
}
},
  "lastmod": "2020-09-10"
}

## فایل Class چیست؟

فایل **Class در جاوا** خروجی کامپایل شده کلاس [.java](/programming/java/) است که در واقع توسط یک ماشین مجازی جاوا (JVM) اجرا می شود. فایل های کلاس را می توان به صورت جداگانه اجرا کرد و همچنین می تواند بخشی از یک فایل [JAR](/programming/jar/) به عنوان یک بسته همراه با سایر فایل های بسته باشد. اینها را می توان با استفاده از دستور **`javac`** از رابط خط فرمان ایجاد کرد. برخی از IDE های جاوا مانند [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) و NetBeans فایل های خروجی .class را از فایل های جاوا پروژه ایجاد می کنند.

## فرمت فایل کلاس

یک فایل کلاس جاوا شامل کد بایتی است که یک کد میانی برای اجرا توسط JVM است. یک فایل کلاس شامل جریانی از بایت های 8 بیتی است و موارد داده چند بایتی همیشه به ترتیب بزرگ ذخیره می شوند.

### ساختار فایل کلاس

ساختار فایل کلاس مانند شکل زیر است.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
جایی که:

* u1 = مقدار یک بایت بدون علامت

* u2 = مقدار دو بایت بدون علامت

* u4 = مقدار چهار بایت بدون علامت


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `magic` - آیتم جادویی شماره جادویی را ارائه می دهد که فرمت فایل کلاس را مشخص می کند. مقدار آن 0xCAFEBABE است.

* 'minor_version'، 'major_version' - مقادیر موارد minor_version و major_version شماره‌های نسخه اصلی و اصلی این فایل کلاس هستند.

* "constant_pool_count" - مقدار مورد ثابت_pool_count برابر است با تعداد ورودی های جدول ثابت_pool به اضافه یک. یک شاخص konstant_pool در صورتی معتبر تلقی می شود که بزرگتر از صفر و کمتر از ثابت_pool_count باشد، به استثنای ثابت های نوع long و double.

* "constant_pool[]" - استخر_constant جدولی از ساختارها (§4.4) است که ثابت‌های رشته‌ای مختلف، نام‌های کلاس و رابط، نام فیلدها و سایر ثابت‌ها را نشان می‌دهد که در ساختار ClassFile و زیرساخت‌های آن به آن اشاره می‌شود. قالب هر ورودی جدول ثابت_pool با اولین بایت "برچسب" آن نشان داده می شود.

* "access_flags" - مقدار آیتم access_flags ماسکی از پرچم‌ها است که برای نشان دادن مجوزهای دسترسی و ویژگی‌های این کلاس یا رابط استفاده می‌شود.

* `this_class` - مقدار مورد this_class باید یک شاخص معتبر در جدول konstant_pool باشد.

* `super_class` - برای یک کلاس، مقدار آیتم super_class یا باید صفر باشد یا باید یک شاخص معتبر در جدول konstant_pool باشد.

* 'interfaces_count' - مقدار آیتم interfaces_count تعداد سوپر اینترفیس های مستقیم این کلاس یا نوع رابط را نشان می دهد.

* `Interfaces[]` - هر مقدار در آرایه واسط ها باید یک شاخص معتبر در جدول konstant_pool باشد.

* `counts_fields` - مقدار مورد fields_count تعداد ساختارهای field_info را در جدول فیلدها نشان می دهد.

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `methods_count` - مقدار آیتم method_count تعداد ساختارهای method_info را در جدول متدها نشان می دهد.

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* "ویژگی_شمار" - مقدار مورد ویژگی_count تعداد صفات (§4.7) را در جدول ویژگی های این کلاس نشان می دهد.

* `ویژگی‌ها[]` - هر مقدار از جدول ویژگی‌ها باید ساختار ویژگی_info باشد.





## منابع

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

