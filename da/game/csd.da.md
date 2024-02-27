{
  "date" : "2022-02-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om CSD Steam Game Data Backup Filformat og API'er.",
  "title" : "CSD filformat - Steam Game Data Backup File",
  "linktitle" : "CSD",
  "menu" : {
    "docs" : {
      "identifier": "game-csd-da",
      "parent" : "game"
}
},
  "lastmod" : "2022-02-08"
}

## Hvad er en CSD fil?

En CSD-fil er en sikkerhedskopi af spil genereret af spiltjenesten **Steam**, som lader brugere downloade og administrere **Valve**-spil. Den indeholder sikkerhedskopieringsdata relateret til spil, der kan bruges til at gendanne et slettet spil. Steam er kun i stand til at gendanne spil fra en CSD-fil, hvis spillet blev fuldført downloadet, installeret og patchet gennem Steam. For at gendanne spillet fra CSD-filen, brug muligheden for Steam → Sikkerhedskopier og gendan Gamesteam og vælg filen.

## CSD-filformat - flere oplysninger

Den interne struktur af CSD-filformatet er ikke tilgængelig offentligt, og dets filformatspecifikationer er ikke tilgængelige for udviklerens reference. CSD-filer er ledsaget af CSM- og ISS-filer, som også er Steam-spilfilformater.

### Hvor finder jeg Steam-sikkerhedskopifiler?

Hele Steam-sikkerhedskopifilerne kan findes på følgende steder:

 * C:\Program Files (x86)\Steam\steamapps\common\<game name> \ :
 * \cfg\ - Brugerdefinerede konfigurationer og konfigurationsscripts
 * \downloads\ - Brugerdefineret indhold til multiplayer-spil
 * \maps\ - Brugerdefinerede kort, der er blevet installeret eller downloadet under multiplayer-spil
 * \materialer\ - Brugerdefinerede teksturer og skind
 * \SAVE\ - Gemte spil for én spiller

Placeringen af tredjepartsskabte spil kan dog være anderledes og bestemmes af spillets udvikler.

### Gendannelse fra CSD-sikkerhedskopifil

Installer Steam og log ind på den korrekte Steam-konto (se Installation af Steam for yderligere instruktioner)
 * Start Steam
 * Klik på Steam i øverste venstre hjørne af Steam-applikationen
 * Vælg Sikkerhedskopiér og gendan spil...
 * Vælg Gendan en tidligere sikkerhedskopi
 * Gå til placeringen af spillets sikkerhedskopifiler
 * Fortsæt gennem Steam-vinduerne for at installere de nødvendige spil.

## Referencer

 * [Brug af Steam Backup-funktionen](https://help.steampowered.com/en/faqs/view/4593-5CB7-DC3C-64F0)

