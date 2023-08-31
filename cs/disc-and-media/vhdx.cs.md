{
  "date" : "2022-07-22",
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů VHDX a rozhraních API, která mohou vytvářet a otevírat soubory VHDX.",
  "title" :"Formát souboru VHDX - Co je soubor VHDX?",
  "linktitle" : "VHDX",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-07-22"
}

## Co je soubor VHDX?

Soubor VHDX je soubor obrazu disku ve formátu souboru Virtual Hard Disk v2. Obsahuje celý operační systém, který lze načíst a používat jako jakýkoli normální stroj pro testování softwaru nebo spouštění softwaru, který vyžaduje specifický operační systém. VHDX, přestože jde o úplný obraz disku, je uložen v jediném souboru. Software virtuálního stroje, jako je Parallels Desktop, Windows Virtual Machine a Virtual Box, může načíst a otevřít obraz disku.

Soubor VHDX lze převést na [VHD](/cs/disc-and-media/vhd/) pomocí Hyper-V Manager nebo na [VDI](/cs/disc-and-media/vdi/) pomocí VirtualBox.

## Formát souboru VHDX – Další informace

Podrobnosti o formátu souboru VHDX jsou kompletně zdokumentovány a dostupné online jako [Specifikace formátu souboru VHDX](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) v dokumentaci společnosti Microsoft. Jedná se o rozšíření formátu VHD a zahrnuje rozšířené možnosti. Formát souboru VHDX poskytuje další funkce, které jsou dostupné ve vrstvách souborů virtuálního pevného disku a virtuálního pevného disku. Je více optimalizovaný a poskytuje lepší výsledky pro konfiguraci hardwaru úložiště a možnosti. Soubory VHDX lze otevřít

### Podpora virtuálních pevných disků ve VHDX

Podporuje tři typy virtuálních pevných disků.

1. **Fixed Virtual Hard Disk** - Virtuální pevný disk s přidělenou pevnou velikostí dat. Velikost virtuálního pevného disku se přidáním nebo odebráním dat nemění.

1. **Dynamický virtuální pevný disk** – Virtuální pevný disk s dynamickou velikostí disku. Jeho velikost je kdykoli stejně velká jako skutečná data do něj zapsaná a metadata. Velikost jeho souboru se dynamicky zvyšuje, jak jsou do něj přidávána nebo odebírána data.

1. **Rozdílný virtuální pevný disk** – Představuje proud virtuálního pevného disku jako sadu upravených bloků ve srovnání s nadřazeným souborem virtuálního pevného disku.

## Reference

* [Specifikace formátu souboru VHDX](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD – z Wikipedie](https://en.wikipedia.org/wiki/VHD_(file_format))

