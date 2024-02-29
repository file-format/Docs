{
  "date": "2019-12-03",
  "keywords": [
"DOCX",
"فایل",
"قالب",
"نوع فایل",
"افزونه",
"فایل DOCX چیست؟"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOCX",
  "description": "درباره فرمت فایل DOCX و APIهایی که می‌توانند فایل‌های DOCX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "DOCX",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-doc-fax"
}
},
  "lastmod": "2019-12-03"
}

## فایل DOCX چیست؟ ##

DOCX یک فرمت شناخته شده برای اسناد Microsoft Word است. از سال 2007 با انتشار Microsoft Office 2007، ساختار این قالب سند جدید از باینری ساده به ترکیبی از فایل های XML و باینری تغییر یافت. فایل‌های Docx را می‌توان با Word 2007 و نسخه‌های جانبی باز کرد، اما با نسخه‌های قبلی MS Word که از پسوند فایل DOC پشتیبانی می‌کنند، نمی‌توان آن‌ها را باز کرد.

## تاریخچه مختصر ##

After Microsoft opened the specifications for the DOC file format, it was easy for its competitors to reverse engineer the format and provide the same support in their own applications. In addition, the competition from Open Office in the form of its Open Document Format, compelled Microsoft to adopt more open and wide standards. It was in early 2000 when Microsoft decided to go for the change to accommodate the standard for **Office Open XML**. Documents under this new Standard were given [.docx extension](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd), the "X" being for XML. By 2007, this new file format became part of Office 2007 and is carried on in the new versions of Microsoft Office as well. The new file type has added advantages of small file sizes, fewer changes of corruption and well-formatted images representation.

## مشخصات فرمت فایل DOCX - اطلاعات بیشتر

یک فایل Docx شامل مجموعه ای از فایل های XML است که در یک آرشیو ZIP قرار دارند. محتویات یک سند Word جدید را می توان با بازکردن محتویات آن مشاهده کرد. این مجموعه حاوی لیستی از فایل های XML است که به صورت زیر دسته بندی می شوند:

* فایل های متا دیتا - حاوی اطلاعاتی در مورد سایر فایل های موجود در آرشیو است

* سند - حاوی محتویات واقعی سند است


### فایل های فراداده ###

مایکروسافت ورد از این فایل ها برای یافتن رابطه بین فایل ها و مکان یابی محتوای سند استفاده می کند. هنگامی که یک آرشیو سند Word استخراج می شود، حاوی تعدادی از این فایل ها است که در زیر توضیح داده شده است.

#### روابط - \_rels/.rels ####

این فایل حاوی اطلاعاتی است که به MS Word می گوید که در کجا به دنبال محتویات سند و سایر مراجع بگردد. هر رابطه با یک شناسه رابطه منحصر به فرد شناسایی می شود و فایل XML ارجاع شده را به عنوان هدف مشخص می کند. نمونه فایل رابطه به صورت زیر نشان داده شده است:

```
<Relationship Id#"rId1" Type#"http://schemas.openxmlformats.org/officeDocument/2006/relationships/officeDocument" Target#"word/document.xml"/>.
```

#### انواع محتوا ####

یک سند می‌تواند حاوی چندین نوع رسانه مانند تصاویر، مضامین، هنرهای کلمه، و غیره باشد. [Content_Types].xml حاوی اطلاعاتی درباره انواع رسانه‌های موجود در سند است. محتویات یک چنین فایل XML به صورت زیر نشان داده شده است:

```
<Override PartName#"/word/document.xml" ContentType#"application/vnd.openxmlformats-officedocument.wordprocessingml.document.main+xml"/>
```

#### مراجع به منابع - \_rels/document.xml.rels ####

اطلاعات مربوط به منابع، مانند تصاویر جاسازی شده در سند، در این فایل XML ارجاع داده شده است.

#### محتوای سند اصلی ####

این به فایل XML اصلی بایگانی اشاره دارد که حاوی محتوای متنی سند است. این محتوا طبق مشخصات OpenOffice XML با انواع گره ها نشان داده می شود. بیشتر محتویات این فایل از پاراگراف ها و جداول تشکیل شده است، اگرچه آنها می توانند گره های دیگری نیز باشند.

