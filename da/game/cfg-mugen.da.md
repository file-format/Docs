{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg fil",
"cfg mugen konfigurationsfil",
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
  "title": "CFG-filformat - MUGEN-konfigurationsfil",
  "description": "Lær om CFG MUGEN Configuration File format og API'er, der kan oprette og åbne CFG filer.",
  "linktitle": "CFG M.U.G.E.N",
  "menu": {
    "docs": {
      "identifier": "game-cfg-mugen-da",
      "parent": "game"
}
},
  "lastmod": "2023-09-27"
}

## Hvad er en CFG fil?

CFG-fil i sammenhæng med MUGEN refererer til MUGEN-konfigurationsfil. **MUGEN** er tilpasselig 2D-kampspilsmotor udviklet af Elecbyte. Brugere kan skabe deres egne karakterer, scener og endda ændre spillets adfærd og regler ved at redigere forskellige konfigurationsfiler, herunder CFG-filer.

Her er en grundlæggende oversigt over, hvad du kan finde i MUGEN `.cfg`-fil:

1.  **Systemkonfiguration**: CFG-filer indeholder ofte indstillinger relateret til generel opførsel af spilmotoren. Dette inkluderer ting som skærmopløsning, lydindstillinger og inputkonfiguration (tastatur-, joystick- eller controller-tilknytninger).
    
2.  **Standarder for tegn og scener**: Du kan definere standardindstillinger for karakterer og stadier. For eksempel kan du angive, hvilke karakterer og stadier der skal indlæses, når spillet starter.
    
3.  **Spillemuligheder**: MUGEN `.cfg`-filer kan også styre forskellige spilmuligheder såsom runde tidsgrænser, skadeskalering og mere.
    
4.  **Fejlretning og udvikling**: Avancerede brugere kan bruge `.cfg`-filer til fejlfinding og udviklingsformål. Disse indstillinger kan styre, hvordan fejlretningsoplysninger vises på skærmen eller definere anden udviklingsrelateret adfærd.
    
5.  **Skærmpakkekonfiguration**: Skærmpakker er visuelle temaer, der ændrer spillets udseende og følelse. `.cfg` filer kan specificere hvilken screenpack der bruges og konfigurere dens forskellige elementer.
    
6.  **AI-adfærd**: MUGEN giver dig mulighed for at definere, hvordan computerstyrede karakterer (AI) opfører sig i kampe. `.cfg`-filer kan indeholde indstillinger relateret til AI-besvær og adfærd.

## MUGEN konfigurationsfil 

En MUGEN CFG (konfiguration) fil er en afgørende komponent for skabere i en verden af tilpassede kampspil. Det giver dem mulighed for at forme grundlæggende spilleregler. Dette inkluderer faktorer som, hvor længe hver runde varer, udfordringsniveau præsenteret af computerstyrede modstandere, spillets tempo, i hvilken grad kombinationer påvirker skaden og meget mere.

Desuden giver CFG-filen skabere mulighed for at bestemme spillets skærmindstillinger, såsom skærmopløsning og beslutte, om MUGEN skal afspille lydeffekter og musik under gameplay. For dem, der er velbevandret i MUGENs forviklinger, tilbyder denne fil potentiale til at finjustere en række andre spilrelaterede indstillinger for at skabe en unik spiloplevelse.

Som standard ligger MUGENs primære CFG-fil, kendt som `mugen.cfg`, i programmets datamappe. Selvom det er muligt direkte at redigere spillets indstillinger i denne fil, er det generelt tilrådeligt at oprette en sikkerhedskopi først. Denne forholdsregel sikrer, at du ubesværet kan vende tilbage til MUGENs oprindelige indstillinger, hvis det er nødvendigt, for at forhindre utilsigtede ændringer i at forstyrre din spiloplevelse.

## MUGEN - Game Engine

MUGEN er alsidig og meget tilpasselig 2D-kampspilmotor udviklet af Elecbyte. Navnet MUGEN står for Mugen Ultimate Game Engine. Det blev oprindeligt udgivet i 1999 og har siden fået et dedikeret fællesskab af brugere og skabere, der bruger motor til at designe og udvikle deres egne 2D-kampspil.

Her er nogle nøglefunktioner og aspekter af MUGEN:

1.  **Tilpasbare karakterer:** MUGEN giver brugerne mulighed for at skabe og importere deres egne karakterer (kendt som fighters eller sprites) til spillet. Skabere kan designe unikke bevægelsessæt, animationer og specielle angreb til disse karakterer, hvilket gør det muligt at inkludere praktisk talt enhver karakter fra forskellige franchises eller originale kreationer.
    
2.  **Stadier:** Ud over karakterer kan brugere også oprette og tilpasse stadier, hvor kampe finder sted. Disse stadier kan have interaktive elementer og unikke baggrunde.
      
3.  **Screenpacks:** Screenpacks are visual themes that change overall appearance of game, including menus, character selection screens and life bars. Users can create and share their own screenpacks to give their games unique look and feel.
    
4.  **Lyd og musik:** Skabere kan tilføje lydeffekter og baggrundsmusik til deres spil, hvilket forbedrer den samlede spiloplevelse.
    
5.  **Scripting:** Avancerede brugere kan bruge indbygget scriptsprog til at skabe kompleks karakteradfærd, unik spilmekanik og specielle effekter.

## Hvordan åbner jeg filen CFG?

MUGEN CFG-filer er almindelige tekstdokumenter, der gør dem tilgængelige med forskellige teksteditorer. På Windows kan du bruge Microsoft Notepad eller WordPad, mens macOS-brugere kan bruge Apple TextEdit til dette formål. Disse editorer giver brugerne mulighed for nemt at se og ændre konfigurationsindstillinger i CFG-filer.

Programmer, der åbner eller refererer til CFG filer

- Elecbyte MUGEN
- Notesblok
- Tekstredigering

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
* [Mugen (spilmotor)](https://en.wikipedia.org/wiki/Mugen_(game_engine))


