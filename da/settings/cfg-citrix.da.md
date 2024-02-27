{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg fil",
"cfg citrix server forbindelsesfil",
"hvad er en cfg-fil",
"hvordan man åbner cfg fil",
"fil",
"cfg filtypenavn",
"udvidelse"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG-filformat - Citrix-serverforbindelsesfil",
  "description": "Lær om CFG Citrix Server Connection File format og API'er, der kan oprette og åbne CFG filer.",
  "linktitle": "CFG Citrix",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-citrix-da",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## Hvad er en CFG fil?

CFG-fil er også kendt som **Citrix Server Connection File**. Det er vital komponent, der bruges til at etablere forbindelse til Citrix-serveren. Denne fil indeholder væsentlig information, der er nødvendig for en vellykket forbindelse mellem klientenhed og Citrix-server. Det inkluderer typisk detaljer såsom værtsnavn eller IP-adresse på serveren, specifik serverport, der skal bruges, og legitimationsoplysninger, der kræves til godkendelse, som ofte omfatter brugernavn og adgangskode.

Disse CFG-filer spiller en afgørende rolle i konfigurationen af Citrix-klientsoftware, hvilket gør det muligt for brugere at oprette forbindelse til forskellige Citrix-servere problemfrit. De fungerer som konfigurationsfiler, der strømliner forbindelsesprocessen ved at foruddefinere væsentlige parametre, hvilket reducerer behovet for, at brugere manuelt skal indtaste disse oplysninger, hver gang de ønsker at få adgang til Citrix-serveren.

## Citrix server

En Citrix-server, også kendt som Citrix XenApp eller Citrix XenDesktop-server, er specialiseret server, der bruges i Citrix-virtualiseringsløsninger. Citrix er et firma, der leverer teknologi til fjernadgang, applikationsvirtualisering og desktopvirtualisering. Citrix-servere spiller en central rolle i disse løsninger ved at lette leveringen af applikationer og desktop-miljøer til fjernbrugere eller klientenheder.

Her er, hvordan Citrix-serveren typisk fungerer:

1.  **Applikations- og desktoplevering**: Citrix-servere er vært for applikationer og skrivebordsmiljøer. I stedet for at køre software direkte på brugerens enhed, kører applikationen eller skrivebordet på Citrix-serveren, og kun brugergrænsefladen overføres til klientenheden. Dette giver brugerne adgang til Windows-applikationer og desktops fra en lang række enheder, herunder pc'er, Mac'er, tablets og smartphones.
    
2.  **Fjernadgang**: Citrix-servere muliggør fjernadgang til applikationer og desktops, hvilket gør det muligt for brugere at arbejde hvor som helst med en internetforbindelse. Dette er især værdifuldt for fjerntliggende og distribuerede teams, da det giver en ensartet og sikker computeroplevelse.
    
3.  **Load Balancing**: Citrix-servere arbejder ofte i klynger for at afbalancere belastningen af indgående forbindelser. Belastningsbalancering sikrer, at brugeranmodninger fordeles jævnt mellem servere, hvilket optimerer ydeevne og tilgængelighed.

## Citrix-serverforbindelsesfil

En Citrix Server Connection File, ofte omtalt som CFG-fil, er en konfigurationsfil, der bruges i Citrix-miljøer til at etablere forbindelser mellem klientenheder og Citrix-servere. Nøgledetaljer, der typisk er inkluderet i Citrix Server Connection File, kan omfatte:

1.  **Værtsnavn eller IP-adresse**: Dette angiver netværksplaceringen for Citrix-serveren, som klientenheden skal oprette forbindelse til. Den identificerer, hvor Citrix-ressourcer er hostet.
    
2.  **Serverport**: Portnummeret, der bruges til kommunikation med Citrix-serveren. Dette sikrer, at data overføres til korrekt service på serveren.
    
3.  **Brugernavn og adgangskode**: Brugerlegitimationsoplysninger, inklusive brugernavn og adgangskode, kan inkluderes til godkendelsesformål. Disse legitimationsoplysninger giver brugerne mulighed for at bevise deres identitet og få adgang til Citrix-ressourcer.
    
4.  **Forbindelsesindstillinger**: CFG-filer kan indeholde forskellige forbindelsesindstillinger, såsom krypteringsindstillinger, værdier for sessionstimeout og visningsmuligheder. Disse indstillinger hjælper med at konfigurere brugeroplevelse og sikkerhedsparametre.
    
5.  **Ressourcekonfiguration**: Afhængigt af konfigurationen kan CFG-fil angive, hvilke Citrix-ressourcer (applikationer eller desktops) der skal startes, når forbindelsen er etableret.

## Filformater brugt af Citrix

Citrix-servere og relaterede Citrix-teknologier understøtter flere filformater for at muliggøre levering af applikationer, desktops og indhold til fjernbrugere. Her er nogle almindelige filformater forbundet med Citrix-serverinstallationer:

1.  **ICA (Independent Computing Architecture)**:
    
- **.ica**: ICA-filen er kernekomponenten i Citrix's applikations- og desktoplevering. Den indeholder oplysninger om forbindelse til Citrix-serveren, såsom serveradresse, port, krypteringsindstillinger og visningspræferencer. Når brugeren klikker på Citrix-ressourcen, genereres [.ica](/misc/ica/)-filen og bruges af Citrix Receiver (eller Citrix Workspace) klient til at etablere forbindelse.
2.  **Citrix-modtager (eller Citrix Workspace)-pakker**:
    
- **.exe**: Citrix Receiver eller Citrix Workspace installationspakker kommer ofte i eksekverbart format til forskellige operativsystemer (f.eks. [.exe](/executable/exe/) til Windows, [.dmg](/compression/dmg/) til macOS). Disse pakker giver brugerne mulighed for at installere klientsoftware på deres enheder.
3.  **Citrix Workspace App (tidligere Citrix Receiver)**:
    
- **.app**: På macOS er Citrix Workspace-appen pakket som macOS-applikation [.app](/executable/app/)-fil.
4.  **Webbrowserkompatibilitet**:
    
- Citrix-løsninger kan tilgås via webbrowsere, typisk ved hjælp af HTML5 til webbaseret adgang. Brugere opretter forbindelse til Citrix-ressourcer via URL'er uden at kræve specifikke filformater.
5.  **Virtuelle desktopdiskbilleder**:
    
- **.vhd, .vhdx**: Citrix XenDesktop og XenApp kan levere virtuelle skriveborde og applikationer ved hjælp af virtuelle harddisk-[VHD](/disc-and-media/vhd/)- eller [VHDX](/disc-and-media/vhdx/)-filer.
6.  **Resource Publishing Metadata**:
    
- **.xml**: Citrix-administratorer bruger ofte [XML](/web/xml/)-filer til at definere ressourceudgivelsesindstillinger, herunder applikationsegenskaber, adgangspolitikker og brugertildelinger.
7.  **Printerdriverfiler**:
    
- Citrix-miljøer kan kræve specifikke printerdriverfiler (f.eks. .inf) for at sikre korrekt udskrivningsfunktionalitet ved brug af fjernprogrammer.
8.  **Brugerprofildata**:
    
- **.upm**: Citrix Profile Management kan gemme brugerprofildata i .upm-filer for at give ensartede brugeroplevelser på tværs af sessioner og enheder.
9.  **Konfigurationsfiler**:
    
- **.conf**: Forskellige konfigurationsfiler, dvs. kan bruges til at definere indstillinger for Citrix-komponenter, såsom konfigurationsfiler til Citrix License Server (f.eks. CtxLicChk.conf).
10.  **Citrix ADC (NetScaler)-konfiguration**:

- **.nsconfig:** Konfigurationsfiler til Citrix Application Delivery Controllers (ADC), tidligere kendt som NetScaler, lagrer indstillinger relateret til belastningsbalancering, sikkerhed og trafikstyring.

## Hvordan åbner jeg filen CFG?

Programmer, der åbner eller refererer til CFG filer

- Citrix Access Client (Windows, MAC, Linux)

## Andre CFG-filer

Her er andre filtyper, der bruger filtypen **.cfg**.

**Indstillinger**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Spil**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System og diverse**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## Referencer
* [Citrix Virtual Apps](https://en.wikipedia.org/wiki/Citrix_Virtual_Apps)


