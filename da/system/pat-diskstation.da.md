{
   "date":"2023-11-01",
   "keywords":[
"klappe",
"pat fil",
"pat diskstation manager installationsfil",
"hvordan man åbner en pat-fil",
"fil",
"pat filtypenavn",
"udvidelse",
"fil"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAT-filformat - DiskStation Manager-installationsfil",
   "description":"Lær om PAT DiskStation Manager installationsfilformat og API'er, der kan oprette og åbne PAT-filer.",
   "linktitle":"PAT",
   "menu":{
      "docs":{
         "identifier":"system-pat-diskstation-da",
         "parent":"system"
}
},
   "lastmod":"2023-11-01"
}

## Hvad er en PAT fil?

En PAT-fil er almindeligvis forbundet med **DiskStation Manager (DSM)**, operativsystem, der bruges af Synology Network-Attached Storage (NAS)-enheder. PAT-filen er en installationsfil, der bruges til at opdatere eller installere DSM på en Synology NAS.

## Brug af PAT-fil

Here is how you typically use a PAT file to install or update DSM on Synology NAS:

1.  Download PAT-fil: Du kan hente PAT-fil fra det officielle Synology-websted eller andre pålidelige kilder.
    
2.  Log ind på din NAS: Få adgang til den webbaserede brugergrænseflade på din Synology NAS ved at indtaste dens IP-adresse i en webbrowser. Du skal bruge administratorrettigheder for at udføre denne handling.
    
3.  Gå til Pakkecenter: Naviger til Pakkecenter i webgrænsefladen. Det er her, du administrerer og installerer applikationer på din NAS.
    
4.  Manual Installation: In Package Center, there should be an option for "Manual Installation" or "Install/Update" depending on version of DSM you are using. Choose this option.
    
5.  Søg efter PAT-fil: Du bliver bedt om at gennemse dine lokale filer og vælge den downloadede PAT-fil.
    
6.  Install or Update: After selecting PAT file, follow on-screen instructions to either install DSM (if it is a fresh installation) or update DSM (if you are upgrading to newer version).
    
7.  Wait for Completion: The installation or update process can take some time and your NAS may reboot as part of process. Be patient and wait for it to finish.
    
8.  Post-Installation Configuration: After installation or update, you may need to configure your NAS settings as per your preferences.

## DiskStation Manager

DiskStation Manager, ofte forkortet som DSM, er et operativsystem udviklet af Synology til deres Network-Attached Storage (NAS)-enheder. Den fungerer som administrations- og kontrolgrænseflade til Synology NAS-servere. DiskStation Manager giver brugervenlig webbaseret grænseflade, der giver brugerne mulighed for at konfigurere og administrere forskellige aspekter af deres NAS såsom datalagring, fildeling, backupløsninger, multimedietjenester og mere.

DSM er kendt for sin alsidighed og omfattende pakke-økosystem, som gør det muligt for brugere at installere og køre forskellige applikationer og tjenester på deres Synology NAS, hvilket gør den til en multifunktionsserver til både hjemme- og virksomhedsbrug. Nogle af de almindelige funktioner i DiskStation Manager omfatter fildeling, sikkerhedskopiering og synkronisering af data, mediestreaming, sikkerhedsfunktioner og virtualiseringsunderstøttelse.

Synology udgiver jævnligt opdateringer og nye versioner af DSM for at forbedre sikkerhed, ydeevne og funktioner. Brugere kan manuelt opdatere DSM ved hjælp af PAT-filer eller konfigurere automatiske opdateringer for at sikre, at deres NAS kører den nyeste og mest sikre version af DiskStation Manager.

## Hvordan man åbner en PAT fil

To manually update DiskStation Manager, you can use a PAT file that you have downloaded from Synology Download Center using the following steps:

1. Få adgang til DiskStation Manager Kontrolpanel.
2. Naviger til afsnittet Opdater og gendan, og vælg DSM-opdatering.
3. Derfra skal du vælge Manuel DSM-opdatering.
4. Klik på knappen Gennemse, og find og vælg den PAT-fil, du har downloadet.
5. For at starte opdateringen af DiskStation Manager skal du klikke på knappen Anvend.

## Referencer
* [Synology](https://en.wikipedia.org/wiki/Synology)
