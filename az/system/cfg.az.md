{
  "date": "2021-06-29",
  "keywords": [
"CFG",
"uzadılması",
"fayl",
"format",
"sistemi",
"konfiqurasiya",
"parametrlər",
"proqramlar",
"kompüter",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CFG - Fayl formatı",
  "description": "CFG faylları yarada və aça bilən CFG fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFG",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-cf-azg"
}
},
  "lastmod": "2021-06-29"
}

## CFG faylı nədir? ##

.cfg uzantılı fayl bir növ parametrlər faylıdır. Bu, populyar olaraq istifadə edilən fayl növüdür və kompüter proqramlarının konfiqurasiyası və parametrləri ilə bağlı məlumatları saxlamaq üçün istifadə olunur. CFG fayllarının əksər növləri mətn formatında saxlanılır və əl ilə açılmamalıdır, əksinə, mətn redaktoru ilə açılmalıdır. Bununla belə, məlumatın saxlandığı formatda fərqlənən müxtəlif növ CFG faylları var. CFG fayllarının təklif etdiyi xüsusiyyətlər proqramdan tətbiqə dəyişir. Bəzi kompüter proqramları istifadəçilərə qrafik müdaxilələrdən istifadə etməklə konfiqurasiya fayllarının sintaksisini dəyişdirməyə və ya inkişaf etdirməyə imkan verir, digərləri isə yalnız mətn redaktorundan istifadə edərək dəyişikliklərə icazə verir. Bu faylları dəyişdirdikdən sonra istifadəçilər proqrama bu faylları yenidən oxumağı və dəyişiklikləri sistemə tətbiq etməyi tapşıra bilərlər.


## CFG Fayl Format ##

CFG files are supported by various operating systems such as Unix and Unix-like operating systems, MS-DOS, macOS, Microsoft Windows, and IBM OS/2. Bu faylların saxlandığı və bu əməliyyat sistemlərinin hər birində istifadə olunan format fərqlidir. Əksər sistemlər bu faylları insan tərəfindən oxuna bilən və redaktə edilə bilən düz mətn formatında istifadə edir və saxlayır, digərləri isə faylların istifadəsi və əməliyyat sisteminin tələbindən asılı olaraq daha mürəkkəb formatda saxlayır.

Unix və Unix-ə bənzər əməliyyat sistemlərində əksər CFG faylları CFG faylları üçün bir neçə fərqli format üslubundan istifadə olunur, lakin ən çox yayılmış format asanlıqla oxuna bilən düz mətn formatıdır və demək olar ki, bütün formatlar şərhlər yazmağa və redaktə etməyə imkan verir. Bu əməliyyat sistemlərində CFG faylları üçün ən çox yayılmış fayl uzantıları CNF, CONF, CF və INI-dir.

MS-DOS əməliyyat sistemində əvvəlcə yalnız bir konfiqurasiya faylı formatı var idi, yəni düz mətn, lakin MS-DOS 6 özü ilə INI konfiqurasiya faylı formatının tətbiqini gətirdi.

macOS standart mülkiyyət siyahısı formatı konfiqurasiya faylından istifadə edir.

Microsoft Windows-da düz mətn INI üslublu konfiqurasiya faylları məlumatın saxlanması və redaktə edilməsi üçün mühüm mənbə idi, lakin 1993-cü ildə yeni verilənlər bazası sistemi təqdim edildi və bu, 1993-cü ildən sonra Microsoft Windows-da konfiqurasiya fayllarının istifadəsinin azalmasına səbəb oldu.


## CFG Nümunəsi ##

Nümunə CFG faylı aşağıda görünə bilər:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```

## Digər CFG faylları

**.cfg** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Parametrlər**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Oyun**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistem və Müxtəlif**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

