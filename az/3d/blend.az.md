{
  "date": "2023-04-13",
  "keywords": [
"qarışdırma faylı",
"qarışıq faylı nədir",
"qarışıq faylını necə açmaq olar",
"fayl",
"fayl uzantısını qarışdırın",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "BLEND Fayl Formatı - Blender 3D Faylı",
  "description": "BLEND faylları yarada və aça bilən BLEND formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "BLEND",
  "menu": {
    "docs": {
      "identifier": "3d-blend-az",
      "parent": "3d"
}
},
  "lastmod": "2023-04-13"
}

## BLEND faylı nədir?

Qarışıq faylı geniş istifadə olunan 3D modelləşdirmə və animasiya proqramı olan Blender tərəfindən istifadə edilən fayl formatıdır. Bu, 3D modellər, materiallar, fakturalar, animasiyalar və s. daxil olmaqla 3D səhnə ilə bağlı bütün məlumatları saxlamaq və saxlamaq üçün Blender tərəfindən istifadə olunan standart fayl formatıdır.

Qarışıq fayl formatı məlumatları iyerarxik strukturlar şəklində təşkil edən və saxlayan ikili fayldır. Bu iyerarxik strukturlar 3D səhnədəki obyektlər və onların xassələri haqqında məlumatları ehtiva edir. 3D səhnə arasındakı əlaqə də bu fayllarda saxlanılır. Bütün bu məlumatlar Blender tərəfindən səhnəni real vaxt rejimində göstərmək üçün istifadə olunur. Qarışıq faylı həmçinin Blender tərəfindən onu Collada, FBX, OBJ və s. kimi digər fayl formatlarına ixrac etmək üçün istifadə edilə bilən məlumatları ehtiva edir.

Qarışıq faylları bir sıra üstünlüklər təklif edir, çünki onlar istifadəçilərə layihə ilə bağlı bütün məlumatları bir yerdə saxlamağa imkan verir, başqaları ilə əməkdaşlıq və ya paylaşma prosesini sadələşdirir. Onlar həmçinin nisbətən kiçik ölçülərə malikdirlər və yığcam ölçüləri saxlama və köçürmə zamanı daşıma qabiliyyətini və rahatlığını artırır.

## Blend File Format - Ətraflı Məlumat

Blender qarışdırma fayllarını idarə etmək və saxlamaq üçün bir neçə variant təqdim edir. İstifadəçilər öz fayllarını layihə ilə əlaqəli bütün məlumatları əhatə edən vahid qarışıq faylı kimi saxlamağı seçə bilərlər. Alternativ olaraq, istifadəçilər öz layihələrini hər biri layihənin xüsusi aspektinə yönəldilmiş çoxsaylı qarışıq faylları kimi saxlaya bilərlər. Bundan əlavə, Blender istifadəçilərə digər qarışıq fayllarından məlumatları cari layihələrinə əlavə etmək və ya əlaqələndirmək imkanı verir. Bu xüsusiyyət layihə üzərində başqaları ilə işləyərkən faydalı ola bilər.

Blender-də qarışıq faylları ilə işləyərkən, istifadəçilər icazəsiz girişin və ya onlarda olan məlumatların dəyişdirilməsinin qarşısını almaq üçün onları parolla qorumaq imkanına malikdirlər. Bu, həssas və ya məxfi məlumatların qorunması üçün faydalı ola bilər.

Qarışıq faylı aşağıdakıları əhatə edən 3D səhnəyə aid bütün məlumatları saxlayır:

- 3D modellər: Qarışıq faylı Blenderdə yaradılmış bütün 3D modelləri saxlayır. Buraya mesh həndəsəsi, səth teksturaları və digər əlaqəli məlumatlar daxildir.
- Materiallar: Səhnədəki 3D modellərlə əlaqəli materiallar qarışıq faylında saxlanılır. Bu materiallar işığın səhnədəki obyektlərin səthləri ilə necə qarşılıqlı əlaqədə olduğunu təsvir edir.
- Dokular: 3D modellərin səthlərinə tətbiq olunan teksturalar da qarışıq faylında saxlanılır.
- Python skriptləri: Səhnənin yaradılmasında istifadə edilmiş Python skriptləri də qarışıq faylında saxlanıla bilər.
- Animasiyalar: Blender daxilində yaradılmış istənilən animasiya qarışıq faylında saxlanılır. Bura əsas kadrlar, vaxt məlumatları və animasiya ilə bağlı digər məlumatlar daxildir.
- İşıqlandırma: Səhnədəki işıqlandırma haqqında məlumat, o cümlədən işıqların növü, mövqeyi və rəngi qarışıq faylında saxlanılır.
- Kamera haqqında məlumat: 3D səhnəni çəkmək üçün istifadə edilən kamera haqqında onun mövqeyi, oriyentasiyası və baxış sahəsi kimi məlumatlar da qarışıq faylında saxlanılır.
- Səhnə parametrləri: Render həlli, göstərmə parametrləri və s. kimi digər səhnə parametrləri də qarışıq faylında saxlanılır.

## BLEND faylını necə açmaq olar?
Siz Blenderi işə salaraq, sonra Fayl menyusuna klikləyərək və açılan menyudan Açıq seçimini etməklə BLEND faylını aça bilərsiniz. Alternativ olaraq, siz sadəcə olaraq qarışdırma faylını Blender proqramına sürükləyib buraxa bilərsiniz və o, qarışdırma faylını açacaq.

## İstinadlar
* [Blender (software)](https://en.wikipedia.org/wiki/Blender_(software))
