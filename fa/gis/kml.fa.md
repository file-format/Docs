{
  "date": "2019-10-11",
  "keywords": [
"فایل kml",
"فایل kml چیست",
"فایل",
"kml مثال",
"پسوند فایل kml",
"افزونه",
"قالب"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "KML - زبان نشانه گذاری سوراخ کلید",
  "description": "درباره فرمت فایل KML و APIهایی که می‌توانند فایل‌های KML را ایجاد و باز کنند، بیاموزید.",
  "linktitle": "KML",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-km-fal"
}
},
  "lastmod": "2019-09-10"
}

## فایل KML چیست؟

KML، Keyhole Markup Language) حاوی اطلاعات مکانی در نماد XML است. فایل‌هایی که به‌عنوان KML ذخیره می‌شوند را می‌توان در برنامه‌های سیستم اطلاعات جغرافیایی (GIS) باز کرد، به شرط اینکه از آن پشتیبانی کنند. بسیاری از برنامه ها پس از پذیرش فرمت فایل KML به عنوان استاندارد بین المللی، پشتیبانی از آن را آغاز کرده اند. KML از یک ساختار مبتنی بر برچسب با عناصر و ویژگی‌های تودرتو استفاده می‌کند. همه برچسب‌ها به حروف بزرگ و کوچک حساس هستند و ترتیب این برچسب‌ها، طبق مرجع [KML](https://developers.google.com/kml/documentation/kmlreference)، مهم است که رعایت شود.

## تاریخچه مختصر ##

KML was originally developed for use with Google Earth which was originally known as Keyhole Earth Viewer. KLM was adopted as international standard in 2008 by the Open Geospatial Consortium in 2008. از آنجایی که این قالب برای استفاده با Google Earth ایجاد شده است، این تمایز را دارد که اولین کسی باشد که فایل های KML را مشاهده و ویرایش می کند. با گذشت زمان، اکنون پروژه های بیشتری وجود دارد که از فرمت های فایل KML از جمله چندین API به زبان های مختلف پشتیبانی می کنند.

## مشخصات فرمت فایل KML ##

مرجع KML یک راهنمای کامل برای ارجاع به منظور داشتن مشخصات فرمت فایل کامل است. یک فایل استاندارد KML شامل موارد زیر است:

* علامت مکان

* مکان نماهای توصیفی HTMLin

* پوشش های زمینی

* راه ها

* چند ضلعی ها


علاوه بر اینها، یک نسخه پیشرفته از فایل KML می تواند دارای موارد زیر باشد:

* سبک برای هندسه

* سبک برای نمادهای برجسته

* پوشش های صفحه نمایش

* پیوندهای شبکه


هر یک از عناصر KML دارای اطلاعات طولانی است که اطلاعات موجود در فایل را مکان یابی می کند. با این حال، ممکن است پارامترهای اضافی مانند عنوان، ارتفاع و شیب نیز وجود داشته باشد.

### علامت‌های مکان ###

برای نشان دادن موقعیتی در سطح زمین استفاده می شود و توسط آن مشخص می شود<Point> عنصر در زیر نمونه ای از نحوه نمایش مکان نشان در فایل KML آورده شده است.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Placemark>
    <name>Simple placemark</name>
    <description>Attached to the ground. Intelligently places itself
       at the height of the underlying terrain.</description>
    <Point>
      <coordinates>-122.0822035425683,37.42228990140251,0</coordinates>
    </Point>
  </Placemark>
</kml>
```

### HTML توصیفی در مکان‌ها ###

اطلاعات اضافی را می‌توان با یک مکان‌مارک مرتبط کرد که نمایش مکان نشان را بیشتر افزایش می‌دهد. چنین اطلاعاتی شامل پیوندها، اندازه فونت ها، سبک ها و رنگ ها است. علاوه بر این، شامل تراز متن و جداول نیز می شود تا بخشی از مکان نشانگر باشد.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <Placemark>
      <name>CDATA example</name>
      <description>
        <![CDATA[
          <h1>CDATA Tags are useful!</h1>
          <p><font color#"red">Text is <i>more readable</i> and
          <b>easier to write</b> when you can avoid using entity
          references.</font></p>
        ]]>
      </description>
      <Point>
        <coordinates>102.595626,14.996729</coordinates>
      </Point>
    </Placemark>
  </Document>
</kml>
```

### روکش های زمینی ###

اینها لایه بندی یک تصویر را بر روی سطح زمین نشان می دهند. این<icon> elment حاوی پیوند به فایل تصویری همپوشانی است.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Folder>
    <name>Ground Overlays</name>
    <description>Examples of ground overlays</description>
    <GroundOverlay>
      <name>Large-scale overlay on terrain</name>
      <description>Overlay shows Mount Etna erupting
          on July 13th, 2001.</description>
      <Icon>
        <href>https://developers.google.com/kml/documentation/images/etna.jpg</href>
      </Icon>
      <LatLonBox>
        <north>37.91904192681665</north>
        <south>37.46543388598137</south>
        <east>15.35832653742206</east>
        <west>14.60128369746704</west>
        <rotation>-0.1556640799496235</rotation>
      </LatLonBox>
    </GroundOverlay>
  </Folder>
</kml>
```

### راه ها ###

مسیرها با نشان داده می شوند<LineString> عنصری که مجموعه ای از جفت های lat-long است. با استفاده از اینها، انواع مختلفی از مسیرها را می توان در Google Earth ایجاد کرد.

```

<kml xmlns#"http://www.opengis.net/kml/2.2">
  <Document>
    <name>Paths</name>
    <description>Examples of paths. Note that the tessellate tag is by default
      set to 0. If you want to create tessellated lines, they must be authored
      (or edited) directly in KML.</description>
    <Style id#"yellowLineGreenPoly">
      <LineStyle>
        <color>7f00ffff</color>
        <width>4</width>
      </LineStyle>
      <PolyStyle>
        <color>7f00ff00</color>
      </PolyStyle>
    </Style>
    <Placemark>
      <name>Absolute Extruded</name>
      <description>Transparent green wall with yellow outlines</description>
      <styleUrl>#yellowLineGreenPoly</styleUrl>
      <LineString>
        <extrude>1</extrude>
        <tessellate>1</tessellate>
        <altitudeMode>absolute</altitudeMode>
        <coordinates> -112.2550785337791,36.07954952145647,2357
          -112.2549277039738,36.08117083492122,2357
          -112.2552505069063,36.08260761307279,2357
          -112.2564540158376,36.08395660588506,2357
          -112.2580238976449,36.08511401044813,2357
          -112.2595218489022,36.08584355239394,2357
          -112.2608216347552,36.08612634548589,2357
          -112.262073428656,36.08626019085147,2357
          -112.2633204928495,36.08621519860091,2357
          -112.2644963846444,36.08627897945274,2357
          -112.2656969554589,36.08649599090644,2357
        </coordinates>
      </LineString>
    </Placemark>
  </Document>
</kml>
```

## ارجاع مکانی در فایل KML ##

اطلاعات موجود در هر فایل Geospatial درباره مکان‌های جغرافیایی می‌تواند معانی مختلفی بدون اطلاعات ارجاع مکانی داشته باشد. به طور پیش فرض، ارجاع مکانی فایل KML توسط سیستم جهانی ژئودتیک 1984، WGS84 تعریف شده است.

## منابع ##

* [مرجع KML](https://developers.google.com/kml/documentation/kmlreference)

* [آموزش برنامه‌نویس Google برای KML](https://developers.google.com/kml/documentation/kml_tut)

* [فرمت فایل KML] (https://en.wikipedia.org/wiki/Keyhole_Markup_Language)


