{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WHL-filformat - Python Wheel Package File",
  "description":"Läs mer om WHL-filformat och API:er som kan skapa och öppna WHL-filer.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## Vad är WHL fil?

En WHL-fil (Wheel) är en distributionspaketfil som sparas i Pythons hjulformat. Det är en installation i standardformat av Python-distributioner och innehåller alla filer och metadata som krävs för installation. WHL-filen innehåller också information om Python-versionerna och plattformarna som stöds av denna hjulfil. På samma sätt som en [MSI](/sv/executable/msi/)-installationsfil är WHL-filformatet ett färdigt-att-installationsformat som gör det möjligt att köra installationspaketet utan att bygga källdistributionen.

## WHL filformat

WHL-filformat är ett [ZIP](/sv/compression/zip/) (.zip)-arkiv som innehåller alla installationsfiler och metadata som krävs av installatörer för installation av ett paket. Dessa WHL-filer kan extraheras med hjälp av unzip-alternativet eller standardprogram för dekomprimering som WinZIP och WinRAR.

### WHL-filnamnskonvention

En WHL-fil namnges enligt följande konvention.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Ett exempel på WHL-filnamnet är följande.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `kryptografi` är paketnamnet.
* `2.9.2` är paketversionen av kryptografi. En version är en PEP 440-kompatibel sträng såsom 2.9.2, 3.4 eller 3.9.0.a3.
* `cp35` är Python-taggen och anger Python-implementeringen och versionen som hjulet kräver.
* `abi3` är ABI-taggen. ABI står för application binary interface.
* `macosx_10_9_x86_64` är plattformstaggen, vilket råkar vara en hel mun.

## Referenser

* [Vad är Python-hjul och varför bör du bry dig?](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)

