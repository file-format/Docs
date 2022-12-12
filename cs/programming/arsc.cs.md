{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","co je soubor arsc","jak otevřít soubor arsc", "přípona", "soubor", "soubor arsc","formát souboru arsc", "přípona souboru arsc", "příklad souboru arc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Android Package Resource Table File",
  "description":"Další informace o formátu souboru ARSC a rozhraních API, která mohou vytvořit a otevřít soubor ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## Co je soubor ARSC?

Soubor ARSC je soubor tabulky prostředků systému Android, který obsahuje seznam prostředků aplikace ve formátu tabulky. Obsahuje informace, jako jsou názvy zdrojů, vlastnosti a ID. Soubory ARSC jsou součástí balíčků APK, které se používají k instalaci těchto aplikací pro Android. Všechny zdroje, jako jsou obrázky, rozvržení, styly a řetězce, v aplikaci pro Android jsou při vygenerování souboru APK převedeny na binární soubory. Současně je také generován soubor ARSC, který obsahuje seznam všech zkompilovaných zdrojů programu a jejich ID.

## Formát souboru ARSC

Soubory s příponou .arsc jsou binární soubory generované poté, co kompilátor, jako je ANT (Eclipse) nebo Gradle (AS), zkompiluje kód aplikace pro Android za účelem vytvoření souboru [APK](/cs/compression/apk/). Soubor APK můžete extrahovat pomocí libovolného archivačního nástroje, jako je WinZip, a zobrazit jeho obsah, což jsou kompilované soubory třídy Java, tj. class.dex. Kromě toho obsahuje také tento soubor ARSC, který obsahuje metainformace o:

* Uzly XML
* Atributy
* ID zdrojů

Prostředky v souboru APK jsou odkazovány pomocí ID prostředků, zatímco atributy jsou přeloženy na hodnotu za běhu. Nástroj Android aapt shromažďuje všechny prostředky definované v souborech v době sestavení a přiřazuje jim ID prostředků. Po přiřazení identifikátorů zkompilovaným zdrojům se ze zdrojového kódu a také ze souboru resources.arsc vygeneruje soubor R.java.

## Reference

* [Struktura tabulky binárních zdrojů](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

