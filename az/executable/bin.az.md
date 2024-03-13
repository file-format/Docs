{
   "date":"2023-07-20",
   "keywords":[
"ZİBİL QABI",
"BIN faylı",
"fayl",
"BIN fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN fayl formatı - Unix icra edilə bilən fayl",
   "description":"BIN faylları yarada və aça bilən BIN formatı və API-lər haqqında öyrənin.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin-az",
         "parent":"executable"
}
},
   "lastmod":"2023-07-20"
}

## BIN faylı nədir?

BIN faylı Linux və ya FreeBSD kimi Unix əsaslı əməliyyat sistemlərində icra edilə bilən fayldır. O, mənbə kodundan əldə edilən ikili koddan ibarət tərtib edilmiş proqrama malikdir və onu əsas sistem arxitekturası ilə uyğunlaşdırır. Unix İcra edilə bilən BIN faylları icra edilə bilən formatlar roluna görə Windows .EXE faylları və macOS .APP faylları ilə müqayisə oluna bilər.

Unix sistemləri üçün proqram təminatının inkişafı sahəsində BIN faylları proqramları paketləmək və yaymaq üçün tərtibatçılar tərəfindən adətən istifadə olunur. Onlar asan quraşdırma və icra etməyə imkan verən proqram təminatının istifadəçilərə çatdırılması üçün əlverişli vasitə təklif edirlər. BIN faylları ilə yanaşı, hər biri xüsusi aparat və ya sistem tələblərinə uyğunlaşdırılmış [.ELF](/executable/elf/), .X86, [.RUN](/executable/run/) və .X86_64 daxil olmaqla, digər Unix icra edilə bilən proqram növləri mövcuddur.

BIN faylının daxili strukturuna gəldikdə, o, Unix əməliyyat sisteminin əlavə edilmiş proqramı müəyyən etmək, oxumaq və icra etmək üçün istifadə etdiyi kodlaşdırılmış məlumatlardan ibarətdir. Sistem, BIN faylını icra olunan fayl kimi tanımaq üçün xüsusi fayl imzalarına və ya başlıqlarına etibar edir, ardınca daxilində olan ikili təlimatların təfsiri və icrası.

BIN faylları tez-tez proqramı düzgün quraşdırmaq və quraşdırmaq haqqında ətraflı təlimatları təmin edən **INSTALL.TXT** faylı ilə birlikdə verilir. Bu sənədlər istifadəçilərin quraşdırma prosesini uğurla idarə etmələrini və proqram təminatından heç bir problem olmadan istifadə etməyə başlamalarını təmin edir.

## BIN faylını necə açmaq olar?

BIN faylları birbaşa açılmaq və baxmaq üçün nəzərdə tutulmayıb. Bununla belə, siz proqramları icra edə və ya onların tərkibində olan məlumatları çıxara bilərsiniz. BIN faylının məzmununa daxil olmaq üçün BIN faylının adının sample.bin olduğunu fərz edərək, komanda xəttində bu addımları yerinə yetirin:

1. **İcra edilə bilən icazələri təmin edin:**

BIN faylını icra etməzdən əvvəl onun icra olunan fayl kimi işlədilməsi üçün lazımi icazələrə malik olduğundan əmin olun. Komandanı istifadə edin:

```
$ chmod +x sample.bin
```

Bu əmr fayla icra edilə bilən imtiyazlar verir.

2. **BIN faylını icra edin:**

İcra edilə bilən icazələri təyin etdikdən sonra aşağıdakı əmri daxil edərək BIN faylını işə sala bilərsiniz:

```
$ ./sample.bin
```

**Xəbərdarlıq**

_Endirilmiş və ya e-poçtla göndərilmiş BIN faylları ilə işləyərkən ehtiyatlı olun, çünki onlar potensial olaraq kibercinayətkarlar tərəfindən zərərli proqramları yaymaq üçün istifadə edilə bilər. Zərərli icra edilə bilən hücumlar riskini azaltmaq üçün yalnız etibarlı mənbələrdən BIN fayllarını işə salın._

## Digər BIN faylları

**.bin** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

- [BIN - MacBinary Encoded File](/compression/bin/)
- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## İstinadlar

* [Linux-da Binar Faylları Necə İcra etmək olar](https://linuxhint.com/execute-binary-files-in-linux/)



