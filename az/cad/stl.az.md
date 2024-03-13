{
  "date": "2020-03-16",
  "keywords": [
"STL faylı",
"Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "STL faylları yarada və aça bilən STL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "STL fayl formatı",
  "linktitle": "STL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-st-azl"
}
},
  "lastmod": "2019-09-10"
}

## STL faylı nədir?

STL, stereolitroqrafiyanın abreviaturası, 3 ölçülü səth həndəsəsini təmsil edən dəyişdirilə bilən fayl formatıdır. Fayl formatı sürətli prototipləmə, 3D çap və kompüter dəstəkli istehsal kimi bir neçə sahədə istifadəsini tapır. O, hər bir fasetin perpendikulyar istiqamət və üçbucağın təpələrini təmsil edən üç nöqtə ilə təsvir olunduğu bir sıra kiçik üçbucaqlar kimi səthi təmsil edir. Nəticə məlumatları fabber tərəfindən qurulacaq 3D formanın en kəsiyini təyin etmək üçün proqramlar tərəfindən istifadə olunur. Rəng, tekstura və ya digər ümumi [CAD](/cad/) model atributlarının təsviri üçün STL fayl formatında heç bir məlumat yoxdur.

## Qısa tarix ##

The development of STL file format dates back to 1987. O, kommersiya 3D printerlərində istifadəsi üçün 3D Systems tərəfindən hazırlanmışdır. STL 2.0 kimi tanınan STL fayl formatının yenidən işlənmiş versiyası 2009-cu ildə fayl formatında yeniləmələrlə təklif edilmişdir.

## Fayl Formatının Xüsusiyyətləri ##

STL faylı fasetlərdən istifadə edərək səthin həndəsəsini təmsil edir. Fasetlər 3D obyektin səthini müəyyənləşdirir və unikal olaraq 1.0 uzunluğunda üçbucağa perpendikulyar olan xətt olan normal vahid və üç təpə ilə müəyyən edilir. Normal olaraq hər bir faset üçün cəmi 12 ədəd saxlanılır və hər bir təpə hər biri üç koordinatla müəyyən edilir. StL faylında heç bir miqyas məlumatı yoxdur; koordinatlar ixtiyari vahidlərdədir.

STL fayl formatının spesifikasiyası aşağıdakı iki aspektdən araşdırıla bilər.

### Fasetlərin Orientasiyası ###

Fasetin istiqaməti normal vahidin istiqaməti və təpələrin sıralanma qaydası ilə müəyyən edilir. Fasetlərin istiqaməti aşağıdakı kimi iki şəkildə müəyyən edilir:

* Normalın istiqaməti xaricədir

* Təpələr kənardan saat əqrəbinin əksinə sıralanır, sağ əl qaydasına tabedir.


### Təpədən Təpə Qaydasına ###

Bu qaydaya görə, hər üçbucaq öz bitişik üçbucağının hər biri ilə iki təpəni bölüşür. Beləliklə, bir üçbucağın təpəsi digər üçbucağın tərəfində ola bilməz.

## Fayl Formatları ##

STL ASCII-də, eləcə də kompakt fayl formatı üçün Binar təmsillərdə mövcuddur.

### STL ASCII Format ###

STL fayl formatının ASCII versiyası sadə ASCII-də yazılmışdır. Bununla belə, böyük ölçüsünə görə fayl formatı istifadə üçün üstünlük təşkil edən format kimi seçilmir. ASCII STL faylının sintaksisi aşağıdakı kimidir:
```
solid name
     facet normal ni nj nk
         outer loop
             vertex v1x v1y v1z
             vertex v2x v2y v2z
             vertex v3x v3y v3z
         endloop
     endfacet
endsolid name
```
The bold face words represent keywords that should always be lowercase. Symbols in italics are variables which are to be replaced with user-specified values.  The numerical data in the **facet normal** and **vertex** lines are single precision floats, for example, 1.23456E+789. **faset normal** koordinatının aparıcı mənfi işarəsi ola bilər; **təpə** koordinatı olmaya bilər.

### STL İkili Format ###

Binar format IEEE tam və üzən nöqtəli ədədi təmsildən istifadə edir. Fayl formatı aşağıdakı kimi təqdim olunur:

|Sahə|Məlumat|
---|---|
|Başlıq|80 simvol|
|Üçbucaqların sayı|4 baytlıq kiçik endian işarəsiz tam ədəd|
|Hər üçbucaq üçün verilənlər|12 32-bitlik üzən nöqtəli ədədlər|

Fayl formatının daha ətraflı təsviri aşağıda göstərildiyi kimidir.

```
UINT8[80] – Header
UINT32 – Number of triangles


foreach triangle
REAL32[3] – Normal vector
REAL32[3] – Vertex 1
REAL32[3] – Vertex 2
REAL32[3] – Vertex 3
UINT16 – Attribute byte count
end
```

## İstinadlar ##

* [STL Format](http://www.fabbers.com/tech/STL_Format)

* [STL - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/STL_(file_format))


