{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Unreal Static Meshes VPK fayl formatı və VPK faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title" : "VPK Faylı - Qeyri-real Statik Meshes Faylı",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-az",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## VPK faylı nədir?

.vpk faylı Valve Corporation tərəfindən hazırlanmış oyun mühərriki olan **Mənbə Mühərriki** tərəfindən istifadə edilən fayl formatıdır. VPK faylları modellər, teksturalar və səslər kimi oyun məzmununu paketləmək üçün istifadə olunur və adətən Team Fortress 2, Left 4 Dead və Counter-Strike: Global Offensive kimi oyunlarda istifadə olunur. Fayllar GCFScape və VPK Aləti kimi müxtəlif alətlərdən istifadə etməklə açıla və çıxarıla bilər.

## VPK Fayl Format - Ətraflı Məlumat

VPK faylları ikili fayllar kimi diskdə saxlanılır. Tək bir vpk faylı VPK paketinin bir hissəsi ola bilər və ya müstəqil xam VPK faylı kimi çıxış edə bilər. VPK faylında saxlanıla bilən məlumatlara xəritələr, materiallar, oyun məzmunu və xoreoqrafiya səhnələri daxildir.

### VPK faylını necə yaratmaq olar?

Mövcud alətlərdən asılı olaraq .vpk faylı yaratmağın bir neçə yolu var.

1. `VPK alətindən istifadə:` Bu, VPK faylları yaratmaq və çıxarmaq üçün istifadə edilə bilən komanda xətti alətidir. VPK faylı aşağıdakı əmrdən istifadə etməklə yaradıla bilər:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Bu, göstərilən qovluqdan VPK faylı yaradacaq və onu göstərilən çıxış faylı kimi saxlayacaqdır.

1. `Çəkic Redaktorundan istifadə:` Çəkic Redaktoru Mənbə mühərrikindən istifadə edən oyunlar üçün səviyyələr yaratmaq və redaktə etmək üçün istifadə edilə bilən Mənbə SDK-ya daxil olan alətdir. Bu, həmçinin Fayl Sistemi sekmesinde bir qovluğa sağ tıklayarak və VPK Yarat seçimini etməklə VPK faylları yaratmaq imkanı daxildir.

1. `Valve-nin VPK yaradıcısından istifadə:` Bu, Valve tərəfindən işlənib hazırlanmış və oyun məzmununu qablaşdırmaq və yaymaq üçün istifadə edilən alətdir. Bu alət VPK faylları yaratmaq üçün istifadə edilə bilər və həmçinin VPK faylları yaratmaq üçün rəsmi vasitədir.

## İstinadlar

 * [Valve Proqramı](https://www.valvesoftware.com/en/)
 * [VPK Tərtibatçısının Resursları](https://developer.valvesoftware.com/wiki/GCF)

