{
  "date" : "2020-11-11",
  "keywords" :[ "DTSX", "rozšíření", "soubor", "formát souboru", "Typ souboru databáze", "Formát souboru databáze", "Soubory databáze" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru DTSX a rozhraních API, která mohou vytvářet a otevírat soubory DTSX.",
  "title" :"Formát souboru DTSX - soubor nastavení DTS serveru SQL Server",
  "linktitle" : "DTSX",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## Co je soubor DTSX?

Soubor s příponou .dtsx (Data Transformation Services Package XML) je soubor Data Transformation Services (DTS), který používá Microsoft SQL k odkazování na kroky/pravidla migrace dat pro přenos dat z jedné databáze do druhé. To zahrnuje transformace a jakékoli volitelné kroky zpracování, které mohou být vyžadovány během přenosu dat mezi výchozím a cílovým bodem. SQL Server Integration Services (SSIS), součást Microsoft SQL Server, používá soubory DTSX k identifikaci kroků pro zpracování dat mezi databázovými servery. Soubory DTSX lze otevřít pomocí Microsoft SQL Server 2019.

## Formát souboru DTSX

Přesun dat mezi databázovými servery vyžaduje pravidla a kroky zpracování, které zajistí integritu dat během této operace. SSIS zajišťuje, že všechny tyto činnosti pro přesun a přizpůsobení dat z různých zdrojů v podniku probíhají pohodlně. To je místo, kde přichází DTSX, který definuje struktury, které má SSIS použít k vytvoření kroků, ve kterých mohou být data zpracována, jak následuje prostřednictvím těchto kroků.

Datový tok popsaný DTSX je znázorněn na následujícím obrázku.

{{< figure src="../DataFlowDTSX.png" alt="Datový tok DTSX" >}}

DTSX je založeno na [XML](/cs/web/xml/) a je zdokumentováno v [MS-DTSX](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13- 4b5b-a388-aa3c65aec1dd). Vylepšený refaktoring DTSX XML je DTSX 2.0, který zahrnuje nové atributy struktur, nahrazení pojmenovaných vlastností jako rodičovských atributů XML, specifikuje výchozí hodnoty pro většinu hodnot atributů a umístění opakovaných prvků uvnitř nadřazeného prvku. Struktury DTSX jsou popsány pomocí těchto [XML schémat] (https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/e5095968-26ea-4824-a717-153ccee642dc#Appendix_A_1) a strukturální formát je Celar-text XML.

## Reference

* [Formát DTSX – Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx/235600e9-0c13-4b5b-a388-aa3c65aec1dd)
* [Formát DTSX 2 – od společnosti Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-dtsx2/fb216aa4-62ab-41c8-a6d5-5b1002739d21)

