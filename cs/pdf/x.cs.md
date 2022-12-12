{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PDF/X",
  "description":"Další informace o formátu souborů PDF/X a rozhraních API, která mohou vytvářet a otevírat soubory PDF/X.",
  "linktitle" : "PDF/X",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Co je soubor PDF/X? #

PDF/X je standard ISO 15930 vydaný v roce 2001 s podmnožinou funkcí PDF. Standard byl vytvořen a publikován na základě specifických požadavků polygrafického a vydavatelského průmyslu. Všechny požadavky na tento standard byly navrženy podle různorodých potřeb tiskařského a vydavatelského průmyslu. PDF/X vyžaduje, aby vyhovující soubory byly úplné, tj. samostatné. To vyžaduje, aby prvky jako fonty použité na stránce byly součástí dokumentu. Obsah jako 3D nebo video nemůže být součástí dokumentu PDF/X. Informace obsažené v dokumentu PDF/X vyžadují, aby byly přesné.

## PDF/X standardy a revize ##

Rodina standardů PDF/X se skládá z několika verzí, z nichž každá je navržena pro specializovaný výsledek. Vývoj těchto norem byl zaměřen na řešení mnoha různorodých potřeb tiskařského a vydavatelského průmyslu.

* `PDF/X-1a` - Také známý jako první standard rodiny PDF/X, PDF/X-1a vyžaduje, aby veškerý obsah byl součástí dokumentu PDF, aby jej bylo možné vytisknout. Prvky dokumentu, jako jsou písma, formuláře, ochrana heslem a viditelné anotace, nejsou povoleny. PDF/X-1a má své vlastní specifické požadavky, stejně jako ty, které se týkají průhlednosti a jsou povoleny vrstvy. Ty také vyžadují, aby tiskové prvky používaly pouze CMYK, odstíny šedi nebo přímé barvy, takže se nepoužívají barevné prostory RGB nebo barevné prostory nezávislé na zařízení. je pro výměny, ve kterých mají být všechny soubory dodávány v CMYK (a/nebo přímých barvách), bez RGB nebo dat se správou barev. PDF/X-1a se také označuje jako úplná výměna kvůli úplnosti informací požadovaných
* `PDF/X-3` - byl představen v roce 2002 a zrušil mnohá omezení PDF/X-1a. To umožnilo grafice v PDF/X-3 používat barevné prostory CMYK, grescale, RGB, Lab a ICC. Ve skutečnosti je založen na standardech PDF 1.3 s [ICC profilem](https://en.wikipedia.org/wiki/ICC_Profile). Označuje se také jako správa barev kvůli flexibilitě a pravidlům, které zavádí ve vztahu k barvám obsaženým v dokumentu PDF.
* `PDF/X-4` - podporuje fólie, takže PDF-X/4 obsahuje všechna data potřebná pro výstup bez sloučení.
* `PDF/X-5` - je založen na PDF/X-4 a přidává podporu pro externí grafiku prostřednictvím referenčních objektů XObjects a také externí profily n-colorant pro záměr vykreslení. Použijte jej pro částečnou výměnu tiskových dat pomocí PDF verze 1.6

## Reference ##

* [PDF/X – z Wikipedie](https://en.wikipedia.org/wiki/PDF/X)

