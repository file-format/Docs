{
  "date": "2023-05-09",
  "keywords": [
"pc3 fails",
"kas ir pc3 fails",
"kā izveidot pc3 failu programmā AutoCAD",
"kāds ir pc3 faila formāts",
"ko satur pc3 fails",
"failu",
"pc3 faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "PC3 faila formāts — AutoCAD plotera konfigurācijas fails",
  "description": "Uzziniet par PC3 formātu un API, kas var izveidot un atvērt PC3 failus.",
  "linktitle": "PC3",
  "menu": {
    "docs": {
      "identifier": "cad-pc3-lv",
      "parent": "cad"
}
},
  "lastmod": "2023-05-09"
}

## Kas ir PC3 fails?

PC3 fails programmā AutoCAD ir plotera konfigurācijas fails, kurā ir iekļauti printera vai plotera iestatījumi izmantošanai programmatūrā.

Kad veidojat jaunu plotera konfigurāciju, AutoCAD saglabā visu nepieciešamo informāciju par printeri vai ploteri PC3 failā. Tas ietver tādas lietas kā papīra izmēri, piemales, izšķirtspēja un citi iestatījumi, kas raksturīgi jūsu izmantotajam printerim vai ploterim.

Varat izmantot PC3 failu, lai programmā AutoCAD viegli iestatītu un konfigurētu printeri vai ploteri. Lai izmantotu PC3 failu, dialoglodziņā Plot atlasiet to pieejamo plotera konfigurāciju sarakstā.

Varat arī izveidot pielāgotus PC3 failus, mainot esošā PC3 faila iestatījumus vai izveidojot jaunu PC3 failu no jauna, izmantojot AutoCAD Plotter Manager.

## Kā izveidot PC3 failu programmā AutoCAD?

Lai programmā AutoCAD izveidotu plotera konfigurācijas failu (PC3), rīkojieties šādi:

1. **Atvērt Plotter Manager:** komandrindā ierakstiet PLOTTERMANAGER vai lentē atveriet cilni Izvade un panelī Plot atlasiet Ploter Manager.
2. **Noklikšķiniet uz Add-A-Plotter Wizard:** tiks palaists vednis, kas palīdzēs jums izveidot jaunu plotera konfigurācijas failu.
3. **Atlasiet plotera ražotāju un modeli:** vednis liks jums sarakstā atlasīt printera vai plotera ražotāju un modeli. Ja jūsu printeris vai ploteris nav sarakstā, varat atlasīt Mans dators un pārlūkot draivera failu.
4. **Izvēlieties portu:** atlasiet portu, kuram ir pievienots printeris vai ploteris. Ja neesat pārliecināts, pārbaudiet printera vai plotera komplektācijā iekļauto dokumentāciju.
5. **Norādiet plotera konfigurāciju:** vednis liks jums norādīt dažādus plotera iestatījumus, piemēram, papīra izmēru, izšķirtspēju un krāsu dziļumu. Noteikti iestatiet šīs opcijas atbilstoši savam printerim vai ploterim.
6. **Saglabāt plotera konfigurāciju:** Kad esat norādījis visus iestatījumus, vednis liks jums piešķirt jaunajai plotera konfigurācijai nosaukumu. Tādējādi vedņa norādītajā mapē tiks izveidots jauns PC3 fails.
7. **Izmantojiet jauno plotera konfigurāciju:** Lai izmantotu jauno plotera konfigurāciju programmā AutoCAD, atveriet dialoglodziņu Plot, atlasiet jauno plotera konfigurāciju pieejamo plotera konfigurāciju sarakstā un pēc tam iestatiet diagrammu kā parasti.

Tieši tā! Tagad programmā AutoCAD esat izveidojis jaunu plotera konfigurācijas failu (PC3), ko varat izmantot zīmējumu drukāšanai vai zīmēšanai.

## Kāds ir PC3 faila formāts?

PC3 faila formāts ir patentēts faila formāts, ko izmanto Autodesk AutoCAD programmatūra. Tajā ir konfigurācijas iestatījumi konkrētam ploterim vai printerim, tostarp papīra izmērs, krāsu dziļums, izšķirtspēja un citas opcijas.

PC3 fails parasti tiek glabāts AutoCAD instalācijas direktorija mapē Plotter Configuration, un to var viegli koplietot starp lietotājiem vai datoriem, lai nodrošinātu konsekventus drukāšanas un zīmēšanas iestatījumus.

PC3 fails būtībā ir teksta fails, kas satur XML datus, kas ir mašīnlasāms formāts datu glabāšanai un apmaiņai. Varat skatīt un rediģēt PC3 faila saturu, izmantojot teksta redaktoru vai XML redaktoru, taču ir ieteicams izmantot AutoCAD Plotter Manager, lai veiktu izmaiņas plotera konfigurācijā, jo tas nodrošinās, ka iestatījumi ir pareizi formatēti un saderīgi ar programmatūru.

## Ko satur PC3 fails?

PC3 fails programmā AutoCAD satur printera vai plotera konfigurācijas iestatījumus, kas ir raksturīgi konkrētai ierīcei vai draiverim. AutoCAD izmanto šos iestatījumus, lai precīzi izdrukātu vai uzzīmētu zīmējumus un nodrošinātu, ka tie izskatās tā, kā esat iecerējis.

Šeit ir daži iestatījumi, ko var saglabāt PC3 failā:

- **Papīra izmērs:** norāda papīra izmēru, kas tiks izmantots drukāšanai vai zīmēšanai, piemēram, A4, Letter vai Custom.
- **Grafika apgabals:** norāda zīmējuma daļu, kas tiks uzzīmēta, piemēram, viss izkārtojums vai tikai konkrēts logs.
- **Sižeta mērogs:** norāda mērogu, kādā zīmējums tiks drukāts vai uzzīmēts, piemēram, 1:100 vai 1/4=1'-0.
- **Līnijas svars:** norāda līniju biezumu zīmējumā, kas ietekmē to, kā tās izskatīsies drukājot vai uzzīmējot.
- **Krāsu dziļums:** norāda krāsu skaitu, kas tiks izmantotas drukāšanai vai attēlošanai, piemēram, melnbaltā vai pilnkrāsu.
- **Izšķirtspēja:** norāda izšķirtspēju, ar kādu zīmējums tiks drukāts vai uzzīmēts, kas ietekmē to, cik ass un detalizēts tas izskatīsies.
- **Citas opcijas:** PC3 failā var iestatīt daudzas citas opcijas, piemēram, drukas kvalitāti, orientāciju, piemales, ēnojumu un citas.

Izveidojot un izmantojot PC3 failu, kurā ir pareizi iestatījumi jūsu konkrētajam printerim vai ploterim, jūs varat nodrošināt, ka jūsu zīmējumi tiek izdrukāti vai attēloti precīzi un konsekventā kvalitātē.

## Atsauces
* [PC3 programmā AutoCAD](https://www.autodesk.com/support/technical/article/caas/sfdcarticles/sfdcarticles/Creating-plotter-configuration-files-PC3.html)


