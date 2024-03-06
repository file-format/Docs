{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par CSD Steam Game Data Backup File formātu un API.",
  "title" : "CSD faila formāts — Steam spēles datu dublējuma fails",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd-lv",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Kas ir CSD fails?

CSD fails ir spēļu dublējuma fails, ko ģenerē spēļu pakalpojums **Steam**, kas ļauj lietotājiem lejupielādēt un pārvaldīt **Valve** spēles. Tajā ir ar spēlēm saistītie dublējuma dati, kurus var izmantot izdzēstas spēles atjaunošanai. Steam var atjaunot spēli no CSD faila tikai tad, ja spēle ir pabeigta, lejupielādēta, instalēta un labota, izmantojot Steam. Lai atjaunotu spēli no CSD faila, izmantojiet opciju Steam → Backup and Restore Gamesteam un atlasiet failu.

## CSD faila formāts — vairāk informācijas

CSD faila formāta iekšējā struktūra nav publiski pieejama, un tā faila formāta specifikācijas nav pieejamas izstrādātāju uzziņai. CSD failiem ir pievienoti CSM un ISS faili, kas arī ir Steam spēļu failu formāti.

### Kur atrast Steam dublējuma failus?

Visus Steam dublējuma failus var atrast šādās vietās:

 * C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
 * \cfg\ — pielāgotas konfigurācijas un konfigurācijas skripti
 * \downloads\ — pielāgots saturs vairāku spēlētāju spēlēm
 * \maps\ — pielāgotas kartes, kas ir instalētas vai lejupielādētas vairāku spēlētāju spēļu laikā
 * \materiāli\ — pielāgotas tekstūras un apvalki
 * \SAGLABĀT\ — viena spēlētāja saglabātās spēles

Tomēr trešo pušu radīto spēļu atrašanās vieta var būt atšķirīga, un to nosaka spēles izstrādātājs.

### Atjaunošana no CSD dublējuma faila

Instalējiet Steam un piesakieties pareizajā Steam kontā (sīkākus norādījumus skatiet sadaļā Steam instalēšana)
 * Palaidiet Steam
 * Steam lietojumprogrammas augšējā kreisajā stūrī noklikšķiniet uz Steam.
 * Atlasiet Spēļu dublēšana un atjaunošana...
 * Izvēlieties Atjaunot iepriekšējo dublējumu
 * Pārlūkojiet līdz spēles dublējuma failu atrašanās vietai
 * Turpiniet cauri Steam logiem, lai instalētu nepieciešamās spēles.

## Atsauces

 * [Izmantojot Steam dublēšanas funkciju](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

