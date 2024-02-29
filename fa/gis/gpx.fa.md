{
  "date": "2019-10-11",
  "keywords": [
"فایل gpx",
"فایل gpx چیست",
"فایل",
"نمونه gpx",
"پسوند فایل gpx",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPX - فرمت فایل تبادل GPX",
  "description": "درباره فرمت فایل GPX و APIهایی که می‌توانند فایل‌های GPX را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "GPX",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-gp-fax"
}
},
  "lastmod": "2019-09-10"
}

## فایل GPX چیست؟

فایل‌های با پسوند GPX فرمت تبادل GPS را برای تبادل داده‌های GPS بین برنامه‌ها و سرویس‌های وب در اینترنت نشان می‌دهند. این یک فرمت فایل XML سبک وزن است که حاوی داده‌های GPS است، یعنی نقاط بین راهی، مسیرها و مسیرهایی که باید توسط چندین برنامه وارد شده و قرمز شود. فرمت فایل GPX باز است و توسط انواع برنامه ها و دستگاه های GPS پشتیبانی می شود. داده های GPS از چنین فایل هایی را می توان برای نمایش در برنامه های نقشه برداری برای اهداف جغرافیایی - فضایی بارگذاری کرد.

## فرمت فایل GPX ##

یک فایل GPX از داده های موقعیت جغرافیایی و طول جغرافیایی، مقادیر ارتفاع و سایر اطلاعات توصیفی احتمالاً دیگر تشکیل شده است. داده های مکان به صورت درجه اعشار و ارتفاع بر حسب متر بیان می شود. زمان در یک فایل GPX در زمان هماهنگ جهانی (UTC) با فرمت ISO 8601 است. مزایای استفاده از فایل GPX به شرح زیر است:

* GPX به شما امکان می دهد با لیست رو به رشدی از برنامه ها برای Windows، MacOS، Linux، Palm و PocketPC، داده ها را مبادله کنید.

* GPX را می توان با استفاده از یک صفحه وب ساده یا برنامه مبدل به فرمت های فایل دیگر تبدیل کرد.

* GPX بر اساس استاندارد XML است، بنابراین بسیاری از برنامه‌های جدیدی که استفاده می‌کنید (مثلاً مایکروسافت اکسل) می‌توانند فایل‌های GPX را بخوانند.

* GPX توسعه ویژگی های جدید را برای هر کسی در وب آسان می کند که فوراً با برنامه های مورد علاقه شما کار می کند.


[GPX Schema](https://www.topografix.com/GPX/1/1/gpx.xsd) فرمت فایل GPX را برای مرجع نشان می‌دهد.

### داده های اساسی ###

در زیر داده های ضروری است که بخشی از یک فایل GPX برای نمایش داده های GPS است.

* **نقاط بین راه**: نقطه بین مختصات WGS84 (GPS) یک نقطه است و نمایانگر لایه ای از ویژگی های نوع OGR wkbPoint است.

* **مسیرها**: نمایانگر لایه ای از ویژگی های OGR از نوع wkbLineString است. این شامل فهرستی از نقاط مسیر است، که نقاطی هستند که نقطه‌های پیچ یا مرحله‌ای را نشان می‌دهند که به مقصدی منتهی می‌شوند

* **Tracks**: آهنگ ها لایه ای از ویژگی های OGR از نوع wkbMultiLineString را نشان می دهند. حداقل از یک بخش شامل نقاط بین فهرستی از نقاط که یک مسیر را توصیف می کند، ساخته شده است. این شامل لیستی از نقاط مسیر است که نشان دهنده یک مسیر GPS مداوم است.


### فایل نمونه GPX ###

فایل GPX زیر سازماندهی داده های GPS را در یک فایل GPX نشان می دهد و می تواند ایده خوبی در مورد محتوای یک فایل GPX به دست دهد.

```
<gpx xmlns#"http://www.topografix.com/GPX/1/1" xmlns:gpxx#"http://www.garmin.com/xmlschemas/GpxExtensions/v3" xmlns:gpxtpx#"http://www.garmin.com/xmlschemas/TrackPointExtension/v1" creator#"Oregon 400t" version#"1.1" xmlns:xsi#"http://www.w3.org/2001/XMLSchema-instance" xsi:schemaLocation#"http://www.topografix.com/GPX/1/1 http://www.topografix.com/GPX/1/1/gpx.xsd http://www.garmin.com/xmlschemas/GpxExtensions/v3 http://www.garmin.com/xmlschemas/GpxExtensionsv3.xsd http://www.garmin.com/xmlschemas/TrackPointExtension/v1 http://www.garmin.com/xmlschemas/TrackPointExtensionv1.xsd">
  <metadata>
    <link href#"http://www.garmin.com">
      <text>Garmin International</text>
    </link>
    <time>2009-10-17T22:58:43Z</time>
  </metadata>
  <trk>
    <name>Example GPX Document</name>
    <trkseg>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.46</ele>
        <time>2009-10-17T18:37:26Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>4.94</ele>
        <time>2009-10-17T18:37:31Z</time>
      </trkpt>
      <trkpt lat#"47.644548" lon#"-122.326897">
        <ele>6.87</ele>
        <time>2009-10-17T18:37:34Z</time>
      </trkpt>
    </trkseg>
  </trk>
</gpx>
```

## منابع ##

* [فرمت فایل GPX](https://www.topografix.com/gpx.asp)

* [GPX - توسط ویکی‌پدیا](https://en.wikipedia.org/wiki/GPS_Exchange_Format)


