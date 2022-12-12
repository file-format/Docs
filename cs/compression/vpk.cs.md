{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VPK File - PlayStation Vita Application Package File Format",
  "description":"Další informace o formátu souborů VPK a rozhraních API, která mohou vytvářet a otevírat soubory VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## Co je soubor VPK?

Soubor s příponou .vpk je komprimovaný soubor archivního balíčku, který se používá k instalaci aplikací třetích stran na herní konzoli Sony PlayStation Vita. Tyto soubory lze nainstalovat pouze na útěk z vězení Vita PlayStation od HENkaku, který umožnil PS Vita a PSTV používat přizpůsobený obsah vytvořený uživateli. Archivní soubor VPK obsahuje veškerý obsah, který tvoří hru, včetně obrázků, jako jsou soubory [PNG](/cs/image/png/), soubory nastavení, jako je [.bin](/cs/disc-and-media/bin/) a jakékoli konfigurace ve formátu souboru [XML](/cs/web/xml/).

## Formát souboru VPK

Soubory VPK se ukládají na disk jako standardní komprimované archivy [ZIP](/cs/compression/zip/). Ty mohou obsahovat více složek a dalších přidružených souborů pro aplikace třetích stran, které se mají nainstalovat do Vita Gaming Console. Chcete-li zobrazit obsah souboru balíčku VPK, přejmenujte jeho příponu z .vpu na .zip a extrahujte obsah pomocí standardních dekompresních nástrojů, jako je WinZip nebo WinRAR.

Valvesoftware má podrobné informace o [formátu souboru VPK] (https://developer.valvesoftware.com/wiki/VPK_File_Format), na který lze odkazovat z pohledu vývojáře.

## Jak nainstalovat soubory VPK?

Soubory VPK lze nainstalovat z nástroje příkazového řádku VPK.exe. V OS Windows mohou být soubory vynechány na soubor vpk.exe, který vrátí \*.vpk obsahující všechny zabalené soubory. Alternativně lze nástroj příkazového řádku použít následovně.

### Vytvořte VPK a přidejte soubory

```
vpk <dirname>
```

### Extrahujte soubory VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Prohlížeč VPK

* [Prohlížeč VRF VPK](https://github.com/SteamDatabase/ValveResourceFormat)

## Reference

* [Formát souboru VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [Soubory VPK](https://developer.valvesoftware.com/wiki/VPK)

