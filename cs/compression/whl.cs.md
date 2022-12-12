{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru WHL - soubor balíčku Python Wheel",
  "description":"Další informace o formátu souborů WHL a rozhraních API, která mohou vytvářet a otevírat soubory WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Co je soubor WHL?

Soubor WHL (Wheel) je soubor distribučního balíčku uložený ve formátu kola Pythonu. Jedná se o standardní formátovou instalaci distribucí Pythonu a obsahuje všechny soubory a metadata potřebná pro instalaci. Soubor WHL také obsahuje informace o verzích Pythonu a platformách podporovaných tímto souborem kola. Podobně jako instalační soubor [MSI](/cs/executable/msi/), formát souboru WHL je formát připravený k instalaci, který umožňuje spuštění instalačního balíčku bez vytváření zdrojové distribuce.

## Formát souboru WHL

Formát souboru WHL je archiv [ZIP](/cs/compression/zip/) (.zip), který obsahuje všechny instalační soubory a metadata vyžadovaná instalačními programy pro instalaci balíčku. Tyto soubory WHL lze extrahovat pomocí možnosti rozbalení nebo standardních dekompresních softwarových aplikací, jako jsou WinZIP a WinRAR.

### Konvence názvů souborů WHL

Soubor WHL je pojmenován podle následující konvence.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Příklad názvu souboru WHL je následující.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `cryptography` je název balíčku.
* `2.9.2` je verze balíčku kryptografie. Verze je řetězec vyhovující PEP 440, například 2.9.2, 3.4 nebo 3.9.0.a3.
* `cp35` je značka Pythonu a označuje implementaci a verzi Pythonu, kterou kolo vyžaduje.
* `abi3` je značka ABI. ABI je zkratka pro aplikační binární rozhraní.
* `macosx_10_9_x86_64` je značka platformy, která je náhodou docela sousto.

## Reference

* [Co jsou Python Wheels a proč by vás to mělo zajímat?](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)

