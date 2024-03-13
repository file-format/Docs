{
  "date": "2020-03-16",
  "keywords": [
"DXF faylı",
"Fayl Format",
"CAD"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "DXF faylları yarada və aça bilən DXF fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "DXF fayl formatı",
  "linktitle": "DXF",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-dx-azf"
}
},
  "lastmod": "2019-09-10"
}

## DXF faylı nədir?

DXF, Drawing Interchange Format və ya Drawing Exchange Format, AutoCAD rəsm faylının etiketlənmiş məlumat təmsilidir. Fayldakı hər bir element qrup kodu adlanan tam ədəd prefiks nömrəsinə malikdir. Bu qrup kodu əslində aşağıdakı elementi təmsil edir və verilmiş obyekt növü üçün məlumat elementinin mənasını göstərir. DXF, demək olar ki, bütün istifadəçi tərəfindən müəyyən edilmiş məlumatları rəsm faylında təmsil etməyə imkan verir.

DXF fayl formatı AutoCAD və digər proqramlar arasında məlumatların qarşılıqlı əlaqəsi üçün CAD məlumat faylı formatı kimi Autodesk tərəfindən hazırlanmışdır. Beləliklə, məlumatlar DXF fayl formatının qarşılıqlı işləmə xüsusiyyətlərinə uyğun olaraq digər formatlardan DXF-yə AutoCAD-a idxal edilə bilər.

## Qısa tarix ##


The history of DXF file format dates back to 1982 when it was introduced as part of AutoCAD 1.0. AutoCAD-in ilkin versiyaları yalnız DXF-nin ASCII fayl formatını dəstəkləyir. 1988-ci ildə AutoCAD (və yuxarıda) 10 buraxılışı ilə AutoCAD-də həm ASCII, həm də ikili DXF fayl formatı üçün dəstək təqdim edildi. Əvvəlki mərhələlərdə Autodesk heç bir fayl formatı spesifikasiyasını paylaşmırdı və buna görə DXF fayllarının düzgün idxalı asan deyildi. Bununla belə, Autodesk indi DXF spesifikasiyalarını dərc edir və geniş ictimaiyyət üçün əlçatandır.

## Fayl Formatının Xüsusiyyətləri ##

DXF fayl formatı məzmunu bölmələrə ayırmaq üçün qrup kodu və dəyər cütlərindən istifadə edir. Hər bölmə hər bir qeyd qrup kodu və məlumat elementindən ibarət olan qeydlərdən ibarətdir. Hər qrup kodu və dəyəri DXF faylında öz sətirindədir. Hər bölmə qrup kodu 0 və ardınca SECTION sətri ilə başlayır. Bundan sonra qrup kodu 2 və bölmənin adını göstərən sətir gəlir (məsələn, BÖLMƏ1). Hər bir bölmə onun elementlərini müəyyən edən qrup kodlarından və dəyərlərdən ibarətdir. Bölmə 0 və ardınca ENDSEC sətri ilə bitir.

DXF fayl formatı obyektlərdən fərqli obyektləri nəzərdən keçirir. Burada obyektlərin qrafik təsviri yoxdur, lakin obyektlər var. Beləliklə, DXF-dəki girişlər qrafik obyektlər, obyektlər isə qeyri-qrafik obyektlər adlanır. DXF faylının BLOCK və ENTITIES bölmələrində Varlıqlar var və bu iki bölmədə qrup kodlarının istifadəsi eynidir. Müəssisənin sonu növbəti obyekti başlayan və ya bölmənin sonunu göstərən növbəti 0 qrupu ilə göstərilir.

### Fayl strukturu ###

DXF faylında bölmələr aşağıdakı ardıcıllıqla düzülür:

|Section|Basic description
---|---|
|Başlıq|Bu bölmədə rəsm haqqında ümumi məlumat var. Bu, çertyoj və onunla əlaqəli dəyərlərlə əlaqəli müxtəlif dəyişənləri ehtiva edən telefonunuzdakı Parametrlər funksiyasına bənzəyir. Məsələn, Başlıq bölməsi DXF faylının hansı AutoCAD versiyasını ($ACADVER dəyişəni) və ya fayldakı bucaqları ölçmək üçün istifadə olunan vahidi ($AUNITS dəyişəni) təyin edəcək.
|Siniflər|SİNİFLƏR bölməsi verilənlər bazasının BLOKLAR, MÜƏSSİSƏLƏR və OBYEKT bölmələrində nümunələri görünən tətbiq tərəfindən müəyyən edilmiş siniflər üçün məlumatı özündə saxlayır.
|Cədvəllər|Bu bölmədə bir neçə fərqli cədvəl üçün təriflər var, onların hər biri bir sıra müxtəlif simvol girişlərini ehtiva edir. Məsələn, [line type](https://help.autodesk.com/view/ACD/2016/ENU/?guid=GUID-20B4D4B3-1220-426A-847B-5BBE36EC6FDF) cədvəli (LTYPE) DXF faylındakı tire, nöqtə, mətn və simvolların nümunəsini və onların necə ölçüləndiyini müəyyən edir. Bu bölmədə tapılan cədvəllərin tam siyahısı:<ul><li> Tətbiq ID (APPID) cədvəli</li><li> Blok Qeydi (BLOCK_RECORD) cədvəli</li><li> Ölçü Stili (DIMSTYPE) cədvəli</li><li> Layer (LAYER) cədvəli</li><li> Linettype (LTYPE) cədvəli</li><li> Mətn üslubu (STYLE) cədvəli</li><li> İstifadəçi Koordinat Sistemi (UCS) cədvəli</li><li> Cədvələ bax (VIEW).</li><li> Viewport konfiqurasiyası (VPORT) cədvəli</li></ul>
|Bloklar|Bu bölmə rəsmdəki hər bir blok istinadını təşkil edən qrafik obyektləri və çertyoj obyektlərini ehtiva edir.
|Şəxslər|Bu bölmədə rəsmin faktiki obyekt məlumatı və qrafik obyektləri var. Buraya xam məlumatlar daxil ola bilər – məsələn, çevrə obyekti qalınlığı, mərkəz nöqtəsi, radiusu və ekstruziya istiqaməti ilə müəyyən edilir.
|Obyektlər|Burada rəsmin qeyri-qrafik hissələrini tapa bilərsiniz. Məsələn, burada AutoCAD lüğətləri saxlanılır.

## İstinadlar ##

* [DXF File Specifications](http://images.autodesk.com/adsk/files/autocad_2012_pdf_dxf-reference_enu.pdf)
* [Vikipediya tərəfindən AutoCAD DXF](https://en.wikipedia.org/wiki/AutoCAD_DXF)


