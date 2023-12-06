{
  "date" : "2023-01-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Soubor OAM – formát souboru widgetu Adobe Edge Animate",
  "description" :"Zjistěte, co je soubor OAM a rozhraní API, která mohou vytvořit a otevřít soubor OAM.",
  "linktitle" : "OAM",
  "menu" : {
    "docs" : {
      "identifier":"web-oam",
      "parent" : "web"
}
},
  "lastmod" : "2023-01-30"
}

## Co je soubor OAM?

Soubor .oam a animovaný soubor widgetu exportovaný z aplikace Adobe Edge Animate Widget. Animace exportované ve formátu souboru widgetu OAM lze vložit do jiných aplikací Adobe, jako jsou dokumenty InDesign ([soubor IND](/cs/page-description-language/indd/), Dreamweaver a Muse. Soubory OAM jsou jako balíčky nasazení, které lze snadno vkládat do jiných projektů Adobe, abyste je mohli používat. Soubory OAM obsahují informace o aktivech, chování a kódu ActionScript animace. Soubor OAM můžete vytvořit publikováním projektu Adobe Animate [soubor .AN](/cs/web/an/) .
Uživatelé mohou vytvářet soubory OAM publikováním z projektu Edge Animate (soubor .AN).

## Formát souboru OAM

Soubor OAM se uloží na disk jako komprimovaný archiv [ZIP](/cs/compression/zip/). To znamená, že příponu souboru můžete přejmenovat na .zip a extrahovat pomocí libovolného komprimačního nástroje, jako je WinZIP nebo WinRAR. Zmenšená velikost souboru usnadňuje přenos a sdílení animace s ostatními uživateli přes internet.

### Struktura souboru OAM

Vnitřní struktura souboru souboru .oam je proprietární a není společností Adobe veřejně zdokumentována. Je však známo, že soubory .oam obsahují kolekci souborů a prostředků (jako je grafika, zvuk a kód jazyka ActionScript) zabalených do jednoho souboru. Obsah souboru .oam může zahrnovat soubory [XML](/cs/web/xml/), soubory SWF a další zdrojové soubory. Přesná struktura souboru .oam závisí na konkrétní verzi aplikace Adobe Animate použité k jeho vytvoření a také na typu animace a datových zdrojů obsažených v souboru.

Soubor OAM obsahuje následující informace.

`Aktiva:` Informace o grafických, zvukových a obrazových prostředcích použitých v animaci.

`Chování:` Popisy akcí a interakcí, které se vyskytují v animaci.

`ActionScript code:` Kód používaný k ovládání chování a interaktivity animace.

`Publish settings:` Informace o platformě a formátu, ve kterém bude animace publikována, jako je HTML5 nebo AIR.

`Metadata:` Další informace, jako je autor animace, datum vytvoření a číslo verze.

## Jak otevřít soubor OAM?

K otevření souborů OAM můžete použít následující aplikace.

* Adobe Edge Animate CC (ukončeno)
* Adobe Animate 2023
* Adobe InDesign 2023
* Adobe Dreamweaver 2021

## Reference

* [Publikování OAM](https://helpx.adobe.com/animate/using/OAM-publishing.html)

