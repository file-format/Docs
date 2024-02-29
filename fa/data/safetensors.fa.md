{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
}،
  "draft" : "false",
  "toc" : true,
  "title" : "SAFETENSORS - مدل انتشار پایدار - SAFETENSORS چیست و چگونه آن را باز کنیم؟",
  "description":"با فایل SAFETENSORS Sable Diffusion Model و نحوه باز کردن آن آشنا شوید.",
  "linktitle" : "SAFETENSORS",
  "menu" : {
    "docs" : {
      "identifier": "data-safetensors-fa",
      "parent" : "data"
}
}،
  "lastmod" : "2023-12-28"
}

## Safetensors چیست؟

Safetensors فرمت سریال سازی جدیدی است که توسط Hugging Face توسعه یافته است. این مانند یک روش ویژه برای ذخیره و بازیابی تکه های داده بزرگ و پیچیده به نام تانسور است که در یادگیری عمیق بسیار مهم هستند. یادگیری عمیق شامل کار با داده های زیادی است و گاهی اوقات پرداختن به این قطعات کلان داده می تواند مشکل باشد. Safetensors کمک می کند تا در هنگام کار با یادگیری عمیق، کار با این بخش های داده بزرگ و پیچیده آسان تر و کارآمدتر شود.

## فایل Safetensors چیست؟

Safetensors file stores algorithms to deal with tensors safely and used in machine learning model created by **Stable Diffusion** that **generates image from text description**. It is considered safe from any malicious code.

## تانسور چیست؟

تانسور یک مفهوم ریاضی است که در زمینه های مختلف از جمله فیزیک و علوم کامپیوتر استفاده می شود. روشی برای نمایش داده ها به صورت آرایه چند بعدی است. در زمینه **یادگیری عمیق و هوش مصنوعی**، تانسورها ساختارهای داده اساسی هستند که برای سازماندهی و دستکاری داده ها استفاده می شوند. آنها می توانند بردار (آرایه های 1 بعدی)، ماتریس ها (آرایه های 2 بعدی) یا دارای ابعاد بیشتری باشند و نقش مهمی در عملیات انجام شده توسط شبکه های عصبی در طول فرآیند یادگیری دارند. تانسور را به عنوان محفظه ای برای داده های عددی در نظر بگیرید که به روش خاصی مرتب شده اند تا محاسبات و پردازش داده ها را کارآمدتر کنند.

## درباره انتشار پایدار

Stable Diffusion نوع خاصی از برنامه کامپیوتری است که در سال 2022 منتشر شد و از تکنیک قدرتمندی به نام انتشار در یادگیری عمیق استفاده می کند. این بخشی از موج پیشرفت های فعلی در هوش مصنوعی است.

Its main job is to create detailed pictures based on written descriptions, but it can also be used for other tasks like filling in missing parts of images, creating new parts outside original image and transforming images based on written instructions. 

## چگونه یک فایل SAFETENSORS را باز کنیم؟

اگر می خواهید از یک فایل SAFETENSOR با Stable Diffusion استفاده کنید، باید آن را در پوشه ای که Stable Diffusion به دنبال مدل می گردد قرار دهید.

