{
  "date" : "2021-08-30",
  "keywords" :[ "soubor ipa", "formát souboru ipa", "co je soubor ipa", "soubor", "příklad ipa", "přípona souboru ipa", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souboru IPA a rozhraních API, která mohou vytvářet a otevírat soubory IPA.",
  "title" :"IPA – soubor balíčku aplikace iOS",
  "linktitle" : "IPA",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-30"
}

## Co je soubor IPA?
Soubor s příponou .ipa patří do systému iOS a je známý jako soubor balíčku aplikací. Toto je archivní soubor (komprimovaný pomocí [ZIP](/cs/compression/zip/) komprese), ve kterém je uložena aplikace pro iOS, ale tuto aplikaci lze nainstalovat pouze na zařízení se systémem iOS nebo ARM MacOS, jako je iPad, iPhone nebo ipod touch. K instalaci souborů IPA lze použít především iTunes, Apple Configurator 2 nebo jakýkoli software třetích stran.

## Formát souboru IPA
Vývojáři IOS, kteří vyvíjejí aplikace pomocí Apple Xcode, dobře znají soubory IPA, protože potřebují zabalit své vyvinuté aplikace jako soubory IPA buď pro účely testování nasazení obchodu s aplikacemi. Ačkoli je známo, že soubory IPA jsou nainstalovány jako aplikace pro iOS, můžete je také dekomprimovat a zobrazit obsažená data aplikace. Protože soubor IPA obsahuje pouze jeden binární soubor pro architekturu ARM mobilních telefonů a neobsahuje binární soubor pro architekturu x86, mnoho souborů .ipa nelze nainstalovat na iPhone Simulator.
### Struktura souboru .ipa
Následující příklad ukazuje strukturu IPA:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Výše uvedené je vestavěná struktura, kterou iTunes a App Store rozpoznávají. Podle této struktury:
- Adresář Payload obsahuje všechna data aplikace.
- Soubor iTunes Artwork je obrázek PNG o velikosti 512 × 512 pixelů, který obsahuje ikonu aplikace pro zobrazení v iTunes a aplikaci App Store na iPadu.
- iTunesMetadata.plist obsahuje různé informace, od jména a ID vývojáře, informací o autorských právech, identifikátoru balíčku, názvu aplikace, žánru, data vydání, data nákupu atd.
- Složka META-INF obsahuje pouze metadata o tom, jaký program byl použit k vytvoření IPA.


## Reference

* [.ipa – z Wikipedie](https://en.wikipedia.org/wiki/.ipa)


