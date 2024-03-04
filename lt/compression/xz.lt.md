{
  "date": "2022-01-23",
  "keywords": [
"xz failą",
"Dokumento formatas",
"kas yra xz failas",
"failą",
"xz pavyzdys",
"xz failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "XZ failas – XZ suspaustas archyvas",
  "description": "Sužinokite apie XZ failo formatą ir API, kurios gali kurti ir atidaryti XZ failus.",
  "linktitle": "XZ",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-x-ltz"
}
},
  "lastmod": "2022-01-23"
}

## Kas yra XZ failas?

XZ yra suspausto failo formatas, kuriame naudojamas LZMA2 glaudinimo algoritmas. Jis buvo sukurtas kaip populiarių gzip ir bzip2 formatų pakaitalas ir turi daug pranašumų, palyginti su šiais senesniais standartais. XZ failai yra gerai palaikomi daugelyje platformų ir gali būti greitai ir lengvai išskleisti. Nors XZ archyvai nėra tokie įprasti kaip [ZIP](/compression/zip/) arba [RAR](/compression/rar/) failai, XZ archyvai gali būti naudojami dideliems duomenų kiekiams saugoti neprarandant glaudinimo kokybės. Jei reikia suspausti arba išskleisti didelius failus, verta apsvarstyti XZ failo plėtinį.

## XZ failo formatas

XZ failai generuojami ir išsaugomi diske kaip dvejetainiai failai. Duomenims suspausti naudojamas LZMA algoritmas ir gali pasiekti iki 50 % suspaudimo koeficientą. XZ failai paprastai naudojami programinės įrangos platinimui ir atsarginių kopijų archyvams. Juos galima išspausti naudojant XZ įrankį, kuris yra daugelyje Linux platinimų.

## Išpakuokite XZ failus Linux / Unix

Norėdami išpakuoti XZ failus, pirmiausia įdiekite paketą xz-utils:
```
$ sudo apt-get install xz-utils
```

Norėdami išskleisti .xz failus, naudokite komandą unxz:
```
$ unxz compressed_xz_file.xz
```

arba naudojant XZ parinktį --decompress:
```
$ xz --decompress compressed_xz_file.xz
```

## Nuorodos

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)


