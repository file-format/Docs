{
  "date": "2019-12-12",
  "keywords": [
"GLTF",
"fayl",
"uzadılması",
"format",
"3D",
"Khronos qrupu 3D"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "GLTF faylları yarada və aça bilən GLTF faylları və API-lər haqqında məlumat əldə edin.",
  "title": "GLTF - GL Transmissiya Fayl Format",
  "linktitle": "GLTF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-glt-azf"
}
},
  "lastmod": "2019-09-10"
}

## GLTF faylı nədir?

glTF (GL Transmission Format) 3D model məlumatlarını JSON formatında saxlayan 3D fayl formatıdır. JSON-un istifadəsi həm 3D aktivlərin ölçüsünü, həm də həmin aktivləri qablaşdırmadan çıxarmaq və istifadə etmək üçün lazım olan iş vaxtı emalını minimuma endirir. 3D səhnələrin və modellərin tətbiqlər tərəfindən səmərəli ötürülməsi və yüklənməsi üçün qəbul edilmişdir. glTF Khronos Group 3D Formatlar İşçi Qrupu tərəfindən hazırlanmışdır və yaradıcıları tərəfindən 3D-nin [JPEG](/image/jpeg/) kimi təsvir edilmişdir.

GLTF fayl formatı 3D məzmun alətləri və xidmətləri üçün genişləndirilə bilən, ümumi nəşr formatını müəyyən edir ki, bu da müəlliflik iş axınlarını asanlaşdırır və bütün sənaye üzrə məzmundan qarşılıqlı istifadəyə imkan verir. glTF fayl formatının yaradılmasının məqsədi 3D məzmun alətləri və xidmətləri üçün genişləndirilə bilən, ümumi nəşriyyat formatını müəyyən etmək idi ki, bu da müəlliflik iş axınlarını sadələşdirməli və bütün sənaye üzrə məzmunun qarşılıqlı istifadəsini təmin etməlidir. WebGL və digər API-lərdən istifadə edən proqramlar tərəfindən iş vaxtının işlənməsini minimuma endirir.

## GLTF Faylının Qısa Tarixi

The first specifications for glTF file format 1.0 were announced in October 2015. Bu, Khronos tərəfindən 2012-ci ilin martında başlayan bir sıra səylər kimi gəldi. Bu səylərin məqsədi WebGL dartma ətrafındakı imkanları qiymətləndirmək idi. Nəticədə, JSON formatına əsaslanan glTF formatının ilk demosu 2012-ci ildə WebGl görüşündə təqdim olundu. Bu format vaxtaşırı Cesium, 3D Tiles, Oculus, Microsoft, Archilogic və başqaları da daxil olmaqla bir neçə şirkət tərəfindən qəbul edildi.

glTF 2.0 5 iyun 2017-ci ildə Web3D 2017 Konfransında nəşr olundu. Bundan sonra glTF fayl formatını qəbul edən şirkətlərin uzun bir siyahısı var.

## GLTF fayl formatı

glTF 2.0 üçün fayl formatı spesifikasiyaları istinad üçün [online](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0) mövcuddur və glTF fayl formatının dəstəklənməsi üçün oxumaq/yazma ilə bağlı istənilən tətbiqdə məsləhətləşmək lazımdır.

glTF aktivləri xarici məlumatları dəstəkləyən JSON faylları kimi müəyyən edir. O, aşağıdakıların köməyi ilə 3D modelləri təmsil edir:

* Full scene description contained in a JSON-formatted .glTF file that includes information about node hierarchy, materials, cameras, as well as descriptor information for meshes, animations and other constructs
* Həndəsə və animasiya məlumatlarını və digər bufer əsaslı məlumatları ehtiva edən ikili fayllar (.bin).

* Dokular üçün şəkil faylları ([.jpg](/image/jpeg/), [.png](/image/png/))


Şəkillər kimi hər hansı xarici aktivlər URI vasitəsilə istinad edilən xarici fayllarda saxlanılır. Bu URI-lər GLB konteynerinin yanında saxlanılır və ya data URI-lərindən istifadə edərək birbaşa JSON-a daxil edilir. Hər bir etibarlı glTF öz versiyasını göstərməlidir.

glTF kiçik fayl ölçüsü, sürətli yükləmə, tam 3D səhnə təsviri və genişlənmə qabiliyyətinə nail olmaq üçün nəzərdə tutulmuşdur. Bu unikal dizayn məqsədləri 3D domenində glTF fayl formatının populyarlığının əsas səbəbləridir. Müxtəlif fayl növləri üçün glTF fayl formatı tərəfindən dəstəklənən mim növləri aşağıdakılardır:

* .gltf faylları model/gltf+json istifadə edir

* .bin faylları proqram/oktet axınından istifadə edir

* Tekstura faylları xüsusi şəkil formatına əsaslanan rəsmi şəkil/* növündən istifadə edir. Müasir veb-brauzerlərlə uyğunluq üçün aşağıdakı şəkil formatları dəstəklənir: image/jpeg, image/png.


### JSON Kodlaşdırma

glTF JSON fayl formatına əlavə məhdudiyyətlər qoyur

Müştəri tərəfində tətbiqi sadələşdirmək üçün glTF-də JSON formatı və kodlaşdırma ilə bağlı əlavə məhdudiyyətlər var.

1. JSON BOM olmadan UTF-8 kodlamasından istifadə etməlidir.
1. Bu spesifikasiyada müəyyən edilmiş bütün sətirlər (xüsusiyyət adları, nömrələr) yalnız ASCII simvol dəstindən istifadə edir və düz mətn kimi yazılmalıdır, məsələn, `\u0062\u0075\u0066\u0066\u0065\u0072` əvəzinə bufer.
1. JSON obyektlərindəki adlar (açarlar) unikal olmalıdır, yəni dublikat açarlara icazə verilmir.

### URI

Buferlərə və Şəkil resurslarına URI-lər vasitəsilə istinad edilir. Aşağıdakı iki URI növü müştərilər tərəfindən dəstəklənməlidir.

**Data URI-ləri:** Data URI-ləri RFC 2397 tərəfindən müəyyən edildiyi kimidir və resursları JSON-a daxil etmək üçün glTF tərəfindən istifadə olunur.

**Relative URI Paths:** or path-noscheme as defined by RFC 3986, [Section 4.2](https://datatracker.ietf.org/doc/html/rfc3986#section-4.2) — without scheme, authority, or parameters. Reserved characters must be percent-encoded, per RFC 3986, [Section 2.2](https://datatracker.ietf.org/doc/html/rfc3986#section-2.2).

## İstinadlar ##

* [glTF 2.0 Spesifikasiyalar - Khronos](https://github.com/KhronosGroup/glTF)

* [glTF Fayl Formatı - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/GlTF)


