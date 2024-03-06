{
   "date":"2023-11-01",
   "keywords":[
"pat",
"pat fails",
"pat diskstation pārvaldnieka instalācijas fails",
"kā atvērt pat failu",
"failu",
"pat faila paplašinājums",
"pagarinājumu",
"failu"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAT faila formāts — DiskStation Manager instalācijas fails",
   "description":"Uzziniet par PAT DiskStation Manager instalācijas faila formātu un API, kas var izveidot un atvērt PAT failus.",
   "linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation-lv",
         "parent":"system"
}
},
   "lastmod":"2023-11-01"
}

## Kas ir PAT fails?

PAT fails parasti tiek saistīts ar **DiskStation Manager (DSM)** — operētājsistēmu, ko izmanto Synology tīklam pievienotās atmiņas (NAS) ierīces. PAT fails ir instalācijas fails, ko izmanto, lai atjauninātu vai instalētu DSM Synology NAS.

## PAT faila izmantošana

Here is how you typically use a PAT file to install or update DSM on Synology NAS:

1.  Lejupielādēt PAT failu: PAT failu varat iegūt no oficiālās Synology vietnes vai citiem uzticamiem avotiem.
    
2.  Piesakieties savā NAS: piekļūstiet Synology NAS tīmekļa lietotāja interfeisam, ievadot tās IP adresi tīmekļa pārlūkprogrammā. Lai veiktu šo darbību, jums būs nepieciešamas administratora tiesības.
    
3.  Dodieties uz pakotņu centru: tīmekļa saskarnē dodieties uz pakotņu centru. Šeit jūs pārvaldāt un instalējat lietojumprogrammas savā NAS.
    
4.  Manual Installation: In Package Center, there should be an option for "Manual Installation" or "Install/Update" depending on version of DSM you are using. Choose this option.
    
5.  Pārlūkojiet PAT failu: jums tiks piedāvāts pārlūkot vietējos failus un atlasīt lejupielādēto PAT failu.
    
6.  Install or Update: After selecting PAT file, follow on-screen instructions to either install DSM (if it is a fresh installation) or update DSM (if you are upgrading to newer version).
    
7.  Wait for Completion: The installation or update process can take some time and your NAS may reboot as part of process. Be patient and wait for it to finish.
    
8.  Post-Installation Configuration: After installation or update, you may need to configure your NAS settings as per your preferences.

## DiskStation Manager

DiskStation Manager, bieži saīsināts kā DSM, ir operētājsistēma, ko Synology izstrādājusi savām tīklam pievienotajām atmiņas (NAS) ierīcēm. Tas kalpo kā Synology NAS serveru pārvaldības un kontroles saskarne. DiskStation Manager nodrošina lietotājam draudzīgu tīmekļa saskarni, kas ļauj lietotājiem konfigurēt un pārvaldīt dažādus sava NAS aspektus, piemēram, datu glabāšanu, failu koplietošanu, dublēšanas risinājumus, multivides pakalpojumus un daudz ko citu.

DSM ir pazīstama ar savu daudzpusību un plašo pakotņu ekosistēmu, kas lietotājiem ļauj instalēt un palaist dažādas lietojumprogrammas un pakalpojumus savā Synology NAS, pārvēršot to par daudzfunkcionālu serveri gan mājas, gan biznesa lietošanai. Dažas no izplatītākajām DiskStation Manager funkcijām ietver failu koplietošanu, datu dublēšanu un sinhronizāciju, multivides straumēšanu, drošības līdzekļus un virtualizācijas atbalstu.

Synology regulāri izlaiž DSM atjauninājumus un jaunas versijas, lai uzlabotu drošību, veiktspēju un funkcijas. Lietotāji var manuāli atjaunināt DSM, izmantojot PAT failus, vai konfigurēt automātiskos atjauninājumus, lai nodrošinātu, ka viņu NAS darbojas jaunākā un drošākā DiskStation Manager versija.

## Kā atvērt PAT failu

To manually update DiskStation Manager, you can use a PAT file that you have downloaded from Synology Download Center using the following steps:

1. Piekļūstiet DiskStation Manager vadības panelim.
2. Dodieties uz sadaļu Atjaunināt un atjaunot un izvēlieties DSM atjaunināšana.
3. No turienes atlasiet Manuāla DSM atjaunināšana.
4. Noklikšķiniet uz pogas Pārlūkot un pēc tam atrodiet un izvēlieties lejupielādēto PAT failu.
5. Lai sāktu DiskStation Manager atjaunināšanu, noklikšķiniet uz pogas Lietot.

## Atsauces
* [Synology](https://en.wikipedia.org/wiki/Synology)
