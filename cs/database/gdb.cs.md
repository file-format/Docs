{
  "date" : "2022-05-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru GDB - soubor geodatabáze souborů ESRI",
  "description":"Další informace o formátu souborů GDB a rozhraních API, která mohou vytvářet a otevírat soubory GDB.",
  "linktitle" : "GDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2022-05-08"
}

## Co je soubor GDB?

Soubor ESRI Geodatabase (FileGDB) je kolekce souborů ve složce na disku, která obsahuje související geoprostorová data, jako jsou datové sady prvků, třídy prvků a související tabulky. Aby fungoval, vyžaduje, aby byly vedle souboru .gdb ve stejném adresáři uchovávány určité další soubory. Na soubor .gdb lze provádět dotazy pro správu prostorových i neprostorových dat.

## Formát souboru GDB – Další informace

Souborové geodatabáze se skládají ze sedmi systémových tabulek plus uživatelských dat. Uživatelská data mohou být uložena v následujících typech datových sad:

* Třída funkcí
* Soubor dat funkcí
* Mozaikový datový soubor
* Katalog rastrů
* Rastrová datová sada
* Schematický soubor dat
* Tabulka (neprostorová)
* Sady nástrojů

Datové sady funkcí mohou obsahovat třídy funkcí a také následující typy datových sad:

* Přílohy
* Anotace související s funkcemi
* Geometrické sítě
* Síťové datové sady
* Balíkové tkaniny
* Vztahové třídy
* Terény
* Topologie

Výchozí maximální velikost datových sad v souborových geodatabázích je 1 TB. Maximální velikost může být zvýšena na 256 TB pro velké datové sady (obvykle rastrové). To je řízeno konfiguračním klíčovým slovem. Další informace naleznete v části Klíčová slova konfigurace pro souborové geodatabáze.

Souborové geodatabáze mohou také obsahovat podtypy a domény a podílet se na replikaci checkout/check-in a jednosměrných replikách.

Ke souborové geodatabázi může současně přistupovat několik uživatelů. Pokud uživatelé upravují, musí upravovat různé datové sady.

## Specifikace formátu souboru GDB ##

Soubor GDB je proprietární formát ESRI a jeho specifikace nejsou veřejně dostupné. Z tohoto důvodu nemohly být podrobnosti o formátu souboru pro FIle GDB zdokumentovány nikde jinde než v některých zdrojích, které to [částečně] provedly (https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec) pomocí reverzního inženýrství .

## Reference ##

* [Specifikace FGDB](https://github.com/rouault/dump_gdbtable/wiki/FGDB-Spec)