### گره های فرمت فایل ###

فایل document.xml اصلی مجموعه ای از گره ها برای نمایش محتویات کلی یک فایل است. هر گره شروع و پایانی دارد که گره های دیگر یا محتویات را در خود محصور می کند. یک مثال ساده از چنین فایل xml به شرح زیر است:

```
<w:document>
   <w:body>
       <w:p w:rsidR#"005F670F" w:rsidRDefault#"005F79F5">
           <w:r><w:t>Example Document</w:t></w:r>
       </w:p>
       <w:sectPr w:rsidR#"005F670F">
           <w:pgSz w:w#"12240" w:h#"15840"/>
           <w:pgMar w:top#"1440" w:right#"1440" w:bottom#"1440" w:left#"1440" w:header#"720" w:footer#"720"
                    w:gutter#"0"/>
           <w:cols w:space#"720"/>
           <w:docGrid w:linePitch#"360"/>
       </w:sectPr>
   </w:body>
</w:document>
```

در زیر اطلاعاتی در مورد برخی از گره های موجود در یک فایل DOCX برای نمایش محتوا آمده است.

`<w:document> ` - نشان دهنده عنصر ریشه محتوای اصلی فایل است.

`<w:body> ` - نمایانگر بدنه سند است که می تواند از بسیاری از گره های عنصر دیگر مانند پاراگراف ها، جداول و بخش ها تشکیل شده باشد.

#### پاراگراف ها ####

یک پاراگراف، دارنده محتوای اصلی یک سند است. این توسط **<w:p> ** عنصر در یک سند. یک پاراگراف بیشتر از یک یا چند اجرا تشکیل شده است **<w:r> ** که حاوی متن واقعی پاراگراف است. علاوه بر اجراها، پاراگراف ها ممکن است حاوی عناصر سند دیگری مانند لینک ها، نظرات و غیره باشند. یک نمونه ساختار پاراگراف مانند زیر است:

```
<w:p>
<w:pPr>
<w:pStyle> w:val#"MyStyle"/>
<w:spacing w:before#"120" w:after#"120"/>
</w:pPr>
<w:r>
<w:t xml"space#"preserve">A paragraph is main container in a document that further consists of a one or more runs where the text of paragraph is actually contained.</w:t>
</w:r>
</w:p>
```

## سوالات متداول DOCX

 * **آیا DOCX یک پسوند فایل است؟** - DOCX به عنوان پسوند فایل برای نمایش فرمت های فایل Microsoft Word 2007 و بعد از آن برای ذخیره فایل های Word استفاده می شود. همچنین به سیستم عامل شما می گوید که این فایل DOCX به Microsoft Word 2007 نیاز دارد تا آن را باز کند و نماد آن را نشان دهد.
 * **آیا DOCX همانند Word** است - DOCX فرمت فایلی است که توسط Microsoft Word برای ذخیره اسناد در قالب Open XML استفاده می شود. از طرف دیگر، Word یک نرم افزار کاربردی توسط مایکروسافت آفیس است که از فرمت های دیگر فایل مانند DOC، DOT، DOTM و غیره نیز پشتیبانی می کند.
 * ** تفاوت DOC و DOCX ** - DOC فایل word است که در فرمت فایل Word 2007 و قبل از آن ذخیره شده است. DOCX بر اساس فرمت فایل XML Open است که توسط مایکروسافت 2007 و نسخه های بعدی پشتیبانی می شود. برای جزئیات بیشتر، [تفاوت بین DOC و DOCX](https://blog.fileformat.com/2022/08/11/doc-vs-docx/) را بررسی کنید.

## منابع ##

* [MS - فرمت فایل DOCX](https://learn.microsoft.com/en-us/openspecs/office_standards/ms-docx/b839fe1f-e1ca-4fa6-8c26-5954d0abbccd)

* [Office Open XML](http://officeopenxml.com/)


