{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"XAR - تنسيق ملف الأرشيف القابل للتوسيع" ,
  "description":"تعرف على تنسيق ملف XAR وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات XAR وفتحها." ,
  "linktitle" : "XAR",
  "menu" : {
    "docs" : {
    "identifier": "compression-xar",
      "parent" : "compression"
}
} ,
  "lastmod" : "2021-04-13"
}

## ما هو ملف XAR؟

الملف ذو الامتداد .xar (تنسيق الأرشيف القابل للتوسيع) هو أرشيف UNIX قد يكون بتنسيق مضغوط أو غير مضغوط. يتم استخدامه أيضًا على نظام التشغيل Mac OS لتثبيت الحزم. XAR مفتوح المصدر وكان جزءًا من Mac OS X 10.5 للاستخدام مع متصفح Safari.

## تنسيق ملف XAR

يحتوي ملف [XAR] (https://github.com/mackyle/xar/wiki/xarformat) على ثلاث مناطق رئيسية.

* رأس
* جدول المحتويات
* كومة

### رأس XAR

تم تنظيم رأس XAR على النحو التالي.

| حقل | نوع البيانات | الحجم بالبايت |
---|---|---|
| Magic | Unsigned Int 32 | 4 |
| الحجم | غير محدد Int 16 | 2 |
| الإصدار | Unsigned Int 16 | 2 |
| مضغوط طول جدول المحتويات | غير محدد Int 64 | 8 |
| طول جدول المحتويات غير مضغوط | غير محدد Int 64 | 8 |
| المجموع الاختباري | عدد العمليات 32 غير الموقعة | 4 |
| اسم ملخص الرسالة | مُنتهي بلا قيمة ||

يمكن تعريف البنية C لرأس XAR على النحو التالي.
```
struct xar_header {
    uint32_t magic;
    uint16_t size;
    uint16_t version;
    uint64_t toc_length_compressed;
    uint64_t toc_length_uncompressed;
    uint32_t cksum_alg;
    /* A nul-terminated, zero-padded to multiple of 4, message digest name
     * appears here if cksum_alg is 3 which must not be empty ("") or "none".
     */
};
```
لاحظ أن جميع حقول الرأس (السحر ، الحجم ، الإصدار ، toc_length_compressed ، toc_length_uncompressed ، cksum_alg) يتم تخزينها دائمًا في ملفات XAR بترتيب بايت الشبكة (المعروف أيضًا باسم endian الكبير).

### جدول محتويات XAR (TOC)

جدول المحتويات هو مستند XML (ويجب) ترميزه كـ UTF-8. يتم تخزينه في بداية الملف ، مما يسهل عملية المسح من خلال الأرشيف لاستخراج الملف الفردي. يتيح لك أرشيف XAR ضغط / ترميز الملفات الفردية في الأرشيف بشكل مستقل باستخدام أنظمة ضغط مختلفة مثل [GZIP] (/ar/ compression / gz /) و [BZIP2] (/ar/ compression / bz2) وأنظمة أخرى مماثلة.

```
<?xml version="1.0"?>

<xar>
  <toc>
    <checksum style="sha1">
      <size>20</size>
      <offset>0</offset>
    </checksum>
    <file id="1">
      <name>xar</name>
      <type>file</type>
      <mode>0755</mode>
      <uid>0</uid>
      <gid>0</gid>
      <user>root</user>
      <group>wheel</group>
      <size>81180</size>
      <data>
        <offset>0</offset>
        <size>74108</size>
        <length>23083</length>
        <extracted-checksum style="md5">d852c77ac3c8e83f312c12b4c3198e6d</checksum>
        <archived-checksum style="md5">ceaf793ccb1990ecbadb20112d5f9e5d</checksum>
        <encoding style="application/x-gzip"/>
      </data>
      <ea>
        <name>com.apple.ResourceFork</name>
        <offset>0</offset>
        <size>7072</size>
        <length>3942</length>
        <extracted-checksum style="md5">0f7061dca2d7411352377db0e53792db</checksum>
        <archived-checksum style="md5">c72de8ac25abe462a930254d82958534</checksum>
        <encoding style="application/x-gzip"/>
      </ea>
    </file>
  </toc>
</xar>
```

### كومة

يبدأ الكومة مباشرة بعد toc المضغوط. إنها كومة غير منظمة من البيانات المشار إليها بواسطة جدول المحتويات. تبدأ قيم الإزاحة المدرجة في جدول المحتويات من بداية الكومة. تشير قيم الطول في toc إلى العدد الفعلي للبايتات المخزنة في الكومة (مضغوطة أم لا) بينما تشير قيمة الحجم إلى الحجم المستخرج للعنصر (بعد فك الضغط إذا لزم الأمر).

## مراجع

* [XAR] (https://github.com/mackyle/xar/wiki/xarformat)
* [XAR - ويكيبيديا] (https://en.wikipedia.org/wiki/Xar_ (أرشيفي))

