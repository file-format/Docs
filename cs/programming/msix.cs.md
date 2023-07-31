{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - Co je soubor MSIX?",
  "description":"Další informace o souboru MSIX a rozhraních API, která mohou vytvářet a otevírat soubory MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Co je soubor MSIX?

Soubor MSIX je formát balení aplikací pro Windows, který se používá k vytváření a distribuci aplikací v systému Windows 10. Jedná se o moderní formát souboru balíčku ve srovnání s [APPX](/cs/programming/appx/) a MSI, který bude nakonec postupně vyřazen. do tohoto nového formátu souboru. Lze jej použít pro nasazení aplikací Win32, WPF a Windows Forms. Soubory MSIX jsou spolehlivé a optimalizují síť a místo na disku. Vývojáři je používají k distribuci programů koncovým uživatelům prostřednictvím obchodu Microsoft Store (dříve známého jako Windows Store).

## Formát souboru MSIX – Další informace

Soubory MSIX jsou komprimovány [ZIP](/cs/compression/zip/) a všechny soubory jsou obsaženy v zabaleném souboru. Kromě souborů souvisejících s aplikací obsahuje soubor MSIX konfigurační soubory [.xml](/cs/web/xml/), které obsahují informace související s instalací aplikace.

## Co je uvnitř balíčku MSIX?

Balíček MSIX se skládá z následujících souborů.

* `AppxBlockMap.xml` – Známý jako soubor mapy bloků balíčku, jde o dokument XML, který obsahuje seznam souborů aplikace s indexy a kryptografickými hodnotami hash pro každý blok dat uložený v balíčku.
* `AppxManifest.xml` – Dokument XML, který obsahuje informace požadované pro nasazení, zobrazení a aktualizaci aplikace MSIX. Tyto informace zahrnují identitu balíčku, závislosti balíčku, požadované schopnosti, vizuální prvky a body rozšiřitelnosti.
* `AppxSignature.p7x` - Soubor, který se vygeneruje při podpisu balíčku. Všechny balíčky MSIX musí být před instalací podepsány. S AppxBlockmap.xml je platforma schopna nainstalovat balíček a být ověřena.

## Reference

* [Přehled MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Vytvářejte soubory APPX pomocí Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

