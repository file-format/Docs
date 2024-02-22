{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "EAZ File - Co je soubor EAZ a jak jej otevřít?",
  "description":"Přečtěte si o formátu souborů EAZ a rozhraních API, která mohou vytvářet a otevírat soubory EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-csz"
}
},
  "lastmod" : "2023-12-23"
}

## Co je soubor EAZ?

Soubor EAZ je doplňkový soubor používaný aplikací ArcGIS Explorer, bezplatnou aplikací vyvinutou společností ESRI pro průzkum, vizualizaci a sdílení map. Obsahuje komprimovaný archiv souborů, který obsahuje [XML file](/web/xml/), zkompilovaný kód a podpůrné soubory potřebné pro doplněk. Tyto soubory se používají k rozšíření základní funkčnosti softwaru začleněním nových tlačítek, ukotvitelných oken a dalších rozšíření.

## Formát souboru EAZ – Další informace

Soubory EAZ jsou vytvářeny pomocí sady ArcGIS Explorer SDK, vývojové sady navržené pro vytváření vlastních funkcí v rámci ArcGIS Explorer. Tyto soubory využívají kompresi [ZIP](/compression/zip/) k efektivnímu zabalení jejich obsahu. V jádru archivu je soubor **Addins.xml** umístěn v kořenovém adresáři a slouží jako životně důležitá součást, která nastiňuje a podrobně popisuje různá přizpůsobení vložená do souboru EAZ.

Soubor Addins.xml v podstatě funguje jako cestovní mapa, která nabízí pohled na konkrétní vylepšení, úpravy a rozšíření, které soubor EAZ zavádí do ArcGIS Explorer. Prostřednictvím této komplexní struktury mohou vývojáři zapouzdřit a hladce integrovat nové funkce, tlačítka a dokovatelná okna, čímž vylepší celkovou funkčnost a uživatelskou zkušenost aplikace ArcGIS Explorer.

## Reference

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
