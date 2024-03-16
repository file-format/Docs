{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "soubor", "rozšíření", "formát souboru", "Rozvržení stránky", "Encapsulated PostScript" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů EPS a rozhraních API, která mohou vytvářet a otevírat soubory EPS.",
  "title" :"Formát souboru EPS - soubor Encapsulated PostScript",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor EPS?

Soubor .eps je soubor obrázku, který je uložen na disk ve formátu souboru Encapsulated Postscript. Může obsahovat libovolnou kombinaci textu, grafiky a obrázků. Soubory EPS mohou také obsahovat bitmapový náhledový obrázek zapouzdřený uvnitř pro zobrazení aplikacemi, které mohou takové soubory otevřít.

## Stručná historie formátu souborů EPS

Rychlý pohled na formát souboru EPS z pohledu historie odhalí následující informace:

* První verzi EPS vydala Adobe někdy v letech 1985 až 1988
* Verze 2.0 specifikace EPS byla zveřejněna v lednu 1989
* Specifikace pro verzi 3.0 EPS byla vydána jako samostatný dokument v roce 1992; toto je poslední zveřejněná verze.

EPS v kombinaci s rozšiřujícím mechanismem Open Structuring Conventions popsaným v článku 9 specifikace Adobe PostScript Language Document Structuring Conventions Specification vytvořil základ raných verzí formátu souboru Adobe Illustrator Artwork.

## Formát souboru EPS

EPS je proprietární, ale veřejně dokumentovaný formát a specifikace formátu souborů EPS jsou veřejně dostupné pro vývojáře. EPS je formát souboru odpovídající [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Document Structuring Convention) a dodržuje všechna pravidla stanovená DSC. DSC je speciální formát souboru pro PostScriptové dokumenty od Adobe. Každá aplikace, která tvrdí, že je schopna číst soubory EPS, by měla být kompatibilní s DSC.

Soubor EPS se skládá ze dvou hlavních částí, jak je vysvětleno níže.

### Náhled obrázku ###

Typický soubor EPS obsahuje náhledový obrázek ve formátu určeném pro pohodlné použití v pracovním postupu, který zahrnuje několik systémů nebo aplikací. Záměrem náhledu je mít obrázek ve formátu, který většina grafických aplikací dokáže vykreslit; náhled má obvykle nižší rozlišení, rozměry v pixelech a/nebo bitovou hloubku. Soubor náhledu může být v jednom z mnoha formátů. Specifikace pro EPS_3 uvádí tři formáty náhledu „specifické pro zařízení“:

* pro Apple Macintosh, obrázek PICT používaný aplikací QuickDraw
* pro počítače DOS bitmapa TIFF
* Windows Metafile.

PICT a Windows Metafile mohou obsahovat bitmapová data i vektorovou grafiku. Specifikace navíc definuje velmi jednoduchou reprezentaci pro vložený bitmapový náhledový obrázek nezávislou na zařízení. Tato reprezentace je známá jako Encapsulated PostScript Interchange Format (EPSI).

Náhled EPSI je bitmapa reprezentovaná jako hexadecimální ASCII, zabalená mezi několik PostScriptových komentářů pro identifikaci a určená k tomu, aby byla jednoduchá a snadno přenosná. Aby bylo možné rozlišit soubory EPS s různými formáty náhledu, byly ve specifikaci EPS doporučeny různé přípony souborů DOS a typy souborů Macintosh.

### PostScriptový kód

Formát souboru EPS musí obsahovat minimálně následující:

* komentář v záhlaví, %!PS-Adobe-3.0 EPSF-3.0
* a komentář ohraničujícího rámečku %%BoundingBox: llx lly urx ury, který popisuje hranice ilustrace. Tyto čtyři argumenty odpovídají levému dolnímu (llx, lly) a pravému hornímu rohu (urx, ury) ohraničovacího rámečku.

Soubor EPS nemůže používat žádný z následujících operátorů:

*pásmové zařízení,
* cleardictstack
* kopírovací stránka
* smazat stránku
* výstupní server
* rámové zařízení
* grestoreall
* initclip
* initgraphics
* initmatice
* ukončit
* vykreslovací pásma
* nastavit globální
* nastavení zařízení
* nastaví sdílené
* nástupní zaměstnání.

## Převod EPS do jiných formátů souborů

Soubory EPS lze převést do standardních obrazových formátů, jako jsou [JPG](/cs/image/jpeg/), [PNG](/cs/image/png/), [TIFF](/cs/image/tiff/) a [PDF](/cs/pdf/) pomocí různých aplikací, např. Adobe Illustrator, Photoshop a PaintShop Pro.

Kvůli [chybě zabezpečení](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) v souborech EPS, Office 2016, Office 2013, Office 2010 a Office 365 vypnuly možnost vkládat soubory EPS do dokumentů Office.

## Reference

* [Encapsulated PostScript – Wikipedia](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

