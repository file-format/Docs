{
  "date": "2019-10-11",
  "keywords": [
"arsc",
".arsc",
"hvad er en arsc-fil",
"hvordan man åbner arsc fil",
"udvidelse",
"fil",
"arsc-fil",
"arsc filformat",
"arsc filtypenavn",
"arsc fil eksempel"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ARSC - Android Package Resource Table File ",
  "description": "Lær om ARSC filformat og API'er, der kan oprette og åbne ARSC fil.",
  "linktitle": "ARSC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ars-dac"
}
},
  "lastmod": "2021-06-22"
}

## Hvad er en ARSC fil?

En ARSC-fil er en Android-ressourcetabelfil, der indeholder applikationens liste over ressourcer i et tabelformat. Dette indeholder oplysninger såsom ressourcenavne, egenskaber og id'er. ARSC-filer er en del af APK-pakker, der bruges til at installere disse Android-apps. Alle ressourcer såsom billeder, layout, stilarter og strenge i en Android-applikation konverteres til binære filer, når APK-filen genereres. ARSC-filen er også genereret på samme måde, der indeholder en liste over alle programmets kompilerede ressourcer og deres ID'er.

## ARSC filformat

.arsc-udvidelsesfilerne er binære filer, der er genereret efter compileren, såsom ANT (Eclipse) eller Gradle (AS), kompilerer Android-applikationskoden for at producere [APK](/compression/apk/)-filen. Du kan udpakke APK-filen ved hjælp af et hvilket som helst arkiveringsværktøj såsom WinZip for at se indholdet, som er de kompilerede java-klassefiler, dvs. classes.dex. Ud over disse indeholder den også denne ARSC-fil, der indeholder metainformation om:

 * XML-noder
 * Egenskaberne
 * Ressource-id'erne

Ressourcer i en APK-fil henvises af ressource-id'erne, mens attributterne opløses til en værdi ved kørsel. Android aapt-værktøjet indsamler alle de ressourcer, der er defineret i filer på byggetidspunktet og tildeler ressource-id'er til dem. Efter identifikatorer er tildelt de kompilerede ressourcer, genereres en R.java-fil fra kildekoden såvel som resources.arsc.

## Referencer

* [Binær ressourcetabelstruktur](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)


