{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru FIT- Garmin Activity File",
  "description":"Další informace o formátu souborů FIT a rozhraních API, která mohou vytvářet a otevírat soubory FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## Co je soubor FIT?

Soubor FIT je soubor GIS vytvořený sportovními nositelnými zařízeními Garmin. Slouží k zaznamenávání činností osoby, když se s těmito zařízeními pohybuje. Údaje o aktivitě zahrnují polohu a čas zaznamenané zařízením GPS. Soubory FIT se také používají k přenosu zaznamenaných dat o aktivitě pomocí webových rozhraní API. To je důvod, proč jsou soubory FIT nejběžněji používaným formátem souborů pro sdílení fitness dat s jinými fitness platformami. Mezi další běžné formáty souborů patří [GPX](/cs/gis/gpx/), TCX a [KML](/cs/gis/kml/).

## Formát souboru FIT – Další informace

Soubory FIT se ukládají na disk jako binární soubory s informacemi zaznamenanými zařízeními Garmin pro danou aktivitu. Informace uložené uvnitř souboru FIT zahrnují:

* Čas schůzky
* Sportovní typy
* Údaje o kole a rozdělení
* GPS stopa
* Data senzoru
* Události pro aktivní relaci

Údaje o aktivitě lze zaznamenávat do souboru v reálném čase nebo exportovat po dokončení záznamu aktivity.

### Zprávy o aktivitě FIT

Soubor aktivit FIT může obsahovat některé požadované typy zpráv. Níže jsou uvedeny požadované zprávy pro soubor aktivit.

|Zpráva|Účel|
---|---|
|ID souboru| Zpráva File Id je vyžadována všemi typy souborů FIT a očekává se, že bude první zprávou v souboru. U souborů aktivit by vlastnost Type měla být nastavena na 4.|
|Aktivita| V souboru Aktivita FIT je vyžadována jedna zpráva o aktivitě. Ve zprávě Aktivita jsou zahrnuty vlastnosti Místní časové razítko a Počet relací. Místní časové razítko se používá k určení posunutí časového pásma, které lze použít na všechna časová razítka v souboru. Většina zařízení zaznamenává soubory FIT v reálném čase a počet relací bude až do konce záznamu neznámý. Z tohoto důvodu bude zpráva Aktivita často poslední zprávou v souboru.|
|Relace| Soubory aktivit budou obsahovat jednu nebo více zpráv relace. Zpráva relace je typ souhrnné zprávy. Start Time, Total Elapsed Time, Total Timer Time a Timestamp jsou povinná pole pro všechny souhrnné zprávy.|
|Kolo| Zprávy kola představují kola nebo intervaly v rámci relace. Zpráva Lap je typ zprávy Souhrn. Start Time, Total Elapsed Time, Total Timer Time a Timestamp jsou povinná pole pro všechny souhrnné zprávy.|
|Záznam| Záznamové zprávy zahrnují GPS souřadnice, rychlost, vzdálenost, srdeční frekvenci, výkon atd.|

## Užitečné zdroje souborů FIT

* [Decoding FIT Activity Files](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Kódování souborů aktivit FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Reference ##

* [Soubor aktivity FIT](https://developer.garmin.com/fit/file-types/activity/)

