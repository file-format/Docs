{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADMX fájl – csoportházirend felügyeleti sablon fájlformátuma",
  "description":"További információ az ADMX fájlformátumról és az ADMX fájlok megnyitásáról.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Mi az ADMX fájl?

Az ADMX-fájl a Microsoft Windows csoportházirend-szoftver által használt házirend-konfigurációs fájl, amely a csoport számítógépeinek csoportját kezeli. Ez egy XML-alapú adminisztrációs sablonfájl, amelyet a Windows Vista Service Pack 1 szervizcsomaggal vezettek be. Az ADMX-fájlok felhasználói fiókok, operációs rendszer-konfigurációk és alkalmazások konfigurációs beállításait tartalmazzák. Az ADMX-fájlok a konfigurációk tárolására és üzembe helyezésére szolgálnak számos számítógépes rendszer központi kezeléséhez.

ADMX-fájlokat bármilyen XML-kompatibilis, bármilyen szövegszerkesztővel vagy Microsoft csoportházirend-objektumszerkesztővel létrehozhat vagy szerkeszthet.

## ADMX fájlformátum - További információ

Az ADMX fájlok univerzális [XML](/hu/web/xml/) fájlformátumban vannak tárolva, amely ember által olvasható. Ez többnyelvű fájlformátum, és lehetővé teszi a különböző nyelvű rendszergazdák számára, hogy ugyanazokkal az ADMX fájlokkal dolgozzanak. Az ADMX fájlok felváltották a régi [ADM](/hu/system/adm/) fájlformátumot, amely egy unicode formátumú szöveges fájlformátum. Az ADMX-fájlok meghatározzák azokat a beállításkulcsokat, amelyek egy bizonyos csoportházirend-beállítás módosításakor módosulnak.

### Mit tehetek az ADMX fájllal?

Az ADMX-fájlok határozzák meg, hogy milyen műveletek engedélyezettek a csoport részét képező felhasználói számítógépeken. A csoportházirend az Active Directory szoftverrel kombinálva határozza meg a szabályokat. Az ADMX-fájlok kezelése a Windows operációs rendszer központi tárolójából történik, amely a tartomány központi helye.

A munkakörnyezetben telepített ADMX-fájl lehetővé teszi a rendszergazdák számára, hogy olyan házirendeket hajtsanak végre, mint például:

* Irányítsd az internet használatát
* Bizonyos típusú fájlok letöltése
* Cserélhető eszközök használata a rendszereken

## Hivatkozások

* [Felügyeleti sablonfájlok – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – Felügyeleti sablonfájlok kezelése](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

