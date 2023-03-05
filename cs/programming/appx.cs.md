{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - Co je soubor APPX?",
  "description":"Další informace o formátu souboru APPX a rozhraních API, která mohou vytvářet a otevírat soubory APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## Co je soubor APPX?

Soubor APPX je distribuovatelný formát souboru balíčku, který se používá pro distribuci a instalaci aplikace. Byl představen s Windows 8, který má být zveřejněn na Microsoft Windows Store. Obsahuje všechny soubory potřebné k instalaci aplikace Windows. Patří mezi ně metadata, soubory a informace o přihlašovacích údajích. Modernějším formátem balicích souborů je MSIX, který se v současnosti běžněji používá ve srovnání s APPX.

## Formát souboru APPX – Další informace

Soubory APPX se ukládají jako komprimované soubory ve formátu souboru [ZIP](/cs/compression/zip/). Díky tomu je celý balíček jako archivní soubor s menší velikostí souboru, který lze snadno nahrát do obchodu Microsoft Store.

## Jak zobrazit soubory v souboru APPX?

Chcete-li zobrazit obsah nebo soubory v souboru APPX, měli byste postupovat podle následujících kroků.

1. Protože soubory APPX jsou uloženy jako komprimované soubory ZIP, přejmenujte soubor na příponu .zip
1. Pomocí libovolného dekompresního nástroje, jako je 7-Zip, WinZip nebo WinRAR, extrahujte soubory obsažené v souboru APPX

## Jak vytvořit soubor APPX?

Existují dvě metody, které lze použít k vytvoření souborů APPX.

1. Pomocí MakeApp.exe – [MakeApp.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) se používá k vytvoření obou balíčky aplikací (.msix nebo .appx) a soubory balíčků aplikací .msixbundle nebo .appxbundle). Kromě toho může extrahovat soubory z balíčku aplikace. MakeApp.exe je k dispozici s Windows 10 SDK a lze jej použít z příkazového řádku.
1. Použití Microsoft Visual Studio – Vývojáři obvykle [vytvářejí soubory APPX](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) pomocí Microsoft Visual Studio. Jakmile je vývoj aplikace dokončen a aplikace je připravena k publikování, lze vytvořit soubor balíčku APPX jeho publikováním v sadě Visual Studio.

## Reference

* [Vytvořte balíček nebo balíček MSIX pomocí MakeAppx.exe](https://docs.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Vytvářejte soubory APPX pomocí Microsoft Visual Studio](https://docs.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

