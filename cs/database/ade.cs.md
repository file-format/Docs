{
  "date" : "2021-08-29",
  "keywords" :[ "ade", "přípona", "soubor", "formát souboru", "Typ databázového souboru", "Formát databázového souboru", "Microsoft Access" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru ADE a rozhraních API, která mohou vytvářet a otevírat soubory ADE.",
  "title" :"ADE - Access Project Extension File",
  "linktitle" : "ADE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-08-29"
}

## Co je soubor ADE?

Soubor s příponou .ade je soubor projektu Microsoft Access, který obsahuje kompilovaný výstup informací obsažených v souboru projektu Microsoft Access ADP. Informace v souboru projektu Access, jiné než Visual Basic for Applications (VBA), jsou k dispozici v kompilované podobě v souborech ADE. Data jsou v těchto souborech uložena v komprimovaném formátu, aby se zmenšila velikost souboru a zlepšil výkon v Accessu. Vzhledem k tomu, že ADE je zkompilovaným výstupem souboru projektu Access, jakýkoli zdrojový kód VBA, který je součástí projektu, zůstává chráněn tím, že není součástí výstupu. Soubory ADE lze otevřít v aplikaci Microsoft Access 365.

## Formát souboru ADE - Další informace

ADE jsou kompilované soubory databáze Access, které se ukládají na disk jako binární soubory. Vnitřní struktura souborů těchto souborů není známa.

Soubory ADE mohou způsobit problémy při otevírání na základě verze aplikace Microsoft Access, která byla použita k vytvoření těchto souborů. Databáze aplikace Access, které používají 64bitovou verzi Microsoft Access 2010 a které jsou zkompilovány jako soubory MDE, [ACCDE](/cs/database/accde/) nebo ADE, musí být znovu zkompilovány v Microsoft Access 2021 Service Pack 1 (SP1), aby správně pracovat s Access 2010 SP1. K tomuto problému dochází, protože Access 2010 SP1 používá novější verzi souboru VBE7.dll (verze 7.00.1619).

## Reference

* [Problém s přístupem k souborům ADE](https://learn.microsoft.com/en-us/office/troubleshoot/access/error-run-compiled-mde-accde-ade)
* [Jaké přístupové formáty souborů použít](https://support.microsoft.com/en-us/office/which-access-file-format-should-i-use-012d9ab3-d14c-479e-b617-be66f9070b41)

