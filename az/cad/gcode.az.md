{
   "date":"2023-12-20",
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"GCODE Fayl - .gcode faylı nədir və onu necə açmaq olar?",
   "description":"GCODE fayl formatı və GCODE faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
   "linktitle":"GCODE",
   "menu":{
      "docs":{
         "identifier":"cad-gcode-az",
         "parent":"cad"
}
},
   "lastmod":"2023-12-20"
}

## GCODE faylı nədir?

**GCODE faylı** kompüterləşdirilmiş dəzgahlara və 3D printerlərə nəzarət etmək üçün təlimatları ehtiva edən düz mətn faylıdır; G-kodu və ya Həndəsi Kod, **CNC (Kompüter Rəqəmsal Nəzarət)** maşınlarının hərəkətlərini və hərəkətlərini idarə etmək üçün istifadə edilən dildir; CNC maşınlarına freze maşınları, tornalar, marşrutlaşdırıcılar və 3D printerlər daxildir.

G kodu əmrləri adətən hərf və rəqəmlərdən ibarət olan xüsusi sintaksisdə yazılır; hər bir əmr maşına aləti müəyyən bir mövqeyə köçürmək, aləti dəyişdirmək və ya sürəti tənzimləmək kimi xüsusi hərəkətləri yerinə yetirməyi tapşırır.

G-kodu çox vaxt **CAM (Kompüter Dəstəkli İstehsalat)** proqram təminatı ilə yaradılır; CAM proqramı 3D model və ya 2D dizaynı götürür və müvafiq alət yollarını və G kodu təlimatlarını yaradır; G-kod faylı daha sonra icra üçün CNC maşınına və ya 3D printerə yüklənir.

G-kod faylları adətən .nc və ya .gcode fayl uzantısına malikdir, məsələn, program.nc və ya print.gcode.

## GCODE Fayl Strukturu:

GCODE faylları hər bir sətirdə xüsusi əmrdən ibarət düz mətn fayllarıdır; bu əmrlər maşının hərəkətinə nəzarət etməkdən tutmuş temperaturun, sürətin və obyektin hazırlanması üçün vacib olan digər parametrlərin tənzimlənməsinə qədər dəyişir.

GCODE sintaksisi hərf və rəqəmlərin birləşməsini əhatə edir; hər biri fərqli hərəkət və ya parametri təmsil edir; ümumi əmrlərə hərəkət üçün G0 və G1, mili idarə etmək üçün M3 və M5, sürət və qidalanma sürətinin tənzimlənməsi üçün S və F daxildir.

## GCODE Yaradılması:

**Simplify3D** və **Slic3r** kimi dilimləmə proqramı Kompüter Dəstəkli Dizayn (CAD) çertyojlarını GCODE-a tərcümə edir; CAD proqram təminatı 3D modelləri yaratmaq üçün istifadə olunur, sonra STL kimi formatlarda ixrac edilir; dilimləmə proqramı bu modelləri götürür və təbəqənin hündürlüyü, çap sürəti və temperatur parametrləri kimi təfərrüatları göstərən GCODE faylı yaradır.

## GCODE Nümunəsi

CNC maşınını hərəkət etdirmək üçün G kodunun sadə nümunəsi:

```
G0 X10 Y5      ; Rapid move to position X=10, Y=5
G1 Z2 F500     ; Linear move to Z=2 at feed rate of 500 units/minute
M3 S1000       ; Start spindle at 1000 RPM
G2 X20 Y10 I2 J0   ; Clockwise circular interpolation
G0 Z5          ; Rapid move to Z=5
M5             ; Stop spindle
```

## GCODE faylını necə açmaq olar?

G-kod faylını açmaq üçün ehtiyaclarınızdan asılı olaraq müxtəlif növ proqramlardan istifadə edə bilərsiniz.

3D printer üçün G kodu yaratmısınızsa; onu 3D printeriniz və ya xüsusi dilimləmə proqramı ilə birlikdə gələn proqram təminatından istifadə edərək aça bilərsiniz; misallara **PrusaSlicer**, **Cura**, **Simplify3D**, **MatterControl** və ya **Repetier-Host** daxildir; bu proqramlar tez-tez G kodunu yükləməyə və vizuallaşdırmağa imkan verən istifadəçi dostu interfeysə malikdir.

GCODE faylları düz mətndir, ona görə də onları istənilən mətn redaktoru ilə aça bilərsiniz; ümumi mətn redaktorlarına **Notepad (Windows-da)**, **TextEdit (macOS-da)** və ya **Gedit (Linux-da)** daxildir; sadəcə olaraq **G-kod faylına sağ klikləyin**, **Birlikdə aç** seçin və mətn redaktoru seçin.

