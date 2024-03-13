---
date: 2022-01-31
keywords: stp, .stp, stp file format, how to open stp files, .stp extension, stp extension
author:
  display_name: Kashif Iqbal
draft: false
toc: true
title: STP fayl formasıat
linktitle: STP
description: LSTP faylı yarada və aça bilən STP fayl formatı və API-lər haqqında qazanıns.
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## STP faylı nədir?

STP faylı CAD və CAM proqramları arasında məhsul məlumatlarının mübadiləsi üçün istifadə edilən 3D CAD faylıdır. O, 3D obyektləri haqqında məlumatı ehtiva edir və **STEP** fayl formatına bənzər şəkildə saxlanılır. STP faylları [STEP](/3d/step/) Tətbiq Protokollarına ISO 10303-2xx uyğun olaraq proqramlar arasında məlumat mübadiləsini asanlaşdırır. Bu ISO EXPRESS məlumat modelləşdirmə dilində məlumatların təqdim edilməsi üçün kodlaşdırma mexanizmini müəyyən edir. STP faylları **Autodesk Fusion 360** kimi proqramlarda açıla bilər.

## STP Fayl Format - Ətraflı Məlumat

STP faylları düz ASCII fayl formatında diskdə saxlanılır. Bunlar bu modelləri yükləmək üçün CAD/CAM proqramları tərəfindən oxuna bilən düz mətn kimi 3D model məlumatlarını ehtiva edir.

STP faylları da .step uzantısı ilə saxlanılır və qeydlər ardıcıllığından ibarətdir. Bu fayllarla bağlı diqqət çəkən xüsusiyyətlər bunlardır:

 * Simvol dəsti ISO 10646 kod nöqtələri kimi müəyyən edilir.
 * ISO-10303-21; ilk qeydin ilk simvollarıdır.
 * Şərhlər /* və */ simvolları ilə əhatə olunub.
 * Son qeyddə END-ISO-10303-21; STEP faylı 2002 versiyasına uyğundursa.
 * 2016-cı il versiyasına uyğundursa, END-ISO-10303-21;dən sonra bir və ya daha çox rəqəmsal imza ola bilər. terminator.
 * Sətir fasilələri \N\ və səhifə fasilələri \F\ ilə işarələnir.

## STP fayllarını açın

STP faylları STP Viewers-də, eləcə də Mətn Redaktorlarında aça bilər.

### STP Fayllarını STP Viewers ilə açın

Müxtəlif CAD proqramları Windows, MacOS və Linux-da baxmaq üçün STP fayllarını aça bilər. Bunlara daxildir:

 * Autodesk Fusion 360 (çarpaz platforma)
 * FreeCAD (platformalar arası)
 * IMSI TurboCAD (Windows, Mac)
 * Dassault Sistemləri CATIA (Windows, Linux)

### STP fayllarını mətn redaktorları ilə açın

STP faylları düz mətn faylları kimi saxlanılır. Bu, mətn redaktorları ilə STP fayllarını açmağa imkan verir. Windows OS-də Notepad və Notepad++ və MacOS-da Apple TextEdit kimi məşhur mətn redaktorları STP fayllarını aça bilər. Mətn redaktorunda açıldıqdan sonra istifadəçi STP faylının xüsusiyyətlərini redaktə edə bilər. Bununla belə, xassələrin səhv yenilənməsi halında faylın korlanmasına səbəb ola bilər.

## STP fayllarını necə çevirmək olar

STP fayllarını digər fayl formatlarına çevirə bilən bir neçə proqram var. STP fayllarını çevirə bilən CAD proqramlarına aşağıdakılar daxildir:

 * Autodesk Fusion 360
 * IMSI TurboCAD
 * Siemens Solid Edge

Bunlara əlavə olaraq, STP fayllarını digər fayl formatlarına çevirə bilən bir neçə onlayn proqram var. Bu onlayn proqramlar STP faylınızı bulud serverlərinə yükləməyə imkan verir, orada onlar istədiyiniz formata çevrilir və endirmək üçün geri qaytarılır.

Autodesk Fusion 360 STP fayllarını aşağıdakı 3D və CAD fayl formatlarına çevirə bilər.

 * [OBJ](/3d/obj/)
 * [3MF](/3d/3mf/)
 * [DWG](/cad/dwg/)
 * [DXF](/cad/dxf/)
 * [ASM](/cad/asm/)
 * [IGES](/cad/iges/)
 * [STL](/cad/stl/)
 * [FBX](/3d/fbx/)
 * F3D
 * [USD](/3d/usd/)

## İstinadlar

 * [ISO 10303-21 - Vikipediya](https://en.wikipedia.org/wiki/ISO_10303-21)
 * [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

