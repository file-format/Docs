{
  "date" : "2022-03-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"تنسيق ملف PCX - ملف صورة نقطية لفرشاة الرسام" ,
  "description":"تعرف على تنسيق ملف PCX وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PCX وفتحها." ,
  "linktitle" : "PCX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
} ,
  "lastmod" : "2022-03-16"
}

## ما هو ملف PCX؟

ملف PCX ، ملف Picture Exchange ، هو تنسيق ملف صورة نقطية تم استخدامه كتنسيق ملف أصلي لتطبيق PC Paintbrush. تم تطويره بواسطة ZSoft Corporation ، الولايات المتحدة الأمريكية لأنظمة DOS و Windows وتم اعتماده كتنسيق ملف التصوير الرئيسي قبل وصول [BMP](/ar/image/bmp/) ، [JPEG](/ar/image/jpeg/) ، و [ PNG](/ar/image/png/) تنسيقات الملفات. تكون ملفات PCX أصغر حجمًا حيث يتم ضغطها باستخدام تشفير RLE. يتم استخدامه في ملف [DCX](/ar/image/dcx/) متعدد الصفحات الذي يستخدم بشكل أساسي لإنشاء ملفات فاكس رقمية.

## تنسيق ملف PCX

يتم حفظ ملفات PCX على القرص بتنسيق ملف ثنائي. يتبع هيكل تنسيق الملف الداخلي ترتيب بايت صغير ويحتوي على الأقسام الثلاثة التالية:

** "رأس PCX" ** - يبلغ طول رأس PCX 128 بايت. يحتوي على معرف ورقم إصدار وأبعاد الصورة و 16 لونًا للوحة وعدد مستويات الألوان وعمق البت لكل مستوى وقيمة لطريقة الضغط.

يتم عرض رأس PCX كما هو موضح أدناه مع مرجع من موسوعة تنسيقات ملفات الرسومات (الطبعة الثانية).
```
typedef struct _PcxHeader
{
  BYTE	Identifier;        /* PCX Id Number (Always 0x0A) */
  BYTE	Version;           /* Version Number */
  BYTE	Encoding;          /* Encoding Format */
  BYTE	BitsPerPixel;      /* Bits per Pixel */
  WORD	XStart;            /* Left of image */
  WORD	YStart;            /* Top of Image */
  WORD	XEnd;              /* Right of Image
  WORD	YEnd;              /* Bottom of image */
  WORD	HorzRes;           /* Horizontal Resolution */
  WORD	VertRes;           /* Vertical Resolution */
  BYTE	Palette[48];       /* 16-Color EGA Palette */
  BYTE	Reserved1;         /* Reserved (Always 0) */
  BYTE	NumBitPlanes;      /* Number of Bit Planes */
  WORD	BytesPerLine;      /* Bytes per Scan-line */
  WORD	PaletteType;       /* Palette Type */
  WORD	HorzScreenSize;    /* Horizontal Screen Size */
  WORD	VertScreenSize;    /* Vertical Screen Size */
  BYTE	Reserved2[54];     /* Reserved (Always 0) */
} PCXHEAD;
```

** `بيانات الصورة` ** - تتبع بيانات صورة PCX بعد العنوان مباشرةً. قد يتم ضغط بيانات الصورة اعتمادًا على إعداد الحقل في الرأس. يعتمد تخزين البيانات في ملف PCX على عدد مستويات الألوان المحددة. يتم تنظيم بيانات الصورة في صفوف. في حالة وجود مستويات متعددة ، يتم تخزينها عن طريق المستوى داخل الصف بترتيب تسلسلي للبيانات الحمراء والخضراء والزرقاء. يتكرر هذا النمط لكل سطر في المستوى.

## مراجع

* [PCX - بواسطة Wikipedia](https://en.wikipedia.org/wiki/PCX)

