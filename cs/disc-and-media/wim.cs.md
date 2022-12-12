{
  "date" : "2021-08-11",
  "keywords" :[ "soubor wim", "formát souboru wim", "co je soubor wim", "soubor", "příklad wim", "přípona souboru wim", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Další informace o formátu souborů WIM a rozhraních API, která mohou vytvářet a otevírat soubory WIM.",
  "title" :"WIM - Windows Imaging Format File",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## Co je soubor WIM?
Soubory s příponou .wim byly poprvé viděny ve Windows Vista. WIM patří k obrazovému formátu založenému na souborech, který byl obvykle zaveden v systému Microsoft Windows Vista. Umožňuje nasazení jednoho obrazu disku na různé počítačové platformy. Soubory WIM se používají ke správě souborů, jako jsou aktualizace, ovladače a součásti, aniž by bylo nutné znovu spouštět bitovou kopii operačního systému. Soubor AQ WIM obsahuje sadu souborů a souvisejících metadat, která jsou velmi podobná jiným formátům souborů na disku.

## formáty souborů WIM
Formát souboru WIM není jako formáty založené na sektorech, jako je VHD nebo IS, ve skutečnosti je založen na souborech, což znamená, že základní jednotkou informací ve WIM je soubor. Základní výhodou založené na souborech je to, že jednoinstanční úložiště souboru odkazovaného vícekrát ve stromu souborového systému a nezávislost na hardwaru. Snižuje režii otevírání a zavírání různých souborů jednotlivě, protože soubory jsou uloženy v jediném WIM soubor. Soubory WIM mohou ukládat více diskových obrazů, na které se odkazuje buď jejich jedinečným názvem nebo číselným indexem.
### Podpora kompresních algoritmů
WIM podporuje následující rodiny kompresních algoritmů v sestupné rychlosti a vzestupném poměru:
- XPRESS
- LZX
- LZMS
- Solid-komprese.
První tři rodiny jsou založené na LZ77, zatímco Solid-compression byly představeny spolu s LZMS ve WIMGAPI Windows 8 a DISM Windows 8.1.
### Nástroje pro formát souboru WIM
Následující nástroje obvykle podporují formát souboru WIM:

- **ImageX**: Nástroj příkazového řádku používaný k úpravě, vytváření a nasazení bitových kopií disku Windows ve formátu Windows Imaging Format. Spolu s příslušným WIMGAPI je distribuován jako součást bezplatné Windows Automated Installation Kit. Počínaje systémem Windows Vista používá instalační program systému Windows k instalaci systému Windows rozhraní WAIK API.
- **DISM**: Nástroj představený v systémech Windows 7 a Windows Server 2008 R2, který může provádět úlohy související se službami na bitové kopii instalace Windows, ať už se jedná o online bitovou kopii nebo offline bitovou kopii ve složce nebo souboru WIM. tento nástroj byl schopen připojovat a odpojovat obrazy, přidávat ovladač zařízení do obrazu offline a dotazovat se na nainstalované ovladače zařízení v obraze offline.
 




## Reference


* [Windows Imaging Format – z Wikipedie](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


