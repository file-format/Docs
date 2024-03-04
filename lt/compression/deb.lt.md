{
  "date": "2021-04-08",
  "keywords": [
"deb failą",
"deb failo formatas",
"kas yra deb failas",
"failą",
"deb pavyzdys",
"deb failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DEB – Bzip suspausto deguto archyvas",
  "description": "Sužinokite apie DEB failo formatą ir API, kurios gali kurti ir atidaryti DEB failus.",
  "linktitle": "DEB",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-de-ltb"
}
},
  "lastmod": "2021-04-09"
}

## Kas yra DEB failas?

Failas su plėtiniu .deb yra Debiano dvejetainio paketo failo formatas, skirtas programinės įrangos paketams platinti Linux OS. Jį sudaro du [TAR](/compression/tar/) archyvo failai. DPKG suteikia DEB paketų skaitymo ir įdiegimo mechanizmą. DEB paketus galima įdiegti naudojant APT paketo programinės įrangos valdymo sąsają. DEB failų interneto medijos tipas yra application/vnd.debian.binary-package.

## DEB failo formatas

DEB failą sudaro du [TAR](/compression/tar/) archyvo failai. Viename archyve saugoma valdymo informacija, o kitame – įdiegtini duomenys.

### Paketo organizavimas

DEB failas yra **ar** archyvo failas, kurio magiška vertė yra `!<arch> `. Nuo Debian 0.93, DEB failų archyvavimo mechanizme yra trys failai tam tikra tvarka.

 1. Debian Binary – jai skirta eilučių serija, atskirta naujomis eilutėmis. Šiuo metu yra tik viena eilutė, apibūdinanti versijos numerį. Dabartinės versijos numeris yra 2.0.
 1. Valdymo archyvas – jame yra control.tar archyvas, kuriame yra prižiūrėtojo scenarijai ir metainformacija apie paketą, pvz., paketo pavadinimas, versija, priklausomybės ir prižiūrėtojas.
 1. Duomenų archyvas – tai taros archyvas, pavadintas data.tar, kuriame yra tikrieji įdiegiami medijos failai. Archyvas gali būti suglaudintas gz, bz2, lzma arba xz, atitinkamai keičiasi duomenų archyvo failo plėtinys.

### Valdymo archyvas

Valdymo archyve gali būti toks turinys.

 * `control` - It contains a brief description of the package as well as other information such as its dependencies.
 * md5sums – jame yra visų pakete esančių failų MD5 kontrolinės sumos, kad būtų galima aptikti sugadintus arba neužbaigtus failus.
 * conffiles – išvardija paketo failus, kurie turėtų būti traktuojami kaip konfigūracijos failai. Konfigūracijos failai naujinimo metu neperrašomi, nebent nurodyta.
 * preinst, postinst, prerm ir postrm – pasirenkami scenarijai, vykdomi prieš arba po paketo įdiegimo ar pašalinimo
 * config yra pasirenkamas scenarijus, palaikantis debconf konfigūracijos mechanizmą.
 * shlibs – tai bendrinamos bibliotekos priklausomybių sąrašas.

## Nuorodos

* [DEB – Vikipedija](https://en.wikipedia.org/wiki/Deb_(file_format))

* [Debiano dvejetainio paketo formatas](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)


