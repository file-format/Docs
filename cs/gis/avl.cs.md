{
  "date" : "2022-11-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AVL - ArcView Legend File",
  "description":"Přečtěte si o formátu souboru AVL a rozhraních API, která mohou vytvářet a otevírat soubory AVL.",
  "linktitle" : "AVL",
  "menu" : {
    "docs" : {
      "identifier":"gis-avl-cs",
      "parent" : "gis"
}
},
  "lastmod" : "2022-11-30"
}

## Co je soubor AVL?

Soubor AVL je soubor legendy, který obsahuje klíč pro mapu vygenerovanou pomocí softwaru ESRI ArcView GIS (Geographic Information System). Obsahuje informace o referenční symbolice použité v odpovídající mapě pro přístup. Soubor AVL může obsahovat více informací, jako je symbolika, nastavení zobrazení, jako je průhlednost, vlastnosti zobrazení závislé na měřítku, informace spojené tabulky/související tabulky, definiční dotaz, vlastnosti označení pro vrstvy prvků a vlastnosti zobrazení poznámek pro vrstvy poznámek v závislosti na typu. druh vrstvy.

Na soubor AVL lze odkazovat ze souboru projektu ArcView [.APR](/gis/apr/).

## Formát souboru AVL – Další informace

Soubory AVL se ukládají ve formátu prostého textu. To znamená, že můžete otevřít soubory AVL v libovolném textovém editoru, jako je Notepad, Notepad++ a Apple TextEdit. Po otevření můžete obsah souboru nejen prohlížet, ale také jej upravovat.

### Rozdíl mezi soubory .LYR a .AVL

 * **Rozdíl ve formátu souboru** – .lyr je binární soubor, zatímco .avl je textový soubor
 * **Rozdíl v obsahu** – Soubor .lyr obsahuje více informací než soubor .avl. Soubor AVL ukládá pouze informace o symbolice, zatímco soubor LYR ukládá všechny informace, které jsou dostupné v dialogovém okně vlastností vrstvy v ArcMap.

## Reference

* [Rozdíl mezi soubory .lyr a .avl](https://support.esri.com/en/technical-article/000005936)


