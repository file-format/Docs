{
   "date":"2023-10-11",
   "keywords":[
"şeyder",
"shader faylı",
"shader godot engine shader faylı",
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
   "title":"SHADER fayl formatı - Godot Engine Shader Faylı",
   "description":"SHADER Godot Engine Shader fayl formatı və SHADER fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
   "linktitle":"SHADER Godot",
   "menu":{
      "docs":{
         "identifier":"game-shader-godot-az",
         "parent":"game"
}
},
   "lastmod":"2023-10-11"
}

## SHADER faylı nədir?

**Godot Engine Shader File** xüsusi şeyderləri müəyyən etmək üçün **Godot oyun mühərrikində** istifadə olunan fayldır. Şeyderlər 3D və ya 2D oyunda obyektlərin necə göstərilməli olduğunu müəyyən etməklə onların görünüşünü manipulyasiya etmək üsuludur. Bu şader faylları adətən Godot oyun mühərrikində istifadə üçün nəzərdə tutulmuş xüsusi kölgələmə dili olan Godot Shader Language (GDScript) adlı dildə yazılır.

## SHADER necə yaradılır?

Godot-da siz müxtəlif vizual effektlərə nail olmaq üçün şaderlər yarada bilərsiniz, o cümlədən bunlarla məhdudlaşmayaraq:

1.  Obyektin rəngini və ya fakturasını dəyişdirmək.
2.  Müxtəlif işıqlandırma və kölgə effektlərinin tətbiqi.
3.  3D modellər üçün xüsusi materialların yaradılması.
4.  Obyektlərin görünüşünü təhrif etmək və ya canlandırmaq.

## Nümunə SHADER faylı

Godot Shader Faylı adətən .shader uzantısına malikdir və obyektin necə göstərilməsini müəyyən edən şeyder kodunu ehtiva edir. Budur çox sadə bir Godot Shader Faylının sadə bir nümunəsi:

```gdscript
shader_type canvas_item;

void fragment() {
    // Modify fragment color
    COLOR = vec4(1.0, 0.0, 0.0, 1.0); // Red color
}
```

Bu misalda şeyder kodu 2D kətan elementi üçün yazılmışdır və o, sadəcə olaraq obyektin rəngini qırmızıya təyin edir. Bu, çox sadə şeyderdir və praktikada şeyderlər qabaqcıl vizual effektlərə nail olmaq üçün kifayət qədər mürəkkəbləşə bilər.

Godot, birbaşa kod yazmadan şeyderlər yaratmağa imkan verən vizual şeyder redaktoru təqdim edir və onu şeyder proqramlaşdırması ilə dərin təcrübəyə malik olmayan oyun tərtibatçıları üçün əlçatan edir. Bu vizual redaktor, fərdi şaderlər yaratmaq üçün müxtəlif qovşaqları birləşdirməyə imkan verir.

Godot layihənizdə şeyderdən istifadə etmək üçün siz onu materiala əlavə edərdiniz, sonra onu spraytə, 3D modelə və ya müəyyən şeyder effekti ilə göstərmək istədiyiniz hər hansı digər obyektə tətbiq edə bilərsiniz.

## Godot Oyun Mühərriki

Godot, tərtibatçılara 2D və 3D oyunlar və interaktiv proqramlar yaratmağa imkan verən açıq mənbəli, çarpaz platformalı oyun mühərrikidir. O, istifadəçi dostu, çox yönlü və möhkəm funksiyalar dəsti ilə tanınır. Godot oyun mühərrikinin bəzi əsas cəhətləri və xüsusiyyətləri bunlardır:

1.  **Açıq Mənbə:** Qodot MIT lisenziyası ilə buraxılmışdır, yəni istifadə etmək pulsuzdur və açıq mənbədir. Tərtibatçılar mənbə koduna daxil ola və dəyişdirə, onu yüksək dərəcədə fərdiləşdirilə bilər.
    
2.  **Kross-Platforma:** Qodot Windows, macOS, Linux, Android, iOS, HTML5 və s. daxil olmaqla geniş platformaları dəstəkləyir. Oyununuzu bir platformada inkişaf etdirə və bir çox başqa platformaya ixrac edə bilərsiniz.
    
3.  **Scripting:** Godot bir çox skript dillərini, o cümlədən GDScript (Godot üçün hazırlanmış Python-a bənzər dil), C# və VisualScript (vizual proqramlaşdırma dili) dəstəkləyir. Bu çeviklik tərtibatçılara ən rahat olduqları dili seçməyə imkan verir.
    
4.  **Səhnə Sistemi:** Qodot oyun elementlərini təşkil etməyi və tərtib etməyi asanlaşdıran qovşaq əsaslı səhnə sistemindən istifadə edir. Səhnələr obyektləri, simvolları, UI elementlərini və daha çoxunu təmsil edə bilən müxtəlif qovşaqlardan ibarət ola bilər.
    
5.  **Fizika:** Qodotun daxili 2D və 3D fizika mühərriki var ki, bu da real fizika qarşılıqlı təsirləri ilə oyunlar yaratmağı asanlaşdırır.
    
6.  **Animasiya:** Qodot obyektlərə, simvollara və UI elementlərinə tətbiq oluna bilən mürəkkəb animasiyalar yaratmaq üçün möhkəm animasiya sistemi təqdim edir.
    
7.  **Asset Management:** Godot, şəkillər, audio, 3D modellər və daha çox daxil olmaqla, aktivlərin idarə edilməsi üçün resurs sistemi təklif edir. Resurslar asanlıqla idxal edilir və mühərrikdə təşkil edilir.
    
8.  **Visual Shaders:** Godot, tərtibatçılara kod yazmadan mürəkkəb şeyder effektləri yaratmağa imkan verən vizual şeyder redaktoruna malikdir.
    
9.  **Redaktor:** Godot redaktoru istifadəçi dostudur və xüsusiyyətlərlə zəngindir. Buraya səviyyəli dizayn, animasiya, skript redaktəsi və daha çox alətlər daxildir. O, real vaxt rejimində redaktəni və canlı sazlamanı dəstəkləyir.
    
10.  **GDNative:** GDNative sizə modulları və plaginləri C və C++ kimi dillərdə yazmağa və onları Godot ilə qüsursuz inteqrasiya etməyə imkan verir.
    

Godot indie oyun tərtibatçıları, həvəskarlar və kiçik və orta ölçülü oyun inkişaf etdirmə komandaları üçün əla seçimdir. O, müxtəlif səviyyəli təcrübəyə malik tərtibatçılar üçün əlçatan qalaraq oyunlar və interaktiv proqramlar yaratmaq üçün güclü və çevik platforma təklif edir.

## SHADER faylını necə açmaq olar?

SHADER fayllarını açan və ya onlara istinad edən proqramlar daxildir

- **Godot Engine** (Pulsuz) (Windows, Mac, Linux) üçün

## Digər SHADER faylları

**.shader** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Oyun Faylları**
- [SHADER - Godot Engine Shader File](/game/shader-godot/)
- [SHADER - Quake 3 Engine Shader File](/game/shader-quake/)
- [SHADER - Unity Shader Asset](/game/shader-unity/)

## İstinadlar
* [Godot (oyun mühərriki)](https://en.wikipedia.org/wiki/Godot_(oyun_mühərriki))


