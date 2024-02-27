{
  "date": "2022-02-16",
  "keywords": [
"obb fil",
"obb filformat",
"hvad er en obb-fil",
"fil",
"obb eksempel",
"obb filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBB-filformat - Android uigennemsigtig binær blob-fil",
  "description": "Lær om OBB-filformat og API'er, der kan oprette og åbne OBB-filer.",
  "linktitle": "OBB",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-ob-dab"
}
},
  "lastmod": "2022-02-16"
}

## Hvad er OBB fil?

En OBB-fil er en udvidelsesfil, der indeholder yderligere data, der er ud over Android [APK](/compression/apk/)-filen. Google Play Butik tillader ikke at have en Android APK-fil med en størrelse på mere end 100 MB. Men nogle applikationer kræver muligvis højopløsningsgrafik, mediefiler eller andre store aktiver, der skal hostes ud over APK-filerne. Det er her OBB-filtyperne kommer ind. Google Play giver mulighed for at vedhæfte disse udvidelsesfiler som et supplement til APK-filen.

## OBB filformat

OBB-filer gemmes som binære filer sammen med APK-filerne. Når en APK ledsager OBB-filerne, hoster Google Play udvidelsesfilerne på sin server, og udvikleren opkræves ingen ekstra omkostninger. Disse ekstra filer gemmes på enhedens delte lager på SD-kort eller USB-monterbar partition, når appen downloades til installation.

OBB-filerne downloades og installeres ved download. Men i nogle tilfælde downloades disse til installation, når applikationen køres for første gang.

### OBB Maksimal filstørrelse

Google Play Butik giver dig mulighed for at uploade OBB-udvidelsesfiler med en størrelse på op til 2 GB. Filer i store størrelser anbefales at blive uploadet som komprimerede [ZIP](/compression/zip/) filer for effektiv upload via internettet.

Disse udvidelsesfiler kan hostes enten som **hoved** primær udvidelsesfil for yderligere ressourcer, der kræves af appen, eller en valgfri patchudvidelsesfil beregnet til små opdateringer til hovedudvidelsesfilen.

## Referencer

* [Android-udviklere - Udvidelsesfiler](https://developer.android.com/google/play/expansion-files)


