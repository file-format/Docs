{
  "date": "2023-04-20",
  "keywords": [
"ldb faylı",
"ldb faylı nədir",
"ldb hansı məlumatları ehtiva edir",
"ldb faylının məqsədi nədir",
"ldb uzantısı",
"fayl",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "LDB Fayl Format - Microsoft Access Kilidi Faylı",
  "description": "LDB formatı və onun hansı məlumatları ehtiva etdiyini öyrənin.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb-az",
      "parent": "misc"
}
},
  "lastmod": "2023-04-20"
}

## LDB faylı nədir?

LDB faylı birdən çox istifadəçinin eyni verilənlər bazasını eyni vaxtda redaktə etməsinin qarşısını almaq üçün Microsoft Access tərəfindən istifadə edilən kilid faylıdır. İstifadəçi Access verilənlər bazasını açdıqda, Access verilənlər bazası ilə eyni kataloqda müvafiq LDB faylı yaradır. Bu fayl hazırda verilənlər bazasından kimin istifadə etdiyi və hansı qeydləri redaktə etdiyi barədə məlumatı ehtiva edir.

LDB faylı verilənlər bazası açıldıqda avtomatik olaraq Microsoft Access tərəfindən yaradılır və verilənlər bazası bağlandıqda silinir. Qeyd etmək vacibdir ki, LDB faylı heç vaxt əl ilə silinməməlidir, çünki bu, verilənlər bazası ilə problemlər yarada bilər.

Microsoft Access verilənlər bazası ilə bağlı problemlərlə qarşılaşsanız, potensial həll yolu həmin verilənlər bazası ilə əlaqəli LDB faylını silməyə cəhd etməkdir. Bu, verilənlər bazasına daxil olmanıza mane ola biləcək bütün kilidləri azad edəcək. Bununla belə, buna cəhd etməzdən əvvəl verilənlər bazasının ehtiyat nüsxəsini çıxardığınızdan əmin olun, çünki LDB faylının silinməsi düzgün aparılmadıqda məlumat itkisinə və ya korlanmasına səbəb ola bilər.

## LDB Fayl Format - Ətraflı Məlumat

Microsoft Access-də LDB faylı hazırda verilənlər bazasına daxil olan istifadəçilər haqqında istifadəçi adı, kompüter adı və giriş vaxtı kimi məlumatları ehtiva edir. LDB faylı həmçinin verilənlər bazasına yerləşdirilən hər hansı kilidlər haqqında məlumatları, məsələn, hansı qeydlərin hansı istifadəçi tərəfindən redaktə edildiyini ehtiva edir.

LDB faylında tapıla bilən məlumat növlərinin daha ətraflı siyahısı:

- **İstifadəçi adı** - hazırda verilənlər bazasına daxil olan istifadəçinin adı
- **Kompüter adı** - istifadəçinin verilənlər bazasına daxil olduğu kompüterin adı
- **Giriş vaxtı** - istifadəçinin verilənlər bazasını ilk dəfə açdığı vaxt
- **Qeyd kilidləri** - hansı qeydlərin hazırda hansı istifadəçi tərəfindən redaktə edildiyi haqqında məlumat
- **Obyekt kilidləri** - hazırda hansı verilənlər bazası obyektlərinin (məsələn, cədvəllər, formalar və ya hesabatlar) hansı istifadəçi tərəfindən redaktə edildiyi haqqında məlumat
- **Bağlantı məlumatı** - istifadəçinin verilənlər bazasına necə qoşulduğu haqqında məlumat (məsələn, yerli və ya şəbəkə bağlantısından istifadə edib-etməməsi)

LDB faylındakı məlumat birdən çox istifadəçinin eyni verilənlər bazasında eyni vaxtda ziddiyyətli dəyişikliklər etməsinin qarşısını almaq üçün Microsoft Access tərəfindən istifadə olunur. İstifadəçi başqa istifadəçi tərəfindən artıq kilidlənmiş qeydi və ya obyekti redaktə etməyə cəhd etdikdə, Microsoft Access obyektin artıq istifadə edildiyini bildirən bir mesaj göstərəcək. LDB faylı istifadəçilər verilənlər bazasını açıb bağladıqca və kilidlənmiş obyektlərə dəyişiklik etdikcə yenilənir.

## İstinadlar
* [What is an LDB File?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)

