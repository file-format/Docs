{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Přečtěte si o formátu souborů GCF a rozhraních API, která mohou vytvářet a otevírat soubory GCF.",
  "title" : "Soubor GCF – formát GCF hry Nadeo",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-cs",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Co je soubor GCF?

Soubor .gcf je soubor mezipaměti hry používaný herní platformou Steam. Obsahuje herní data, jako jsou textury, modely a další soubory, které hra používá. Tyto soubory jsou uloženy v počítači uživatele a používají se ke snížení množství dat, která je třeba stáhnout při aktualizaci nebo instalaci hry. Soubory .gcf lze také použít k vytvoření zálohy instalace hry nebo k přenosu hry mezi počítači.

Soubory GCF lze číst a zapisovat pomocí Open Source C++ programovací knihovny **HLLib**.

## Formát souboru GCF

Soubory GCF se ukládají na disk jako binární soubory. GCF byl původně používán jako zkratka pro Grid Cache File (počáteční kódové jméno Steamu bylo Grid), ale později bylo převzato jako Game Cache File. Soubor GCF je archivní soubor, který ukládá hry Steam. Veškerý oficiální obsah se stahuje jako soubory GCF. Soubory GCF lze také sdílet mezi hrami.

POZNÁMKA: GCF je předchůdcem [VPK file format](/game/vpk/).
## Reference

* [Software Valve](https://www.valvesoftware.com/en/)

* [Formát souboru GCF](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib – Open Source programovací knihovna C++ pro čtení souborů GCF](https://developer.valvesoftware.com/wiki/HLLib)


