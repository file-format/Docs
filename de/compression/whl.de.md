{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL-Dateiformat - Python-Wheel-Paketdatei",
  "description":"Erfahren Sie mehr über das WHL-Dateiformat und APIs, die WHL-Dateien erstellen und öffnen können.",
  "linktitle" :"WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Was ist eine WHL-Datei?

Eine WHL-Datei (Wheel) ist eine Distributionspaketdatei, die im Wheel-Format von Python gespeichert ist. Es ist eine Installation im Standardformat von Python-Distributionen und enthält alle Dateien und Metadaten, die für die Installation erforderlich sind. Die WHL-Datei enthält auch Informationen zu den Python-Versionen und -Plattformen, die von dieser Wheel-Datei unterstützt werden. Ähnlich wie eine [MSI](/de/executable/msi/)-Setup-Datei ist das WHL-Dateiformat ein sofort installierbares Format, das es ermöglicht, das Installationspaket auszuführen, ohne die Quelldistribution zu erstellen.

## WHL-Dateiformat

Das WHL-Dateiformat ist ein [ZIP](/de/compression/zip/) (.zip)-Archiv, das alle Installationsdateien und Metadaten enthält, die von Installern für die Installation eines Pakets benötigt werden. Diese WHL-Dateien können mit der Unzip-Option oder standardmäßigen Dekomprimierungssoftwareanwendungen wie WinZIP und WinRAR extrahiert werden.

### Konvention für WHL-Dateinamen

Eine WHL-Datei wird gemäß der folgenden Konvention benannt.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Ein Beispiel für den WHL-Dateinamen lautet wie folgt.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* „cryptography“ ist der Paketname.
* „2.9.2“ ist die Paketversion der Kryptografie. Eine Version ist eine PEP 440-kompatible Zeichenfolge wie 2.9.2, 3.4 oder 3.9.0.a3.
* „cp35“ ist das Python-Tag und bezeichnet die Python-Implementierung und -Version, die das Rad erfordert.
* „abi3“ ist das ABI-Tag. ABI steht für Application Binary Interface.
* `macosx_10_9_x86_64` ist das Plattform-Tag, was zufällig ein ziemlicher Bissen ist.

## Verweise

* [Was sind Python-Räder und warum sollten Sie sich darum kümmern?](https://realpython.com/python-wheels/)
* [Python-Rad](https://pypi.org/project/wheel/)

