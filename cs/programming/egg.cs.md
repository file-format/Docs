{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru EGG - distribuční soubor Pythonu",
  "description":"Další informace o formátu souboru EGG a rozhraních API, která mohou vytvářet a otevírat soubory EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## Co je soubor EGG?

Soubor EGG, také známý jako Python vejce, je starší distribuce formátu Python. Jedná se o [ZIP](/cs/compression/zip/) komprimovaný archiv s příponou .egg a obsahuje zdrojové soubory aplikace Python spolu s metainformacemi o distribuci. Soubory EGG jsou alternativou k souboru Windows Executable [EXE](/cs/executable/exe/), ale jsou multiplatformní. Tento starší formát pro distribuce Pythonu byl začátkem roku 2010 nahrazen novějším formátem souborů Wheel (WHL).

## Formát souboru EGG

Soubory EGG se ukládají jako komprimované archivy ZIP. To znamená, že pokud nahradíte příponu .egg příponou .zip, budete ji moci otevřít pomocí standardních dekompresních utilit, jako je Corel WinZIP, Microsoft Explorer nebo RARLAB WinRAR.

Soubory EGG lze vytvořit pomocí balíčku **distutils** dostupného v Pythonu. Dalším nástrojem, který dokáže vytvářet a otevírat soubory EGG, je **SetupTools**. Soubory EGG lze nainstalovat jako balíček pomocí **easy_install**.

`POZNÁMKA - Formát souboru EGG byl zastaralý ve prospěch nového formátu souboru WHL kola.`

## reference ##

* [Python EGG](https://python101.pythonlibrary.org/chapter38_eggs.html)

