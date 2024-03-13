{
  "date": "2023-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LAS - Lidar LASer Fayl Format",
  "description": "LAS fayl formatı və LAS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "LAS",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-la-azs"
}
},
  "lastmod": "2023-07-18"
}

## LAS faylı nədir?

LAS (Lidar LASer) fayl formatı lidar nöqtəsi bulud məlumatlarını saxlamaq üçün xüsusi olaraq hazırlanmış ikili fayl formatıdır. O, Amerika Fotoqrammetriya və Uzaqdan Zondlama Cəmiyyəti (ASPRS) tərəfindən lidar məlumat mübadiləsi və qarşılıqlı fəaliyyət üçün standartlaşdırılmış format kimi hazırlanmış və saxlanılır.

LAS faylları fərdi lidar nöqtələri, o cümlədən onların 3D koordinatları (x, y və z), intensivlik dəyərləri, təsnifat kodları və əlavə atributlar haqqında ətraflı məlumatı saxlayır. Bu format həm diskret qayıdış, həm də tam dalğa formalı lidar məlumatlarını dəstəkləyir və lazer impulsuna görə çoxlu qaytarmaların saxlanmasına imkan verir.

## LAS fayl formatı

LAS faylının strukturu üç əsas bölmədən ibarətdir: fayl başlığı, dəyişən uzunluq qeydləri (VLR) və nöqtə məlumat qeydləri.

1. Fayl başlığı: Fayl başlığı məlumat formatının versiyası, nöqtə məlumat formatı, nöqtələrin sayı, sərhəd qutusu koordinatları, koordinat istinad sistemi (CRS) və digər metadata kimi LAS faylı haqqında vacib məlumatları ehtiva edir. Bu faylda olan lidar məlumatlarının xülasəsini təqdim edir.

2. Variable Length Records (VLRs): VLRs are optional and can store additional metadata and custom information about the lidar data. VLRs allow for flexibility in extending the format to accommodate specific user requirements. Examples of VLRs include information about the sensor system, data processing parameters, or classification schemes.

3. Nöqtə məlumat qeydləri: Nöqtə məlumat qeydləri faktiki lidar ölçmələrini saxlayır. Hər bir nöqtə məlumat qeydi tək bir lidar nöqtəsini təmsil edir və x, y və z koordinatları, intensivlik dəyərləri, təsnifat kodları (məsələn, torpaq, bitki örtüyü, binalar) və digər istifadəçi tərəfindən müəyyən edilmiş atributlar kimi atributları ehtiva edir. Nöqtə qeydləri həmçinin vaxt ştamplarını, geri saymalarını və skan bucaqlarını saxlaya bilər.

LAS faylları müxtəlif növ lidar məlumatlarını və tələb olunan məlumat səviyyəsini yerləşdirmək üçün müxtəlif məlumat formatlarını (0-dan 10-a qədər) dəstəkləyir. Məsələn, 0 formatı əsas məlumatlarla sadə nöqtə formatını təmsil edir, 1-dən 3-ə qədər formatlar isə hər qayıdış üçün dalğa forması məlumatı daxil olmaqla daha əhatəli məlumat təqdim edir.

LAS faylları lidar proqram təminatı və emal alətləri tərəfindən geniş şəkildə dəstəklənir, bu da onları lidar məlumat mübadiləsi və təhlili üçün standart formata çevirir. Bundan əlavə, LAS faylları orijinal məlumatların etibarlılığını qoruyarkən fayl ölçüsünü azaltmaq üçün itkisiz sıxılma üsullarından istifadə edərək sıxıla bilər. LAS fayllarının sıxılmış versiyası tez-tez LAZ adlanır ki, bu da səmərəli saxlama və məlumat ötürmə imkanları təklif edir.

## İstinadlar

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
