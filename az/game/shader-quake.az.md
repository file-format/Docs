{
   "date":"2023-10-11",
   "keywords":[
"şeyder",
"shader faylı",
"shader quake 3 mühərrik şader faylı",
"shader faylını necə açmaq olar",
"fayl",
"shader fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"SHADER Fayl Format - Quake 3 Engine Shader Faylı",
   "description":"SHADER Quake 3 Engine Shader fayl formatı və SHADER fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
   "linktitle":"SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake-az",
         "parent":"game"
}
},
   "lastmod":"2023-10-11"
}

## SHADER faylı nədir?

SHADER fayl formatı **Quake 3 mühərrikində** oyundakı tekstura və materiallar üçün şaderləri müəyyən etmək üçün istifadə olunur. Görünüş, əks etdirmə, şəffaflıq və digər vizual xassələri daxil olmaqla, səthin necə göstərilməli olduğunu müəyyən etmək üçün kölgələr istifadə olunur.

## Quake 3 Engine SHADER Faylı

Quake 3 mühərrik şader faylının strukturu və sintaksisinin əsas icmalı:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

Quake 3 mühərrik şader faylında siz hər birinin özünəməxsus xüsusiyyətləri və mərhələləri olan bir neçə şeyder təyin edə bilərsiniz. Bu şaderlər oyun dünyasında müxtəlif tekstura və materialların görünüşünü müəyyən etmək üçün istifadə olunur. Mühərrik bu məlumatdan səthləri müəyyən vizual effektlər və davranışlarla göstərmək üçün istifadə edir.

Quake 3 mühərrikindəki Shader faylları oyunda toxumaların və materialların necə görünməsi barədə təlimatları ehtiva edən sadə mətn fayllarıdır. Bu fayllar adi mətn redaktoru ilə açıla və redaktə edilə bilər və adətən oyunun .PK3 paketində **/scripts** kataloqunda tapılır.

## Quake 3 Mühərriki

Quake 3 mühərriki id Software tərəfindən hazırlanmış yüksək təsirli və çox yönlü oyun mühərrikidir. İlk dəfə 1999-cu ildə Quake III Arena oyununun buraxılması ilə təqdim edildi və o vaxtdan bəri müxtəlif digər oyunlarda istifadə olunur. Mühərrik qabaqcıl qrafika, çox oyunçu imkanları və dəyişdirilə bilməsi ilə tanınır.

Quake 3 mühərrikinin bəzi əsas xüsusiyyətləri və aspektləri bunlardır:

1.  **Qrafik Mühərrik:** Quake 3 mühərriki vaxtilə ən müasir qrafik texnologiyası ilə məşhur idi. O, 1990-cı illərin sonlarında təməlqoyma yaradan əyri səthlər, şaderlər və dinamik işıqlandırma kimi qabaqcıl xüsusiyyətləri təqdim etdi.
    
2.  **Multiplayer Focus:** Quake 3 Arena ilk növbədə multiplayer birinci şəxs atıcı kimi hazırlanmışdır. Mühərrikin şəbəkə kodu və onlayn multiplayer oyunları üçün dəstəyi müstəsna idi və bu onu rəqabətli onlayn oyun üçün məşhur seçim etdi.
    
3.  **Dəyişdirilmə qabiliyyəti:** Quake 3 mühərriki dəyişdirilə bilənliyi ilə tanınır. id Proqramı açıq mənbəli GNU General Public License (GPL) altında mühərrik mənbə kodunu buraxdı. Bu, canlı modding icmasına gətirib çıxaran çoxsaylı modların və xüsusi xəritələrin yaradılmasını təşviq etdi.
    
4.  **Skriptlə Oynanış:** Mühərrik oyun qaydalarını və davranışını müəyyən etmək üçün skriptə əsaslanan sistemdən istifadə edərək, moderatorlar və xəritəçilərə xüsusi oyun rejimləri və unikal təcrübələr yaratmağı nisbətən asanlaşdırdı.
    
5.  **Xüsusi Məzmun üçün Dəstək:** Quake 3-ün mühərriki istifadəçi tərəfindən yaradılmış xəritələrdə və modifikasiyalarda yüksək dərəcədə fərdiləşdirməyə imkan verən fakturalar, modellər və səs faylları daxil olmaqla fərdi məzmunu dəstəkləyir.
    
6.  **Səviyyə Dizaynı:** Mühərrik fırça əsaslı səviyyəli dizayn sistemindən istifadə etdi, burada xəritələr bərk fırçalardan boşluqlar oyaraq quruldu. Bu yanaşma səviyyəli dizaynerlər üçün yaxşı sənədləşdirilmiş və istifadəçi dostu idi.


İllər ərzində Quake 3 mühərriki bir çox digər oyun və modifikasiyalar üçün əsas kimi istifadə edilmişdir, o cümlədən Qala Wolfenstein, Ulduz Döyüşləri Jedi Cəngavər II: Çıxılan Jedi və digərləri arasında Urban Terror. O, oyun inkişafı dünyasında qalıcı miras qoydu və birinci şəxs atıcı janrının formalaşmasına kömək etdi. O vaxtdan bəri daha yeni və daha təkmil mühərriklər ortaya çıxsa da, Quake 3 mühərriki oyun sənayesinə verdiyi töhfəyə görə hörmət edilməyə davam edir.

## SHADER faylını necə açmaq olar?

SHADER fayllarını açan və ya onlara istinad edən proqramlar daxildir

- **id Software Quake 3** (Ödənişli) (Windows, Mac, Linux)
- Microsoft Notepad
- Notepad++
- İstənilən mətn redaktoru

## Digər SHADER faylları

**.shader** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Oyun Faylları**
- [SHADER - Godot Engine Shader File](/game/shader-godot/)
- [SHADER - Quake 3 Engine Shader File](/game/shader-quake/)
- [SHADER - Unity Shader Asset](/game/shader-unity/)

## İstinadlar
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

