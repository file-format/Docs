{
  "date" : "2020-01-12",
  "keywords" :[ "DGN", "Soubor", "Formát", "Otevřít", "Číst", "API", "MicroStation", "Intergraph Interactive Graphics Design System" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DGN - MicroStation CAD Design File Format",
  "description" :"Další informace o formátu souborů DGN a rozhraních API, která mohou vytvářet a otevírat soubory DGN.",
  "linktitle" : "DGN",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2020-01-12"
}

## Co je soubor DGN?

Soubor s příponou .dgn (Design) je soubor výkresu vytvořený a podporovaný aplikacemi CAD, jako je MicroStation a Intergraph Interactive Graphics Design System. Používá se pro vytváření a ukládání návrhů pro stavební projekty, jako jsou dálnice, mosty a budovy. Formát je podobný formátu souborů [DWG](/cs/cad/dwg/) společnosti Autodesk a je považován za jeho konkurenta. Soubory DNG lze uložit buď jako Intergraph Standard File Format nebo V8 DGN. DGN lze převést do několika dalších formátů, jako je DWG, [BMP](/cs/image/bmp/), [JPEG](/cs/image/jpeg/), [PDF](/cs/pdf/), [GIF](/cs/image/ gif/) a další. Kromě jiných softwarových aplikací, jako jsou verze Corel PaintShop Photo Pro a IMSI TurboCAD Deluxe, lze jej otevřít pomocí Autodesk AutoCAD, Bentley View a Bentley Systems MicroStation.

## Formát souboru V8 DGN

Soubor MicroStation V8 DGN se skládá z jednoho nebo více modelů. Model je kontejner pro prvky. V8 DGN odstraňuje všechna omezení založená na formátu souborů, která byla přítomna v předchozích verzích MicroStation. Následuje seznam vylepšení ve formátu souboru DGN.

* Omezení počtu úrovní v souboru DGN bylo odstraněno a každá úroveň je pojmenována a uložena jako prvek.
* Maximální fyzická velikost souboru DGN nemá žádné omezení a je omezena pouze operačním systémem (např. limit NT je 4 GB)
* Maximální velikost jednoho prvku je 128 kB.
* Maximální velikost buňky není omezena.
* Názvy buněk jsou omezeny na přibližně 500 znaků.
* Počet odkazů, které lze připojit k souboru DGN, není omezen.
* Řetězec čáry, tvar nebo bodová křivka může mít až 5000 vrcholů.
* Počet součástí ve složitém řetězci nebo složitém tvaru není omezen.
* Počet grafických skupin v souboru DGN není omezen.
* Plot je rovnoběžný s pohledem, ve kterém je umístěn.
* Jeden řádek textu může obsahovat 65 535 znaků.
* Maximální velikost textového uzlu není omezena.
* Počet textových uzlů v souboru DGN není omezen.
* Každý prvek má jedinečný 64bitový identifikátor, který se během životního cyklu prvku nemění.
* Každý prvek má časové razítko, které označuje čas poslední změny.

## Reference

* [DNG – z Wikipedie](https://en.wikipedia.org/wiki/DGN)
* [Formát souboru MicroStation V8 DGN](https://web.archive.org/web/20120713013730/http://docs.bentley.com/ko/MicroStation/ustnhelp47.html)

