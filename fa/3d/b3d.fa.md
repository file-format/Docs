{
  "date": "2021-04-19",
  "keywords": [
"Blitz3D",
"b3d",
"فایل",
"افزونه",
"قالب",
"بازی های blitz3d"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "description": "با فرمت فایل B3D آشنا شوید. در بازی‌های blitz3d و APIهایی که می‌توانند فایل‌های B3D را باز کرده و ایجاد کنند استفاده می‌شود.",
  "title": "B3D - فایل مدل موجودیت Blitz3D",
  "linktitle": "B3D",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-b3-fad"
}
}،
  "lastmod": "2021-04-19"
}

## فایل B3D چیست؟

یک فایل با پسوند b3d. یک فایل مدل است که توسط Blitz3D استفاده می‌شود که ممکن است شامل مدل‌های بازی ویدیویی برای شخصیت‌ها، ساختمان‌ها، زمین و اشیاء دیگر باشد. Blitz3D یک زبان برنامه نویسی است که برای ایجاد **بازی های blitz3d** استفاده می شود. Blitz3D یک زبان برنامه نویسی قدرتمند، انعطاف پذیر و آسان برای استفاده است که تنها با هدف نوشتن بازی های ویدیویی طراحی شده است. توسعه دهندگان می توانند بازی های سه بعدی اکشن، معماهای دوبعدی، ماجراجویی، RPGS، و هر چیز دیگری را فقط با استفاده از Blitz3D ایجاد کنند.

Blitz3D بر اساس زبان برنامه نویسی BASIC است. که یادگیری و استفاده از آن نیز آسان است. همه این حقایق، Blitz را برای مبتدیان و برنامه نویسان با تجربه تر ایده آل می کند. اگرچه ویژگی های آن تا حدی قدیمی نسبت به موتورهای سه بعدی مدرن تلقی می شوند، Blitz3D همچنان توسط بسیاری از برنامه نویسان بازی در سراسر جهان مورد استفاده قرار می گیرد.

## تاریخچه مختصر Blitz3D

Blitz3D اساساً برای سیستم عامل مایکروسافت ویندوز در سپتامبر 2001 منتشر شد تا با سایر زبان های توسعه بازی مشابه رقابت کند. Blitz3D یک نسخه ارتقا یافته نسبت به موتور دو بعدی قبلی BlitzBasic بود که مجموعه دستورات خود را با افزودن یک API برای موتور سه بعدی مبتنی بر DirectX 7 گسترش داد. کاربران Blitz3D همچنین باید BlitzMax را که موتور بعدی BlitzBasic است مقایسه کنند. BlitzMax یک نسخه پیچیده اما قدرتمندتر از Blitz3D است که از زبان های برنامه نویسی شی گرا پشتیبانی می کند. این یک API گرافیکی به روز شده است که بهتر با کاراکترهای یونیکد، OpenGL مطابقت دارد و به جای ویندوز فقط به OSX و Linux صادر می شود.

## مثال B3D
یک فایل b3d که شامل 1 تکه TEXS، 1 قطعه BRUS و 1 قطعه NODE است، به شکل زیر خواهد بود:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
یک مش ساده، غیر متحرک و بدون بافت به شکل زیر خواهد بود:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## منابع
 * [B3D](https://moddb.fandom.com/wiki/B3D)
 * [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

