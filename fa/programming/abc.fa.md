
{
  "date": "2021-12-14",
  "keywords": [
"فایل abc",
"افزونه",
"قالب",
"فایل کد بایت اکشن اسکریپت",
"نحوه باز کردن فایل .abc",
"فرمت فایل abc"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "ABC - فایل کد بایت اکشن اسکریپت",
  "description": "با مثال و APIهایی که می توانند فایل های ABC را ایجاد و باز کنند، درباره فرمت فایل ABC بدانید.",
  "linktitle": "ABC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ab-fac"
}
}،
  "lastmod": "2021-12-14"
}

## فایل ABC چیست؟

یک فایل با پسوند abc. یک فایل کد بایتی اکشن اسکریپت است که توسط کامپایلر فلش در نتیجه کامپایل کردن فایل های اسکریپت اکشن اسکریپت ایجاد شده است. کد بایت موجود در فایل ABC توسط ماشین مجازی ActionScript (AVM و AVM2) اجرا می شود. کد بایت شامل داده های ثابت، دستورالعمل های مجموعه دستورات AVM2 و انواع مختلفی از ابرداده است. هنگامی که یک فایل ABC در AVM یا AVM2 بارگذاری می شود، مورد تایید قرار می گیرد. اگر با نمای کلی AVM2 مطابقت نداشته باشد، رد می شود. فایل های ABC را می توان در Adobe Flash Player که مدت ها پیش متوقف شده است باز کرد.

## فرمت فایل ABC - اطلاعات بیشتر

فایل‌های ABC در قالب فایل باینری روی دیسک ذخیره می‌شوند که توسط ماشین‌های مجازی AVM یا AVM2 قابل خواندن هستند. ساختار فایل داخلی آن بلوک کد اجرایی را با تمام داده های ثابت، توصیفگرهای نوع، کد و ابرداده آن نشان می دهد.

## ساختار فایل ABC

ساختار فایل ABC مطابق شکل زیر است.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### فیلدهای فایل ABC

|نام فیلد|توضیحات|
---|---|
|minor_version, major_version|مقادیر major_version و minor_version شماره نسخه اصلی و فرعی فرمت abcFile هستند.|
|constant_pool|constant_pool ساختاری با طول متغیر است که از اعداد صحیح، دوتایی، رشته‌ها، فضاهای نام، مجموعه‌های فضای نام و چند نام تشکیل شده است.|
|method_count, method|مقدار ofmethod_count تعداد ورودی‌های آرایه متد است. هر ورودی در آرایه متد یک ساختار متغییر متد_info است.|
|metadata_count, metadata|مقدار metadata_count تعداد ورودی‌های آرایه ابرداده است. هر ورودی ابرداده یک ساختار فراداده است که یک نام را به مجموعه ای از مقادیر رشته ترسیم می کند. |
|class_count, instance, class|مقدار class_count تعداد ورودی‌های موجود در آرایه‌های نمونه و کلاس است. |
|script_count, script|مقدار script_count تعداد ورودی های آرایه اسکریپت است. هر ورودی اسکریپت یک ساختار script_info است که ویژگی های یک اسکریپت واحد را در این فایل تعریف می کند. |
|method_body_count, method_body|مقدار method_body_count تعداد ورودی‌های آرایه متد_بدن است. هر method_bodyentry از یک ساختار متغییر method_body_info تشکیل شده است که حاوی دستورالعمل های یک متد یا تابع جداگانه است.

## منابع

 * [ABC قوی (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

