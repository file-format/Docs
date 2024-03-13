{
  "date": "2021-06-30",
  "keywords": [
"exe faylı",
"exe fayl formatı",
"exe faylı nədir",
"fayl",
"exe nümunəsi",
"exe fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": ".exe faylı Windows OS-də işləyən Microsoft İcra edilə bilən fayldır. EXE fayl formatı haqqında daha çox məlumat əldə edin.",
  "title": "Executable EXE faylı nədir?",
  "linktitle": "EXE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ex-aze"
}
},
  "lastmod": "2021-06-30"
}

## EXE faylı nədir?

EXE sözü **executable** üçün qısadır. .exe faylı Microsoft Windows əməliyyat sistemində icra oluna bilən proqramdır. Proqram tərtibatçıları əsasən Windows OS üçün proqramlarını exe faylları kimi icra edilə bilən formatda dərc edirlər. Windows-da tətbiqləri işə salmaq üçün standart fayl formatıdır. **Setup.exe**, **Install.exe** və **cmd.exe** EXE fayllarının bəzi ümumi və yaxşı tanış adlarıdır.

## EXE fayl formatı

MS-DOS kompilyatorları 64K yaddaş məhdudiyyətinə malik yaddaş modelləri ilə təqdim edildi. Ümumi konsepsiya x86 CPU-da (CS, DS, ES, SS) müxtəlif və ya eyni seqmentlərə işarə etmək üçün müxtəlif seqment registrlərini təyin etməkdir, buna görə də yaddaşa müxtəlif dərəcələrdə çıxış imkanı verir. Bəzi xüsusi yaddaş modelləri bunlar idi:

- **Tiny**: Bütün yaddaş girişləri 16-bitdir (seqment registrləri dəyişməz). .EXE faylı əvəzinə .COM faylı yaradır.
- **Kiçik**: Bütün yaddaş girişləri 16 bitdir (seqment registrləri dəyişməz).
- **Yığcam**: Məlumat ünvanlarına həm seqment, həm də ofset daxildir, giriş zamanı DS və ya ES registrlərini yenidən yükləyir və 1M-ə qədər məlumat əldə etməyə imkan verir. Kod girişləri CS reyestrini dəyişmir, 64K koda imkan verir.
- **Orta**: Kod ünvanlarına girişdə CS-nin yenidən yüklənməsi və 1M-ə qədər koda icazə verən seqment ünvanı daxildir. Məlumata girişlər DS və ES registrlərini dəyişmir, 64K dataya imkan verir.
- **Böyük**: Həm kod, həm də məlumat ünvanları (seqment, ofset) cütləridir, həmişə seqment ünvanlarını yenidən yükləyir. Bütün 1M bayt yaddaş sahəsi həm kod, həm də məlumat üçün mövcuddur.
- **Böyük**: Böyük modellə eyni, 64K-dan böyük massivlərə giriş imkanı vermək üçün kompilyator tərəfindən əlavə arifmetik yaradılır.

Tərtibatçılar exe faylı yaratarkən hansı modelin seçiləcəyinə qərar verməlidirlər.

### Portativ EXE fayl formatı

Portativ icra edilə bilən fayl formatı (PE) bir sıra məlumat başlıqlarını ehtiva edir, aşağıdakı başlıqların siyahısıdır:

- **DOS başlığı**: MS-DOS başlığı ya geriyə uyğunluğu, ya da yeni fayl növlərinin zərif şəkildə azalmasını təmin edir.
- **PE Başlığı**: DOS başlığının əvvəlindən 60 (0x3C) ofsetdə PE Fayl başlığına göstəricidir
- **COFF Başlığı**: COFF başlığında icra olunan fayl üçün faydalı olan bəzi məlumatlar və obyekt faylı üçün daha faydalı olan bəzi məlumatlar var.
- **PE Könüllü Başlıq**: PE Əlavə Başlığı birbaşa COFF başlığından sonra baş verir və bəzi mənbələr hətta iki başlığı eyni strukturun bir hissəsi kimi göstərir.
- **Bölmə Cədvəli**: PE Əlavə Başlıqdan dərhal sonra bölmə cədvəli tapırıq. Bölmə cədvəli IMAGE_SECTION_HEADER strukturlarının massivindən ibarətdir.
- **Mapable Sections**: Kitabxananın kodunu birdən çox prosesə uyğunlaşdırmaqla yaddaşda yer saxlaya bilər.

## Mac-da EXE faylını işlədə bilərsinizmi?

Exe faylları Mac OS-də icra olunanlar kimi istifadə edilmir. Bununla belə, Mac OS-də exe faylını işə salmaq istəyirsinizsə, aşağıdakı üsullardan istifadə edə bilərsiniz.

 1. **Wine** - Şərab Mac sistemlərində öz kompüter proqramlarından istifadə etmək istəyən insanlar üçün mükəmməl həlldir. Bu, Şərab Emulator Deyil mənasını verən qısaltmadır. Wine, Microsoft tərəfindən istifadə edilən eyni kataloqlar mühitini yaradır ki, siz ondan istifadə edərək Windows proqramınızı işə salasınız.
 2. **Virtual Maşınlar** - Parallel Desktop və ya VM Virtual Box istifadə edərək Windows Virtual Maşın yaradın və tətbiqinizi virtual maşın daxilində işlədin.
 3. **Boot Camp** - Mac OS-də Windows Boot Camp-ın quraşdırılması və konfiqurasiyası sizə Mac maşınında Windows ƏS-ni işə salmağa imkan verir.

## İstinadlar

* [.exe- Wikipewdia tərəfindən](https://en.wikipedia.org/wiki/.exe)

* [x86 Disassembly/Windows Executable Files](https://en.wikibooks.org/wiki/X86_Disassembly/Windows_Executable_Files#MS-DOS_EXE_Files)


