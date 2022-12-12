{
  "date" : "2021-08-13",
  "keywords" :[ "soubor sdi", "formát souboru sdi", "co je soubor sdi", "soubor", "příklad sdi", "přípona souboru sdi", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů SDI a rozhraních API, která mohou vytvářet a otevírat soubory SDI.",
  "title" :"SDI - soubor obrazu nasazení systému Windows",
  "linktitle" : "SDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-13"
}

## Co je soubor SDI?
Soubor s příponou .sdi obsahuje load blob, boot blob a part blob; běžně používaný Windows Embedded Studio k vytvoření RAM disků nebo spouštěcích disků pro načítání a instalaci Windows. SDI je zkráceno pro System Deployment Image. Windows Embedded Studio je program používaný k vytváření obrazů disků pro Windows. Tento program ve skutečnosti obsahuje program SDI File Manager a nástroj příkazového řádku nazvaný **sdimgr.exe**, oba lze použít k načítání, vytváření a úpravě obrázků SDI.

## Formát souboru SDI
Formát souboru SDI je široce používán k umožnění použití virtuálního disku pro spouštění systému. Některé verze systému Microsoft Windows umožňují **bootování z paměti RAM**, což je důležité pro načtení souboru SDI do paměti a následné spuštění z něj. Formát souboru SDI také umožňuje zavádění ze sítě pomocí PXE (Preboot Execution Environment). Používá se také pro zobrazování na pevném disku.
### Sekce souborů SDI
Samotný soubor SDI lze rozdělit do následujících částí:
- **Boot BLOB**: Obsahuje skutečný spouštěcí program STARTROM.COM. Jedná se o analogii spouštěcího sektoru pevného disku.
- **Load BLOB**: Obvykle obsahuje NTLDR a spouští se spouštěcím objektem BLOB.
- **Část BLOB**: Obsahuje aktuální dobu spuštění; obsahuje také soubory boot.ini a ntdetect.com, které by měly být umístěny v kořenovém adresáři běhového prostředí.
- **Disk BLOB**: Toto je plochý obraz HDD začínající MBR. Používá se pro zobrazení obrazu na pevném disku místo spouštění. Pomocí nástrojů společnosti Microsoft lze také připojit pouze objekty BLOB disku.


## Reference

* [Image Deployment Image – od Wikipedie](https://en.wikipedia.org/wiki/System_Deployment_Image)


