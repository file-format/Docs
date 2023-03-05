{
  "date" : "2020-08-20",
  "keywords" :[ "soubor fnt", "formát souboru fnt", "co je soubor fnt", "soubor", "příklad fnt", "přípona souboru fnt", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FNT - Windows Font File",
  "description":"Další informace o formátu souborů FNT a rozhraních API, která mohou vytvářet a otevírat soubory FNT.",
  "linktitle" : "FNT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Co je soubor FNT?

Soubor s příponou .fnt je soubor písem, který ukládá obecné informace o písmech v operačních systémech Windows. Soubory FNT byly většinou nahrazeny formáty souborů TrueType (.TTF) a OpenType (.OTF) a od nynějška jde o zastaralý formát souboru písem. Tyto soubory mohou uložit jeden hodnotitel nebo vektorové písmo. Všechny ovladače zařízení podporují písma Windows 2.x. Ne všechny ovladače zařízení
podporují verzi Windows 3.0.

## Formát souboru FNT

Soubory FNT jsou schopny uložit jedno rastrové nebo vektorové písmo. Vektorové formáty jsou v GDI častěji používány ve srovnání s rastrem, kde je glyf každé charty definován pomocí malé bitmapy. Zřejmým důvodem pro nahrazení .fnt za .ttf a .otf je jeho rastrový formát.

### Záhlaví souboru písem
Začátek souborů rastrových i vektorových písem je společný, následovaný různými informacemi pro každý typ souboru. Záhlaví souboru písem obsahuje pro systém Windows 3.0 šest nových polí, jak je uvedeno dále, která jsou nastavena na nulu, aby byla zajištěna kompatibilita s budoucími verzemi systému Windows.

* dFlags
* dfAspace
* dfBspace
* dfCspace
* dfColorPointer
* dfReserved1

Podrobné informace o hlavičkách pro Windows 3.0 a 2.0 naleznete v [archivu Microsoft KnowledgeBase](https://jeffpar.github.io/kbarchive/kb/065/Q65123/).

## Reference
* [Formát souboru písma](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)
* [Jak nainstalovat nebo odebrat písmo ve Windows](https://support.microsoft.com/en-us/windows/how-to-install-or-remove-a-font-in-windows-f12d0657-2fc8 -7613-c76f-88d043b334b8)

