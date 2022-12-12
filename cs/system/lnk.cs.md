{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "rozšíření", "soubor", "formát", "systém", "soubor LNK", "odkaz", "soubory LNK", "dokumenty LNK", "aplikace", "programy" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Link File Format",
  "description":"Další informace o formátu souborů LNK a rozhraních API, která mohou vytvářet a otevírat soubory LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## Co je soubor LNK? ##

Soubor LNK, analogický s identitou v systému Mac, je alternativou systému Windows nebo „odkazem“, který slouží jako připojení k původní složce dokumentů s obrázky nebo programu. Obsahuje typ, pozici a název souboru zástupce, stejně jako aplikaci, která otevře cílový dokument, a další klávesovou zkratku.

Ve Windows rovnou soubor, složku nebo spustitelný program a zvolte Vytvořit zástupce. Umístění formátu souboru a adresář „Začátek“ jsou dvě základní vlastnosti souborů LNK. Formát souboru souborů LNK je maskovaný a zakřivená šipka označuje, že se jedná o zástupce.

## Formát souboru LNK ##

Formáty souborů LNK mají obvykle stejnou ikonu jako jejich cílové soubory, ale s přidáním malé zvlněné šipky, která ukazuje, že soubor ukazuje na jiné místo. Když na zástupce dvakrát kliknete, chová se, jako by uživatel poklepal na skutečný soubor.

Soubory LNK obsahující zástupce aplikací mohou mít vlastnosti, které ovlivňují běh programu. Chcete-li změnit atributy, klikněte pravým tlačítkem na soubor zástupce a vyberte **Vlastnosti**, poté změňte pole Cíl.

Namísto přípon souborů jsou soubory LNK příponami Průzkumníka Windows. Jako terminálové rozšíření lze dokumenty .lnk použít pouze v Průzkumníkovi Windows k nahrazení souboru a v Průzkumníkovi Windows mají jiné účely kromě toho, že slouží jako zástupce místního dokumentu. Tyto soubory také začínají písmenem "L".

Zatímco zástupci odkazují na konkrétní soubory a adresáře, když jsou vytvořeny, mohou se stát nefunkčními, pokud se cíl změní na jiné umístění. Průzkumník začne opravovat složku zástupců, která při otevření ukazuje na mrtvý cíl.


## Technická specifikace ##

Pouze v případě, že není zaškrtnuto nastavení zobrazení složky "Skrýt přípony pro rozpoznané typy souborů", systém Windows nezobrazí příponu dokumentu .lnk pro zástupce dokumentů. I když to není doporučeno, můžete povolit zobrazení přípony souboru odebráním vlastnosti "NeverShowExt" z položky registru Windows souboru HKEY_CLASSES_ROOT\lnk.

Chcete-li tak učinit, postupujte takto:

* Otevřete "Registration Editor" zadáním "Regedit" do vyhledávacího pole na hlavním panelu a výběrem programu
* V aplikaci přejděte do umístění Počítač\HKEY HKEY_CLASSES_ROOT\lnkfile
* Vytvořte zálohu položky tak, že na ni kliknete pravým tlačítkem a zvolíte Exportovat
* Vyberte a odstraňte atribut "NeverShowExt".
* Windows by měl být restartován


## reference ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
