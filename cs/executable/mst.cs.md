{
  "date" : "2021-06-30",
  "keywords" :[ "soubor mst", "formát souboru mst", "co je soubor mst", "soubor", "příklad mst", "přípona souboru mst", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru MST a rozhraních API, která mohou vytvářet a otevírat soubory MST.",
  "title" :"MST - Windows Installer Package File",
  "linktitle" : "MST",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Co je soubor MST?
Soubory s příponou .mst se používají k transformaci obsahu balíčku MSI. Obvykle je používají správci systému k použití vlastních nastavení na existující soubor MSI. Soubory MST se používají společně s původním balíčkem MSI v jejich systémech distribuce softwaru, jako jsou zásady skupiny. Soubory MST se obecně používají při vývoji softwaru a testování pro konfiguraci jejich vyvíjených verzí softwaru.

## Formát souboru MST
Soubor MST nebo Transform se používá ke shromáždění možností instalace pro programy, které používají Instalační službu systému Microsoft Windows, do souboru. Tyto soubory se běžně používají na příkazovém řádku instalačního programu (MSIEXEC.EXE) nebo se používají v zásadách skupiny při instalaci softwaru; v doméně Microsoft Active Directory. Soubory MST lze také použít s zabalenými spustitelnými instalačními programy. Obecným případem je, že někdo chce předat parametry příkazového řádku zabalenému instalačnímu programu. K tomu potřebujete soubor MST, který přidá vlastnost WRAPPED_ARGUMENTS do tabulky vlastností. Tyto soubory nelze vytvářet ani upravovat pomocí obecných editorů. Pro tento účel jsou k dispozici specifické nástroje.

### Jak používat soubory MST?
Soubory MST lze generovat pomocí různých nástrojů a Ocra se obecně používá ke generování souborů MST. Poté lze nastavení upravit podle potřeby a uložit je na konkrétní místo. Poté mohou být soubory MST použity ve spojení se soubory MSI. Pokud chcete tyto soubory otestovat; použijte následující syntaxi na příkazovém řádku

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### Vlastnost TRANSFORMS

Můžete také použít vlastnost **TRANSFORMS** instalačního programu Windows, což je ve skutečnosti seznam transformací, které instalační program použije při instalaci balíčku. Instalační program provede transformace ve stejném pořadí, v jakém jsou uvedeny ve vlastnosti TRANSFORM. Transformace mohou být specifikovány názvem souboru s příponou .mst nebo úplnou cestou. Chcete-li zadat více než jednu transformaci, oddělte každý název souboru nebo středníkem jako v následujícím příkladu.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## Reference

* [MST Transformation Files](https://www.exemsi.com/documentation/mst-transformation-files/)
* [Vlastnost TRANSFORMS](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)


