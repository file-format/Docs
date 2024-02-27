{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOCK-filformat - Hvad er en Lock-fil?",
  "description": "Lær om LOCK-filformatet og dets .",
  "linktitle": "LOCK",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-loc-dak"
}
},
  "lastmod": "2022-01-26"
}

## Hvad er en LOCK fil?

En **LOCK**-fil er en omdøbt fil, der bruges af programmer og operativsystemer til at markere en fil eller en enhed som låst. Dette fortæller andre programmer ikke at bruge filen, medmindre den er fri for den applikation, der bruger den. I de fleste tilfælde er disse låsefiler tomme, men i andre tilfælde kan de indeholde oplysninger relateret til låsen såsom egenskaber og indstillinger.

Nogle gange bruges .lock-filen af Microsofts .NET Framework til at oprette **lockeed**-kopier af en databasefil. I et sådant tilfælde åbnes en kopi af databasefilen med filtypen .lock. Dette tillader ikke brugeren at foretage ændringer i filen, mens den er i brug af en anden bruger.

## LÅS filformat - flere oplysninger

En LOCK-fil oprettes af hver applikation, og dens filformat er specifikt for applikationen. Disse låsefiler kan gemmes i både tekst- og binært filformat.

Tilstedeværelsen af låsefiler forhindrer samtidig adgang af en ressource til flere filer, der forsøger at få adgang til den ressource. En kopi af den originale fil oprettes med filtypenavnet .lock suffikset. Dette fortæller andre programmer at have skrivebeskyttet adgang til filen. For eksempel bliver resource.dat til resource.data.lock.

For Ruby programmeringssprog kan du støde på filen **gemfile.lock**. Det er her Bundler registrerer de nøjagtige versioner, der blev installeret. Når et projekt/bibliotek flyttes til en anden maskine, vil den kørende bundle således se på Gemfilen for den nøjagtige relevante version.

## Lås fil i Linux

Linux understøtter to typer fillåse: rådgivende låse og obligatoriske låse.

 * **Rådgivende låse**: Type låsning, der ikke håndhæves. I dette tilfælde samarbejder de deltagende processer med hinanden og opnår eksplicit låse. Hvis dette ikke er muligt, ignoreres rådgivende låse.

 * **Obligatoriske låse**: I tilfælde af obligatorisk låsning håndhæver operativsystemet fillåsningen ved at forhindre andre processer i at læse eller skrive filen. Dette kræver ikke noget samarbejde mellem processerne.

obligatorisk låsning kræver ikke noget samarbejde mellem de deltagende processer. Når en obligatorisk lås er aktiveret på en fil, forhindrer operativsystemet andre processer i at læse eller skrive filen.

## Referencer

* [GemFile og Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)

* [Låsning i Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)


