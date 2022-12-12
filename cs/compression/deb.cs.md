{
  "date" : "2021-04-08",
  "keywords" :[ "soubor deb", "formát souboru deb", "co je soubor deb", "soubor", "příklad deb", "přípona souboru deb", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DEB - Bzip Compressed Tar Archive",
  "description":"Další informace o formátu souboru DEB a rozhraních API, která mohou vytvářet a otevírat soubory DEB.",
  "linktitle" : "DEB",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Co je soubor DEB?

Soubor s příponou .deb je formát binárního balíčku Debianu dostupný pro distribuci softwarových balíčků na OS Linux. Skládá se ze dvou archivních souborů [TAR](/cs/compression/tar/). DPKG poskytuje mechanismus pro čtení a instalaci balíčků DEB. Balíčky DEB lze nainstalovat pomocí rozhraní pro správu softwaru balíků APT. Soubory DEB mají typ internetového média `application/vnd.debian.binary-package`.

## Formát souboru DEB

Soubor DEB se skládá ze dvou archivních souborů [TAR](/cs/compression/tar/). Jeden archiv obsahuje řídicí informace a druhý obsahuje instalovatelná data.

### Organizace balíčků

Soubor DEB je archivní soubor **ar**, který má magickou hodnotu `!<arch> `. Od Debianu 0.93 obsahuje mechanismus archivace souborů DEB tři soubory v určitém pořadí.

1. `Debian Binary` - Je určen k tomu, aby měl řadu řádků oddělených novými řádky. V současnosti je k dispozici pouze jeden řádek, který popisuje číslo verze. Aktuální číslo verze je 2.0.
1. `Control Archive` - Obsahuje archiv control.tar, který obsahuje skripty správce a metainformace o balíčku, jako je název balíčku, verze, závislosti a správce.
1. `Archiv dat` - Je to archiv tar s názvem data.tar a obsahuje aktuální instalovatelné mediální soubory. Archiv lze komprimovat pomocí gz, bz2, lzma nebo xz a přípona souboru datového archivu se odpovídajícím způsobem změní.

### Kontrolní archiv

Řídicí archiv může obsahovat následující obsah.

* `control` - Obsahuje stručný popis balíčku a také další informace, jako jsou jeho závislosti.
* `md5sums` - Obsahuje MD5 kontrolní součty všech souborů v balíčku, aby bylo možné detekovat poškozené nebo neúplné soubory.
* `conffiles` - Vypisuje soubory balíčku, které by měly být považovány za konfigurační soubory. Konfigurační soubory nejsou během aktualizace přepsány, pokud není uvedeno jinak.
* `preinst`, postinst, prerm a postrm – volitelné skripty, které se spouštějí před nebo po instalaci nebo odstranění balíčku
* `config` je volitelný skript, který podporuje konfigurační mechanismus debconf.
* `shlibs` - Je to seznam závislostí sdílené knihovny.

## Reference

* [DEB – Wikipedie](https://en.wikipedia.org/wiki/Deb_(formát_souboru))
* [Formát binárního balíčku Debianu](https://manpages.debian.org/buster/dpkg-dev/deb.5.en.html)

