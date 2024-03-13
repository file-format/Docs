{
  "date" : "2019-12-03",
  "keywords" : [ "GLB","file", "format", "file type", "extension","what is an GLB file?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "GLB",
  "description":"GLB fayl formatı və GLB fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "linktitle" : "GLB",
  "menu" : {
    "docs" : {
      "identifier":"3d-glb-az",
      "parent" : "3d"
}
},
  "lastmod" : "2020-09-01"
}

## GLB faylı nədir?

GLB GL Transmissiya Formatında ([glTF](/3d/gltf/)) saxlanılan 3D modellərin ikili fayl formatı təmsilidir. İkili formatda node iyerarxiyası, kameralar, materiallar, animasiyalar və şəbəkələr kimi 3D modellər haqqında məlumat. Bu ikili format glTF aktivini (JSON, .bin və şəkillər) binar blobda saxlayır. O, həmçinin glTF halında baş verən fayl ölçüsünün artması probleminin qarşısını alır. GLB fayl formatı kompakt fayl ölçüləri, sürətli yükləmə, tam 3D səhnə təsviri və gələcək inkişaf üçün genişlənmə ilə nəticələnir. Format MIME növü kimi model/gltf-binary istifadə edir.

## GLB Fayl Format - Ətraflı Məlumat

glTF tərəfindən istifadə edilən məzmunun çatdırılma üsulları baza-64 kodlu ikili verilənlərin deşifrə edilməsi üçün əlavə emal ilə nəticələnir və həmçinin fayl ölçüsünü 33% artırır. GLB fayl formatının formalaşmasına töhfə verən bu çatdırılma üsullarına aşağıdakılar daxildir:

* glTF JSON xarici binar məlumatlara (həndəsə, əsas çərçivələr, dərilər) və şəkillərə işarə edir.

* glTF JSON data URI-lərindən istifadə edərək base64 kodlu ikili verilənləri və daxili şəkilləri daxil edir.


Konteyner formatı kimi GLB, glTF-nin yaratdığı problemlərin qarşısını almaq üçün glTF aktivinin binar blobda təmsil olunması üçün ikili fayl formatı kimi təqdim edilmişdir. GLB fayl formatı [specifications](https://github.com/KhronosGroup/glTF/tree/main/specification/2.0#glb-file-format-specification) tətbiqlərin inkişafı üçün eyni olan hər hansı bir oxucu/yazıçı tətbiqi üçün istinad edilməlidir.

## GLB fayl strukturu

GLB fayl formatı kiçik endian-a əsaslanır və onun strukturu onu ehtiva edir:

* Başlıq adlı 12 baytlıq preambula.

* JSON məzmunu və ikili verilənləri ehtiva edən bir və ya bir neçə parça.


#### GLB Başlığı

GLB fayl formatının başlığı üç 4 baytlıq girişdən ibarətdir:

* uint32 magic - sehr 0x46546C67-ə bərabərdir. Bu ASCII sətir glTF-dir və məlumatları Binary glTF kimi müəyyən etmək üçün istifadə edilə bilər

* uint32 versiyası - Binary glTF konteyner formatının versiyasını göstərir

* uin32 uzunluğu - Başlıq və baytdakı bütün parçalar daxil olmaqla Binary glTF-in ümumi uzunluğu


#### Parçalar

GLB faylındakı hər bir parça aşağıdakı quruluşa malikdir:

|uint32|uint32|ubyte[]
---|---|---|
|chunkLength|chunkType|chunkData

* `chunkLength` - chunkData-nın baytla uzunluğu

* `chunkType` - yığının növünü göstərir

* `chunkData` - yığının ikili yükü


parça növləri haradadır:

|# |Yığın Tipi|ASCII|Təsvir|Başlar
---|---|---|---|---|
|1.|0x4E4F534A|JSON|Strukturlaşdırılmış JSON məzmunu|1
|2.|0x004E4942|BIN|İkili bufer|0 və ya 1

Hər bir yığının başlanğıcı və sonu 4 baytlıq sərhədə uyğunlaşdırılmalı və bu məqsədlə padding istifadə edilməlidir.

##### Strukturlaşdırılmış JSON Məzmunu

Bu, Binary glTF aktivinin ilk hissəsi olmalıdır və icraya sonrakı hissələrdən resursları tədricən əldə etməyə imkan verir. Bu, həmçinin ikili glTF aktivindən yalnız seçilmiş resurs alt dəstini, məsələn, şəbəkənin ən qaba LOD-unu oxumaq imkanı verir. Düzəliş tələblərinə cavab vermək üçün bu hissə arxadakı Boşluq simvolları ilə doldurulmalıdır (0x20).

##### İkili Bufer #####

Bu hissə həndəsə, animasiya əsas çərçivələri, dərilər və şəkillər üçün ikili yükdən ibarətdir. O, Binary glTF aktivinin ikinci hissəsi olmalıdır və düzülmə tələblərini yerinə yetirmək üçün arxadakı sıfırlarla (0x00) doldurulmalıdır.

## İstinadlar ##

* [GLB Fayl Formatının Xüsusiyyətləri - Khronos](/3d/gltf/)


