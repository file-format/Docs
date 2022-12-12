{
  "date" : "2022-06-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru SY_ - komprimovaný soubor SYS",
  "description":"Další informace o formátu souboru SY_ a rozhraních API, která mohou vytvářet a otevírat soubory SY_.",
  "linktitle" : "SY_",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-24"
}

## Co je soubor SY_?

Soubor SY_ je komprimovaný soubor .sys, který používají instalační programy softwaru ke zmenšení velikosti instalačních souborů zabalených v instalačním programu. Tím se sníží celková velikost instalačního programu. Soubory SY_ lze rozbalit pomocí nástroje příkazového řádku Microsoft Expand, který rozbalí jeden nebo více komprimovaných souborů.

## Formát souboru SY_ – Další informace

Soubory SY_ se ukládají na disk jako komprimované binární soubory. Jejich interní formát souborů však není veřejně dostupný. Nástroj příkazového řádku Microsoft Expand může rozbalit soubory SY_ pomocí jednoho z následujících příkazových řádků.

```
expand [/r] <source> <destination>
expand /r <source> [<destination>]
expand /i <source> [<destination>]
expand /d <source>.cab [/f:<files>]
expand <source>.cab /f:<files> <destination>
```
Po rozbalení se soubory SY_ převedou na soubor [SYS](https://docs.fileformat.com/system/sys/).

Soubory SY_ jsou podobné souborům EX_ a DL_.

## Reference

* [StuffIt – podle Wikipedie](https://en.wikipedia.org/wiki/StuffIt)
* [Microsoft Expand](https://docs.microsoft.com/en-us/windows-server/administration/windows-commands/expand)

