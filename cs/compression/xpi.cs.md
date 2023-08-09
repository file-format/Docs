{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - soubor instalačního balíčku pro různé platformy",
  "description":"Další informace o formátu souboru XPI a rozhraních API, která mohou vytvářet a otevírat soubory XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## Co je soubor XPI?

Soubor XPI je instalační archiv, který je komprimován, aby se zmenšila velikost souboru. Používají jej aplikace Mozilla pro instalaci pluginů a doplňkových souborů. Obsahuje instalační skript nebo manifest v kořenovém adresáři souboru spolu s řadou datových souborů. Soubor XPI může obsahovat motivy, sadu nástrojů nebo pluginy Firefoxu, které si uživatel může nainstalovat a stát se součástí prohlížeče Firefox, Thunderbird nebo SeaMonkey.

## Formát souboru XPI – Další informace

Soubory XPI se ukládají na disk jako archivy [ZIP](/cs/compression/zip/), které kombinují více souborů do jednoho komprimovaného souboru. Soubory uvnitř souboru XPI mohou zahrnovat soubor instalačního skriptu, jako je JS, a webové soubory, jako je [CSS](/cs/web/css/), [HTML](/cs/web/html/) a [JSON](/cs/web/json/ ). Někdy může obsahovat také obrazové soubory [PNG](/cs/image/png/), které se doplňkem použijí jako ikony.

### Jak zobrazit obsah souboru XPI?

Soubor XPI je prakticky archiv ZIP, jehož obsah lze zobrazit pomocí následujících kroků.

* Změňte příponu souboru z XPI na ZIP
* Extrahujte obsah souboru pomocí libovolného standardního dekompresního nástroje, jako je WinZip (Windows, Mac), 7-Zip (Windows) nebo Apple Archive Utility (Mac).

### Nainstalujte soubor XPI na Firefox Android

Lidé jsou většinou zvědaví, zda lze soubory XPI nainstalovat do Firefoxu na zařízeních Android. V systému Android můžete nainstalovat doplněk ze souboru XPI tak, že soubor vyhledáte a otevřete ve Firefoxu.

## Reference

* [XPIInstall – Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Jak mohu otevřít rozšíření souboru XPI?](https://support.mozilla.org/en-US/questions/1009049)

