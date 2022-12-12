{
  "date" : "2022-02-16",
  "keywords" :[ "soubor obb", "formát souboru obb", "co je soubor obb", "soubor", "příklad obb", "přípona souboru obb", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru OBB - Android neprůhledný binární soubor blob",
  "description":"Další informace o formátu souboru OBB a rozhraních API, která mohou vytvářet a otevírat soubory OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## Co je soubor OBB?

Soubor OBB je soubor rozšíření, který obsahuje další data, která jsou navíc k souboru Android [APK](/cs/compression/apk/). Obchod Google Play neumožňuje mít soubor Android APK o velikosti větší než 100 MB. Některé aplikace však mohou kromě souborů APK vyžadovat hostování grafiky, mediálních souborů nebo jiných velkých aktiv ve vysokém rozlišení. Zde přicházejí na řadu typy souborů OBB. Google Play umožňuje připojit tyto rozšiřující soubory jako doplněk k souboru APK.

## Formát souboru OBB

Soubory OBB se ukládají jako binární soubory spolu se soubory APK. Když je k souborům OBB připojen soubor APK, Google Play hostuje soubory rozšíření na svém serveru a vývojáři nejsou účtovány žádné další náklady. Tyto dodatečné soubory jsou uloženy ve sdíleném úložišti zařízení na SD kartě nebo v oddílu připojitelném přes USB, když je aplikace stažena pro instalaci.

Soubory OBB se stáhnou a nainstalují po stažení. Ale v některých případech jsou tyto staženy pro instalaci při prvním spuštění aplikace.

### Maximální velikost souboru OBB

Obchod Google Play umožňuje nahrávat soubory rozšíření OBB o velikosti až 2 GB. Velké soubory se doporučuje nahrávat jako komprimované soubory [ZIP](/cs/compression/zip/) pro efektivní nahrávání přes internet.

Tyto rozšiřující soubory mohou být hostovány buď jako **hlavní** primární rozšiřující soubor pro další zdroje požadované aplikací, nebo jako volitelný opravný rozšiřující soubor určený pro malé aktualizace hlavního rozšiřujícího souboru.

## Reference

* [Android Developers – Expansion Files](https://developer.android.com/google/play/expansion-files)

