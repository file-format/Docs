{
   "date":"2023-10-11",
   "keywords":[
"سایه زن",
"فایل سایه زن",
"فایل shader quake 3 engine shader",
"نحوه باز کردن فایل شیدر",
"فایل",
"پسوند فایل shader",
"افزونه",
"فایل"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"فرمت فایل SHADER - فایل Shader موتور Quake 3",
   "description":"درباره فرمت فایل SHADER Quake 3 Engine Shader و APIهایی که می‌توانند فایل‌های SHADER را ایجاد و باز کنند، بیاموزید.",
   "linktitle":"SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake-fa",
         "parent":"game"
}
},
   "lastmod":"2023-10-11"
}

## فایل SHADER چیست؟

فرمت فایل SHADER در **موتور Quake 3** برای تعریف سایه زن برای بافت ها و متریال ها در بازی استفاده می شود. سایه بان ها برای تعیین نحوه نمایش یک سطح، از جمله ظاهر، بازتاب، شفافیت و سایر ویژگی های بصری آن استفاده می شوند.

## فایل Shader موتور Quake 3

در اینجا مروری کلی بر ساختار و نحو فایل سایه زن موتور Quake 3 است:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

در فایل shader موتور Quake 3 می توانید چندین سایه زن تعریف کنید که هر کدام دارای مجموعه ای از ویژگی ها و مراحل خاص خود هستند. از این شیدرها برای تعریف ظاهر بافت ها و متریال های مختلف در دنیای بازی استفاده می شود. موتور از این اطلاعات برای نمایش سطوح با جلوه ها و رفتارهای بصری مشخص استفاده می کند.

فایل‌های Shader در موتور Quake 3 فایل‌های متنی ساده‌ای هستند که حاوی دستورالعمل‌هایی برای نحوه نمایش بافت‌ها و متریال‌ها در بازی هستند. این فایل ها را می توان با ویرایشگر متن معمولی باز و ویرایش کرد و معمولاً در فهرست **/scripts** در بسته .PK3 بازی یافت می شوند.

## موتور Quake 3

موتور Quake 3 یک موتور بازی بسیار تاثیرگذار و همه کاره است که توسط id Software توسعه یافته است. اولین بار با انتشار بازی Quake III Arena در سال 1999 معرفی شد و از آن زمان در بازی های مختلف دیگری نیز استفاده شده است. این موتور به خاطر گرافیک پیشرفته، قابلیت های چند نفره و قابلیت تغییر شهرت دارد.

در اینجا برخی از ویژگی ها و جنبه های کلیدی موتور Quake 3 آورده شده است:

1.  **موتور گرافیکی:** موتور Quake 3 در آن زمان به خاطر فناوری گرافیکی پیشرفته خود مشهور بود. ویژگی‌های پیشرفته‌ای مانند سطوح منحنی، سایه‌زنان و نورپردازی پویا را معرفی کرد که در اواخر دهه 1990 پیشگام بود.
    
2.  **تمرکز چند نفره:** Quake 3 Arena در اصل به عنوان تیراندازی اول شخص چند نفره طراحی شده بود. کد شبکه موتور و پشتیبانی از بازی های چند نفره آنلاین استثنایی بود و آن را به انتخابی محبوب برای بازی آنلاین رقابتی تبدیل کرد.
    
3.  **تغییر پذیری:** موتور Quake 3 به دلیل قابلیت تغییر شناخته شده است. id Software کد منبع موتور را تحت مجوز منبع باز گنو عمومی عمومی (GPL) منتشر کرد. این امر باعث ایجاد حالت‌های متعدد و نقشه‌های سفارشی شد که منجر به ایجاد جامعه مودینگ پر جنب و جوش شد.
    
4.  **بازی اسکریپت شده:** این موتور از سیستم مبتنی بر اسکریپت برای تعریف قوانین و رفتار بازی استفاده می‌کرد که ایجاد حالت‌های بازی سفارشی و تجربه‌های منحصربه‌فرد را برای مددرها و نقشه‌برداران نسبتاً آسان می‌کرد.
    
5.  **پشتیبانی از محتوای سفارشی:** موتور Quake 3 از محتوای سفارشی، از جمله بافت‌ها، مدل‌ها و فایل‌های صوتی پشتیبانی می‌کرد که به درجه بالایی از سفارشی‌سازی در نقشه‌ها و مدهای ساخته‌شده توسط کاربر امکان‌پذیر بود.
    
6.  **طراحی سطح:** موتور از سیستم طراحی سطح مبتنی بر قلم مو استفاده می کرد، جایی که نقشه ها با کنده کاری فضاها از برس های جامد ساخته می شدند. این رویکرد برای طراحان سطح به خوبی مستند و کاربرپسند بود.


در طول سال‌ها، موتور Quake 3 به‌عنوان پایه‌ای برای بسیاری از بازی‌ها و مدهای دیگر، از جمله «Return to Castle Wolfenstein»، «Star Wars Jedi Knight II: Jedi Outcast» و «Urban Terror» استفاده شده است. میراث ماندگاری در دنیای توسعه بازی به جا گذاشت و به شکل گیری سبک تیراندازی اول شخص کمک کرد. در حالی که موتورهای جدیدتر و پیشرفته‌تر از آن زمان ظهور کرده‌اند، موتور Quake 3 همچنان به دلیل سهمش در صنعت بازی مورد احترام است.

## چگونه فایل SHADER را باز کنیم؟

برنامه هایی که فایل های SHADER را باز می کنند یا به آنها ارجاع می دهند شامل می شوند

- ** id Software Quake 3 ** (پرداخت شده) برای (ویندوز، مک، لینوکس)
- دفترچه یادداشت مایکروسافت
- Notepad++
- هر ویرایشگر متنی

## سایر فایل های SHADER

در اینجا انواع فایل دیگری وجود دارد که از پسوند فایل **.shader** استفاده می کنند.

**فایل های بازی**
- [SHADER - Godot Engine Shader File](/game/shader-godot/)
- [SHADER - Quake 3 Engine Shader File](/game/shader-quake/)
- [SHADER - Unity Shader Asset](/game/shader-unity/)

## منابع
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

