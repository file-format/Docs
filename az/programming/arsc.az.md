{
  "date": "2019-10-11",
  "keywords": [
"qövs",
".arsc",
"arsc faylı nədir",
"arsc faylını necə açmaq olar",
"uzadılması",
"fayl",
"arsc faylı",
"arsc fayl formatı",
"arsc fayl uzantısı",
"arsc fayl nümunəsi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARSC - Android Paket Resurs Cədvəli Faylı ",
  "description": "ARSC fayl formatı və ARSC faylını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "ARSC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ars-azc"
}
},
  "lastmod": "2021-06-22"
}

## ARSC faylı nədir?

ARSC faylı proqramın cədvəl formatında resursların siyahısını ehtiva edən Android Resurs cədvəli faylıdır. Bu, Resurs adları, xassələr və ID-lər kimi məlumatları ehtiva edir. ARSC faylları bu Android proqramlarını quraşdırmaq üçün istifadə edilən APK paketlərinin bir hissəsidir. Android proqramında olan şəkillər, tərtibatlar, üslublar və sətirlər kimi bütün resurslar APK faylı yaradılan zaman ikili fayllara çevrilir. ARSC faylı da eyni zamanda yaradılır, proqramın bütün tərtib edilmiş resurslarının və onların identifikatorlarının siyahısını ehtiva edir.

## ARSC fayl formatı

.arsc genişləndirmə faylları ANT (Eclipse) və ya Gradle (AS) kimi kompilyator [APK](/compression/apk/) faylını yaratmaq üçün Android proqram kodunu tərtib etdikdən sonra yaradılan ikili fayllardır. Tərtib edilmiş java sinif faylları olan, yəni classes.dex olan məzmununa baxmaq üçün WinZip kimi istənilən arxivləşdirmə yardım proqramından istifadə edərək APK faylını çıxara bilərsiniz. Bunlara əlavə olaraq, bu ARSC faylını, həmçinin meta-məlumatı ehtiva edir:

 * XML qovşaqları
 * Atributlar
 * Resurs İdentifikatorları

APK faylındakı resurslar Resurs İdentifikatorları ilə istinad edilir, atributlar isə icra zamanı bir dəyərə həll edilir. Android aapt aləti quraşdırma zamanı fayllarda müəyyən edilmiş bütün resursları toplayır və onlara resurs identifikatorlarını təyin edir. Tərtib edilmiş resurslara identifikatorlar təyin edildikdən sonra mənbə kodundan, eləcə də resources.arsc-dən R.java faylı yaradılır.

## İstinadlar

* [İkili Resurs Cədvəli Strukturu](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)


