{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "OAM Faylı - Adobe Edge Animate Widget Fayl Formatı",
  "description" : "OAM faylının nə olduğunu və OAM faylını yarada və aça bilən API-lər haqqında öyrənin.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam-az",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## OAM faylı nədir?

A .oam file a an animated widget file exported from Adobe Edge Animate Widget. Animations exported as OAM widget file format can be inserted into other Adobe applications such as InDesign Documents ([INDD file](/page-description-language/indd/), Dreamweaver, and Muse. OAM files are like deployment packages that can be readily inserted into other Adobe's projects to make use of them. OAM files contain information about the animation's assets, behaviors, and actionscript code. You can create an OAM file by publishing an Adobe Animate project [.AN file](/web/an/).
İstifadəçilər Edge Animate layihəsindən (.AN faylı) dərc etməklə OAM faylları yarada bilərlər.

## OAM Fayl Formatı

OAM faylı diskdə sıxılmış [ZIP](/compression/zip/) arxivi kimi saxlanılır. Bu o deməkdir ki, siz fayl uzantısının adını .zip olaraq dəyişdirə və WinZIP və ya WinRAR kimi istənilən sıxılma yardım proqramı ilə çıxara bilərsiniz. Azaldılmış fayl ölçüsü animasiyanı internet üzərindən digər istifadəçilərlə ötürməyi və paylaşmağı asanlaşdırır.

### OAM Fayl Strukturu

.oam faylının daxili fayl strukturu özəldir və Adobe tərəfindən açıq şəkildə sənədləşdirilmir. Bununla belə, məlumdur ki, .oam faylları bir faylda paketlənmiş fayl və resurslar toplusunu (məsələn, qrafika, audio və ActionScript kodu) ehtiva edir. .oam faylının məzmununa [XML](/web/xml/) faylları, SWF faylları və digər resurs faylları daxil ola bilər. .oam faylının dəqiq strukturu onu yaratmaq üçün istifadə olunan Adobe Animate-in xüsusi versiyasından, həmçinin fayla daxil olan animasiya və aktivlərin növündən asılıdır.

OAM faylı aşağıdakı məlumatları ehtiva edir.

`Aktivlər:` Animasiyada istifadə olunan qrafika, audio və video aktivləri haqqında məlumat.

`Davranışlar:` Animasiyada baş verən hərəkətlərin və qarşılıqlı təsirlərin təsviri.

`ActionScript kodu:` Animasiyanın davranışını və interaktivliyini idarə etmək üçün istifadə edilən kod.

`Parametrləri dərc et:` HTML5 və ya AIR kimi animasiyanın dərc ediləcəyi platforma və format haqqında məlumat.

`Metadata:` Additional information such as the animation's author, creation date, and version number.

## OAM faylını necə açmaq olar?

OAM fayllarını açmaq üçün aşağıdakı proqramlardan istifadə edə bilərsiniz.

 * Adobe Edge Animate CC (İstehsalı dayandırılıb)
 * Adobe Animate 2023
 * Adobe InDesign 2023
 * Adobe Dreamweaver 2021

## İstinadlar

* [OAM Nəşriyyatı](https://helpx.adobe.com/animate/using/OAM-publishing.html)


