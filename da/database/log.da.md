{
  "date": "2021-06-14",
  "keywords": [
"LOG",
"udvidelse",
"logfil",
"logfilformat",
"Database filtype",
"Database filformat",
"hvad er en logfil"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om LOG-filformat og API'er, der kan oprette og åbne LOG-filer.",
  "title": "LOG - Logfilformat",
  "linktitle": "LOG",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-lo-dag"
}
},
  "lastmod": "2021-06-14"
}

## Hvad er en LOG fil?
En fil med filtypenavnet .log indeholder listen over almindelig tekst med tidsstempel. Normalt logges visse aktivitetsdetaljer af softwaren eller operativsystemerne for at hjælpe udviklerne eller brugerne med at spore, hvad der skete på et bestemt tidspunkt. Brugere kan meget nemt redigere disse filer ved at bruge et hvilket som helst tekstredigeringsprogram. Normalt logges fejlrapporterne eller loginaktiviteterne af operativsystemerne, men anden software eller webservere genererer også logfiler for at spore besøgende og overvåge båndbreddeforbrug.

## LOG filformat
LOG-filformatet registrerer de typiske hændelser, der forekommer enten i et operativsystem, meddelelser mellem forskellige brugere af en kommunikationssoftware eller enhver anden software, der kører. Simpelthen kan vi sige, at visse meddelelser på bestemte tidspunkter er logget i en LOG-fil. Nogle almindeligt anvendte termer til logning er:
### Hændelseslogs
Den registrerer hændelser, der forekommer under udførelsen af et system for at spore og forstå systemets aktivitet og for at diagnosticere problemer. De er vigtige for at identificere aktiviteterne i komplekse systemer, typisk i tilfælde af applikationer med meget lidt brugerinteraktion.
### Transaktionslogfiler
Næsten alle databasesystemer vedligeholder transaktionsloggen, som normalt ikke er tænkt som et revisionsspor til senere analyse, og som ikke kan læses af mennesker. Disse logfiler opbevarer kun registreringen af ændringer af de eksisterende data for at gøre det muligt for databasen at genoprette fra nedbrud eller andre datafejl og holde dataene i en konsistent tilstand. Derfor har databasesystemer normalt både generelle hændelseslogfiler og transaktionslogfiler.
### Beskedlogfiler
Den tekstmæssige kommunikation gemt af Internet Relay Chat (IRC), instant messaging-programmer (IM), peer-to-peer fildelingsklienter med chatfunktioner og multiplayer-spil (især MMORPG'er) kaldes beskedlogfiler. Disse logfiler gemmes generelt i almindelige tekstfiler, men IM- og VoIP-klienter (f.eks. Skype) gemmer dem muligvis i HTML-filer for at lette læsningen eller aktivere kryptering.
### Serverlogfiler
Serverlog er faktisk en logfil, der indeholder en liste over aktiviteter, der udføres og oprettes eller vedligeholdes automatisk af serveren selv. Normalt er disse filer ikke tilgængelige for almindelige internetbrugere, kun for webmasteren eller anden administrativ person for en internettjeneste.



## Referencer ##

* [Logfil - Wikipedia](https://en.wikipedia.org/wiki/Log_file)


