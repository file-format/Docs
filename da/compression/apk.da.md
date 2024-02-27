{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APK - Hvad er en APK-fil?",
  "description": "Lær at vide, hvad der er en APK-fil og API'er, der kan oprette og åbne APK-filer.",
  "linktitle": "APK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ap-dak"
}
},
  "lastmod": "2021-04-27"
}

## Hvad er en APK-fil?

En fil med filtypenavnet .apk er en Google Android app-fil, der bruges til at installere apps (applikationer) på Android-enhederne. Den er oprettet som en eksekverbar fil ved hjælp af den officielle IDE Google Android Studio og uploades til Google Play Butik for at blive downloadet og installeret af slutbrugere. APK-filer kan genereres og gøres tilgængelige til manuel installation såvel før udgivelse til Google Play Butik. Dette hjælper med at teste funktionaliteten og adfærden af den genererede APK-pakkefil. Derfor skal man være sikker på, at APK-filen er fra en pålidelig kilde og ikke indeholder malware.

## APK filformat

APK-filer er pakket som komprimerede i [ZIP](/compression/zip/) filformat, der kan åbnes med enhver ZIP-fil åbningssoftware. .apk-udvidelsen af en sådan fil kan omdøbes til .zip og åbne filen i ethvert ZIP-program eller udpakke dens indhold.

## APK-pakkeindhold

En enkelt APK-fil indeholder alle de nødvendige filer, der kræves til installation og udførelse. En APK-fil, når den udpakkes med et ZIP-program, indeholder følgende filer og mapper.

 * `META-INF/`: Bibliotek, der indeholder manifestfilen, signaturen og en liste over ressourcer i arkivet
 * `lib/`: Katalog indeholdende kompileret kode relateret til specifikke platforme såsom armeabi-v7a, x86, arm64-v8a osv.
 * `res/`: Bibliotek, der indeholder ikke-kompilerede ressourcer såsom billeder
 * `assets/`: Katalog indeholdende applikationsaktiver, som kan hentes af AssetManager.
 * `androidManifest.xml`: Indeholder navnet, versionsoplysningerne og indholdet af APK-filen
 * `classes.dex`: Disse er kompilerede Java-klasser, der kan køres på Dalvik virtuel maskine og af Android Runtime
 * `resources.arsc`: Kompileret ressourcefil såsom strenge

## Sådan åbner du APK-filer

APK-filer er beregnet til at blive installeret på Android-enheder. Derudover er Windows 11 den første version af Windows, der officielt understøtter funktionen til at installere APK-filer.

### Sådan installeres APK-fil på Android-enhed

For at installere en APK-fil på dine Android-enheder kan følgende trin bruges.

 1. Download APK'en ved hjælp af webbrowser
 2. Tryk på det - du skulle derefter kunne se det downloades på den øverste bjælke på din enhed
 3. Når den er downloadet, skal du åbne Downloads, trykke på APK-filen og trykke på Ja, når du bliver bedt om det.

Ved at følge disse trin starter installationen af appen på din enhed.

### Sådan åbnes en APK-fil på Windows

Du kan bruge en Android-emulator på Windows-pc til at åbne/få adgang til en APK-fil. BlueStacks er en sådan Android-emulator, der kan bruges til at åbne en Android-emulator på Windows. Hvis du bruger Windows 11, er du heldig, da Windows 11 officielt understøtter muligheden for at installere APK-filer.

### Sådan åbnes APK-fil på Mac

Du kan også bruge BlueStack på macOS og åbne APK-filer. Det er en gratis Android-emulator og giver dig mulighed for at bruge den som den bedste måde at få adgang til kun Android-apps.

## Sådan opretter du en APK-fil

Oprettelse af en APK-fil kræver brug af specialiserede værktøjer og udviklingsmiljøer. Android-udviklere bruger primært Android Studio, det officielle integrerede udviklingsmiljø (IDE) til Android-appudvikling. Her er en generel oversigt over de trin, der er involveret i at oprette en APK-fil:

 1. **Konfigurer udviklingsmiljøet:** Installer og opsæt Android Studio på din computer. Android Studio tilbyder et omfattende sæt værktøjer til at udvikle, teste og pakke Android-apps.
 1. **Udvikl din app:** Brug programmeringssprogene Java eller Kotlin til at skrive koden til din Android-app. Android Studio tilbyder et rigt sæt funktioner og ressourcer til at hjælpe dig med at bygge din app, herunder kodeeditorer, emulatorer og fejlfindingsværktøjer.
 1. **Byg appen:** Når du er færdig med at skrive koden og designe brugergrænsefladen, skal du bruge Android Studios byggeværktøjer til at kompilere og pakke din app. Denne proces genererer de nødvendige filer og ressourcer til APK-filen.
 1. **Skriv under APK-filen:** Før du distribuerer din app, er det vigtigt at underskrive APK-filen. App-signering sikrer integriteten og ægtheden af appen. Android Studio giver dig mulighed for at generere en signeringsnøgle og signere din APK-fil ved hjælp af denne nøgle.
 1. **Distribuer APK-filen:** Når du har underskrevet din APK-fil, kan du distribuere den gennem forskellige kanaler. Du kan uploade det til Google Play Butik til distribution til et bredt publikum eller dele det direkte med brugere via e-mail, downloadlinks eller andre distributionsplatforme.

Det er værd at bemærke, at APK-filen, der genereres fra Android Studio, typisk er optimeret til produktionsbrug. Under udviklingsprocessen kan du også generere debug APK-filer, som er nyttige til test- og fejlretningsformål, men ikke beregnet til distribution.

## Ofte stillede spørgsmål

 * **Kan APK-filer skade min enhed?** APK-filer har potentiale til at udgøre en trussel mod enheder. Dette skyldes muligheden for, at malware er til stede i dem. Derfor er det tilrådeligt at udsætte APK-filer for en online virusscanning, før du fortsætter med installationen. Derudover er det en fornuftig foranstaltning at bruge en Android-antivirus-app. For at mindske risikoen for, at din enhed bliver offer for et vildledende program, er det bedst at downloade fra pålidelige kilder, som du er fortrolig med og har tillid til.

 * **Er APK-filer lovlige?** At downloade APK-filer og bruge dem til app-installationer fra andre kilder end Google Play Butik er helt inden for lovens grænser. APK, beslægtet med formater som EXE eller ZIP, er et filformat. Selvom Google var banebrydende for dette format, er det åbent for alle at generere og anvende APK-filer.

 * **Hvordan finder jeg APK-filer på min Android-enhed?** APK-filer forbliver skjulte for brugerne, da Android administrerer app-installationer i baggrunden, uanset om det er via Google Play eller en anden applikationsdistributionsplatform. APK-filer, der er downloadet fra andre kilder, kan dog findes med Android-filhåndteringen.

## Referencer

* [APK-filformat](https://en.wikipedia.org/wiki/Android_application_package)


