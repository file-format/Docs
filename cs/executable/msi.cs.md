{
  "date" : "2021-06-30",
  "keywords" :[ "soubor msi", "formát souboru MSI", "co je soubor msi", "soubor", "příklad msi", "přípona souboru msi", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů MSI a rozhraních API, která mohou vytvářet a otevírat soubory MSI.",
  "title" :"MSI - Windows Installer Package File",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## Co je soubor MSI?
Soubor MSI používaný k instalaci a spouštění programů Windows; kompletní balíček pro Microsoft Windows, který obsahuje instalační informace pro typický softwarový program, včetně základních souborů k instalaci a informací o umístění instalace. Soubory MSI mohou také obsahovat balíček pro aktualizace softwaru. Soubory MSI jsou podobné jako [EXE](/cs/executable/exe/), ale EXE někdy nemusí obsahovat informace o instalaci a softwarový program se může spustit přímo při spuštění souboru EXE.

## Formát souboru MSI
Instalační služba Windows Installer je ve skutečnosti rozhraní API (Application Programming Interface) a softwarová součást systému Microsoft Windows, která se používá k instalaci, odebrání a údržbě softwarového programu. Instalační informace a volitelné soubory jsou zabaleny jako instalační balíčky a volně relační databáze strukturované jako COM Structured Storages; dobře známé jako **soubory MSI** s příponou .msi. Balíčky s příponou **.mst** obsahují **Transformační skripty** Instalační služby systému Windows, soubory s příponou **.msm** obsahují **Merge Modules** a příponu souboru **.pcp** se používá pro **Vlastnosti vytváření záplat**. Instalační služba Windows Installer se stává pokročilejší poté, co došlo k významným změnám oproti dřívějším verzím, Setup API. Rámec GUI a automatické generování sekvence odinstalace jsou nové funkce Instalační služby systému Windows. Nyní byl zvažován jako alternativa k samostatným spustitelným instalačním rámcům.

### Logická struktura MSI balíčků
Balíček označuje instalaci jednoho nebo více úplných produktů a je obecně identifikován pomocí **GUID**. Produkt se skládá z jedné nebo více komponent a seskupených do různých funkcí. Instalační služba Windows Installer nezpracovává závislosti mezi různými produkty současně. Logická struktura balíčků se skládá z následujících prvků:

- **Produkty**: Jeden nainstalovaný fungující program nebo sada více programů spojených dohromady je produkt. Produkt je identifikován jedinečným GUID.
- **Funkce**: Může obsahovat libovolný počet součástí a dalších dílčích funkcí. Menší balíčky se mohou skládat z jediné funkce.
- **Komponenty**: Instalační služba Windows Installer považuje komponentu za jednotku; může obsahovat programové soubory, složky, klíče registru, součásti COM a zástupce.
- **Klíčové cesty**: Cesta klíče je konkrétní soubor, zdroj dat ODBC nebo klíč registru, který autor balíčku určí jako kritický pro danou komponentu.

## Reference

* [Windows Installer – od Wikipedie](https://en.wikipedia.org/wiki/Windows_Installer)


