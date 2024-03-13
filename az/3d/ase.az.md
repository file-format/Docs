{
  "date": "2021-01-22",
  "keywords": [
"ASE",
"fayl",
"format",
"fayl növü",
"uzadılması",
"ASE faylı nədir?"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "ASE fayl formatı və ASE fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "title": "ASE - Autodesk ASCII Scene Export File",
  "linktitle": "ASE",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-as-aze"
}
},
  "lastmod": "2021-01-22"
}

## ASE faylı nədir?

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## ASE Fayl Format - Ətraflı Məlumat

ASE faylları ASCII formatında saxlanılan və istənilən mətn redaktorunda açıla bilən mətn fayllarıdır. ASE faylı Autodesk tərəfindən təmin edilən aşağıdakı məlumat növlərini ehtiva edə bilər.

### Çıxış Seçimləri

 * `Mesh Definition` - Həndəsi obyektlər üçün təpə və üz məlumatları daxil olmaqla, hər bir şəbəkənin tərifini ixrac edir. Bundan əlavə, bunun yandırılması aşağıda təsvir edilən Mesh Seçimləri qrup qutusundakı elementləri aktivləşdirir.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * `Transform Animation Keys` - Obyektlər üçün transformasiya animasiya məlumatlarını ehtiva edir. Obyekt hədəf kamera və ya diqqət mərkəzidirsə, bura hədəf animasiya datası daxil olacaq.
 * `Animated Mesh` - Hər n çərçivənin tam mesh tərifini ixrac edir. Tezlik aşağıda təsvir edilən Controller Output spinner tərəfindən müəyyən edilir. Hər bir blok aşağıda təsvir edilən Mesh Options qrup qutusunda göstərilən eyni məlumatları ehtiva edir. Bunu yandırmaq, hətta kiçik səhnələr üçün də böyük bir faylla nəticələnə bilər.
 * `Animasiyalı Kamera/İşıq Parametrləri` - Kameralar və işıqlar üçün rəng, intensivlik, azalma, xəritə meyli və s. kimi animasiya məlumatlarını ixrac edir. Nəzarətçi Çıxış spinneri tərəfindən müəyyən edildiyi kimi hər n çərçivədən bir blok çıxarır.
 * `Ters Kinematik Qovşaqlar` - İyerarxiya bölməsində IK birləşmə parametrlərini ixrac edir.

### Obyekt növləri

Buradakı elementlər çıxışa hansı obyektin kateqoriyasını daxil etmək istədiyinizi müəyyən etməyə imkan verir. Siz həndəsi obyektləri, formaları, kameraları, işıqları və köməkçi obyektləri daxil edə bilərsiniz.

 * Həndəsi
 * Formalar
 * Kameralar
 * İşıqlar
 * Köməkçilər

### Mesh Seçimləri

 * `Mesh Normals` - Üz və təpə normallarını ixrac edir. Əvvəlcə üzün normalı, sonra isə üzü dəstəkləyən üç təpənin normalları siyahıya alınır. Bunun yandırılması daha böyük bir faylla nəticələnir.
 * `Mapping Coordinates` - 3ds Max Proqram İnkişafı Kitində təsvir edilən TVert və TVFace strukturlarına uyğun olaraq xəritəçəkmə təpələri və üzlərinin siyahısını ixrac edir. Obyekt üz xəritəsindən istifadə edərsə, hər bir üz üçün UVW koordinatlarından ibarət üz xəritəsi siyahısı ixrac edilir.
 * `Vertex Colors` - Təpə rənglərini ixrac edir.

### Nəzarətçinin çıxışı

 * `Use Keys` - Əsas dəyərləri ixrac edir. Nəzarətçi düymələrdən istifadə etmirsə, Force Sample metodu istifadə olunur. Transformasiya nəzarətçiləri vəziyyətində Açarlardan İstifadə seçimi yalnız bütün transformasiya nəzarətçiləri ya Xətti/TCB, ya da Bezier olduqda işləyir. Transformasiya yollarından biri fərqli növ nəzarətçidən istifadə edirsə, o zaman bütün transform trekləri üçün Force Sample metodu istifadə olunur.
 * `Qüvvət Nümunələri` - Nümunə Nəzarət Cihazı üzrə Çərçivələrdə göstərilən tezliyə əsaslanan Nümunələr nəzarətçi dəyərləri.

## İstinadlar

 * [Autodesk - ASCII-yə ixrac](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)

