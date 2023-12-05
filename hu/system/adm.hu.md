{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADM fájl – Adminisztrációs sablon fájlformátum",
  "description":"További információ az ADM fájlformátumról és az ADM fájlok megnyitásáról.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## Mi az ADM fájl?

Az ADM-fájl egy sablonfájl, amelyet a Microsoft Group Policies szoftver használ a beállításjegyzék-alapú házirend-beállítások helyének meghatározására a beállításjegyzék-fájlban. A rendszergazdák a csoport részét képező számítógépek csoportjának kezelési szabályzatának meghatározására használják. Ezek az információk a csoport kezeléséhez létrehozott csoportházirend-objektumok (GPO-k) részévé válnak.

Az ADM-fájlokat a Microsoft Group Policy Object Editor segítségével nyithatja meg.

## ADM fájlformátum - További információ

Az ADM fájlok unicode formátumú szövegfájlokként tárolódnak. Ezeket elsősorban a beállításjegyzék-alapú házirend-beállítások helyének leírására használták a Windows Vista és a Windows 7 rendszerleíró adatbázisában.

Az ADM-fájlok már nem támogatottak, és az [ADMX](/hu/system/admx/) fájlokkal váltották fel őket. A GPA figyelmen kívül hagyja a következő alapértelmezett ADM-fájlokat a Microsoft Windows Vista Service Pack 1 vagy újabb verzióját futtató számítógépeken.

* system.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## Hivatkozások

* [Felügyeleti sablonfájlok – ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ – Felügyeleti sablonfájlok kezelése](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

