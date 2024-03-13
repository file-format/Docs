{
  "date": "2021-04-08",
  "keywords": [
"deb faylı",
"deb fayl formatı",
"deb faylı nədir",
"fayl",
"deb misal",
"deb fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DEB - Bzip Sıxılmış Tar Arxivi",
  "description": "DEB faylları yarada və aça bilən DEB fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DEB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-de-azb"
}
},
  "lastmod": "2021-04-09"
}

## DEB faylı nədir?

.deb uzantısı olan fayl Linux ƏS-də proqram paketlərinin paylanması üçün mövcud Debian ikili paket fayl formatıdır. O, iki [TAR](/compression/tar/) arxiv faylından ibarətdir. DPKG DEB paketlərini oxumaq və quraşdırmaq mexanizmini təmin edir. DEB paketləri APT paket proqram idarəetmə interfeysindən istifadə etməklə quraşdırıla bilər. DEB faylları `application/vnd.debian.binary-package` kimi İnternet Media Tipinə malikdir.

## DEB fayl formatı

DEB faylı iki [TAR](/compression/tar/) arxiv faylından ibarətdir. Bir arxiv nəzarət məlumatını, digəri isə quraşdırıla bilən məlumatları ehtiva edir.

### Paket Təşkilatı

DEB faylı sehrli dəyəri olan **ar** arxiv faylıdır!<arch> `. Debian 0.93-dən bəri DEB fayllarının arxivləşdirmə mexanizmində müəyyən ardıcıllıqla üç fayl var.

 1. `Debian Binary` - It is destined to have a series of lines, separated by newlines. At present, only a single line is present that describes the version number. The current version number is 2.0.
 1. `İdarəetmə Arxivi` - O, idarəedici skriptləri və paketin adı, versiya, asılılıqlar və baxıcı kimi paket haqqında meta-məlumatı olan control.tar arxivindən ibarətdir.
 1. `Məlumat Arxivi` - Bu data.tar adlı tar arxividir və faktiki quraşdırıla bilən media fayllarını ehtiva edir. Arxiv gz, bz2, lzma və ya xz ilə sıxıla bilər və məlumat arxivinin fayl uzantısı müvafiq olaraq dəyişir.

### Nəzarət Arxivi

Nəzarət arxivinə aşağıdakı kimi məzmun daxil ola bilər.

 * `control` - It contains a brief description of the package as well as other information such as its dependencies.
 * `md5sums` - O, pozulmuş və ya natamam faylları aşkar etmək üçün paketdəki bütün faylların MD5 yoxlama cəmini ehtiva edir.
 * `conffiles` - Konfiqurasiya faylları kimi qəbul edilməli olan paketin fayllarını sadalayır. Konfiqurasiya faylları müəyyən edilmədiyi təqdirdə yeniləmə zamanı üzərinə yazılmır.
 * `preinst`, postinst, prerm və postrm - Paketi quraşdırmadan və ya çıxarmadan əvvəl və ya sonra yerinə yetirilən isteğe bağlı skriptlər
 * `config` debconf konfiqurasiya mexanizmini dəstəkləyən əlavə skriptdir.
 * `shlibs` - Bu, paylaşılan kitabxana asılılıqlarının siyahısıdır.

## İstinadlar

* [DEB - Vikipediya](https://en.wikipedia.org/wiki/Deb_(file_format))

* [Debian ikili paket formatı](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)


