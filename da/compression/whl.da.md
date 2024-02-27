{
  "date": "2022-06-29",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WHL-filformat - Python-hjulpakkefil",
  "description": "Lær om WHL filformat og API'er, der kan oprette og åbne WHL filer.",
  "linktitle": "WHL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-wh-dal"
}
},
  "lastmod": "2022-06-29"
}

## Hvad er WHL fil?

En WHL (Wheel) fil er en distributionspakkefil gemt i Pythons hjulformat. Det er en standardformatinstallation af Python-distributioner og indeholder alle de filer og metadata, der kræves til installationen. WHL-filen indeholder også oplysninger om Python-versionerne og -platformene, der understøttes af denne hjulfil. I lighed med en [MSI](/executable/msi/)-opsætningsfil, er WHL-filformatet et format, der er klar til installation, der tillader at køre installationspakken uden at bygge kildedistributionen.

## WHL filformat

WHL-filformatet er et [ZIP](/compression/zip/) (.zip)-arkiv, der indeholder alle installationsfiler og metadata, der kræves af installatører til installation af en pakke. Disse WHL-filer kan udpakkes ved hjælp af unzip-option eller standard dekomprimeringssoftwareapplikationer såsom WinZIP og WinRAR.

### WHL-filnavnekonvention

En WHL-fil er navngivet i henhold til følgende konvention.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Et eksempel på WHL-filnavnet er som følger.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

 * `kryptografi` er pakkenavnet.
 * `2.9.2` er pakkeversionen af kryptografi. En version er en PEP 440-kompatibel streng såsom 2.9.2, 3.4 eller 3.9.0.a3.
 * `cp35` er Python-tagget og angiver den Python-implementering og version, som hjulet kræver.
 * `abi3` er ABI-tagget. ABI står for application binary interface.
 * `macosx_10_9_x86_64` er platformsmærket, som tilfældigvis er noget af en mundfuld.

## Referencer

* [Hvad er Python-hjul, og hvorfor skulle du være ligeglad?](https://realpython.com/python-wheels/)

* [Python Wheel](https://pypi.org/project/wheel/)


