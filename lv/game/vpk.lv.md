{
  "date" : "2023-01-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Uzziniet par Unreal Static Meshes VPK faila formātu un API, kas var izveidot un atvērt VPK failus.",
  "title" : "VPK fails — nereāls statisko tīklu fails",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "identifier":"game-vpk-lv",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-16"
}

## Kas ir VPK fails?

.vpk fails ir faila formāts, ko izmanto Valve Corporation izstrādātais spēļu dzinējs **Source Engine**. VPK faili tiek izmantoti, lai iesaiņotu spēļu saturu, piemēram, modeļus, tekstūras un skaņas, un tos parasti izmanto tādās spēlēs kā Team Fortress 2, Left 4 Dead un Counter-Strike: Global Offensive. Failus var atvērt un izvilkt, izmantojot dažādus rīkus, piemēram, GCFScape un VPK Tool.

## VPK faila formāts — vairāk informācijas

VPK faili tiek saglabāti diskā kā bināri faili. Viens vpk fails var būt daļa no VPK pakotnes vai darboties kā neatkarīgs neapstrādāts VPK fails. Informācija, ko var saglabāt VPK failā, ietver kartes, materiālus, spēļu saturu un horeogrāfijas ainas.

### Kā izveidot VPK failu?

Atkarībā no pieejamajiem rīkiem ir vairāki veidi, kā izveidot .vpk failu.

1. `Izmantojot VPK rīku:` Šis ir komandrindas rīks, ko var izmantot, lai izveidotu un izvilktu VPK failus. VPK failu var izveidot, izmantojot šādu komandu:
```
"vpk.exe -M <directory> <output_file.vpk>"
```
Tas izveidos VPK failu no norādītā direktorija un saglabās to kā norādīto izvades failu.

1. Hammer redaktora izmantošana: Hammer redaktors ir rīks, kas iekļauts avota SDK, ko var izmantot, lai izveidotu un rediģētu līmeņus spēlēm, kurās tiek izmantota avota programma. Tas ietver arī iespēju izveidot VPK failus, ar peles labo pogu noklikšķinot uz mapes cilnē Failu sistēma un atlasot Izveidot VPK.

1. `Izmantojot Valve VPK veidotāju:` Šis ir Valve izstrādāts rīks, ko izmanto spēļu satura iepakošanai un izplatīšanai. Šo rīku var izmantot, lai izveidotu VPK failus, un tas ir arī oficiālais rīks VPK failu izveidei.

## Atsauces

 * [Valve Software](https://www.valvesoftware.com/en/)
 * [VPK izstrādātāja resursi](https://developer.valvesoftware.com/wiki/GCF)

