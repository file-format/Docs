{
  "date": "2021-05-24",
  "keywords": [
"xul",
"Fayl",
"Uzatma",
"Fayl Format",
"Fayl uzadılması",
"XML İstifadəçi İnterfeysi Dili"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XUL - XML İstifadəçi İnterfeysi Dil Faylı",
  "description": "XUL faylları yarada və aça bilən XUL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "XUL",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-xu-azl"
}
},
  "lastmod": "2021-05-24"
}

## XUL faylı nədir?

.xul genişləndirilməsi olan fayl ([XUL](https://wiki.mozilla.org/XUL:Home_Page) XML İstifadəçi İnterfeysi Dili deməkdir) istifadəçi interfeysləri yaratmaq üçün [XML](/web/xml/) əsaslı işarələmə dili faylıdır. O, veb-səhifələrin yaradılması üçün istifadə olunan digər işarələmə dillərinə bənzər qrafik istifadəçi interfeysi elementləri yaratmaq üçün tərtibatçılar üçün Mozilla tərəfindən hazırlanmışdır. XUL, Mozilla kod bazasından istifadə etdiyi Firefox brauzerində Mozilla tərəfindən geniş şəkildə istifadə edilmişdir. XUL renderindən istifadə etməklə həyata keçirilir
[Gecko engine](https://en.wikipedia.org/wiki/Gecko_(software)). Pale Moon, Basilisk və Waterfox kimi Firefox çəngəlləri XUL əlavələri üçün dəstəyi saxlayır. XUL faylları MIME növü ilə müəyyən edilir: application/vnd.mozilla.xul+xml.

## XUL fayl formatı

XUL faylları XML fayl formatına əsaslanan düz mətnlə yazılır və Gecko mühərrikindən istifadə etməklə göstərilir. XUL strukturunun üç əsas hissəsi bunlardır:

 * `Məzmun` - Bura pəncərənin bəyannamələri və onların daxilində olan istifadəçi interfeysi elementləri daxildir.
 * `Dəri` - Buraya istənilən üslub cədvəlləri, şəkillər və digər mövzu ilə bağlı fayllar daxildir. Pəncərənin görünüşü stil vərəqlərində təsvir edilmişdir.
 * `Yerli` - Pəncərədə göstərilən mətn ayrıca saxlanılır və istifadəçilər tərəfindən çoxlu dil faylları dəsti istifadə edilə bilər.

### XUL Nümunəsi

Aşağıdakı nümunə şaquli istiqamətdə bir-birinin üstünə yığılmış üç düymə yaradır.

```
<?xml version="1.0"?>
<?xml-stylesheet href="chrome://global/skin/" type="text/css"?>

<window id="vbox example" title="Example 3...."
xmlns="http://www.mozilla.org/keymaster/gatekeeper/there.is.only.xul">
  <layout>
    <button id="yes1" label="Yes"/>
    <button id="no1" label="No"/>
    <button id="maybe1" label="Maybe"/>
  </layout>
</window>
```

## İstinadlar

* [XUL - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/XUL)

* [XUL Arxiv Sənədi - Mozilla tərəfindən](https://wiki.mozilla.org/XUL:Home_Page)


