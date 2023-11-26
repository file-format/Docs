{
"datum": "2023-06-12",
  "keywords": [
"bakken",
"bak-bestand",
"BAK Chroom Bladwijzers",
"wat is een bak-bestand",
"hoe bak-bestand te openen",
"bestand",
"bak bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"BAK-bestandsindeling - Back-up van Chromium-bladwijzers",
  "description":"Leer meer over het BAK Chromium Bookmarks-formaat en API's waarmee BAK-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"BAK Chromium-bladwijzers",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
"parent":"diversen"
}
},
"laatste mod": "2023-06-12"
}

## Wat is een BAK-bestand?

Een .bak-bestand in de context van Chromium-gebaseerde webbrowsers, zoals Google Chrome en Microsoft Edge, is in wezen een back-upbestand van uw bladwijzers. Deze bladwijzers worden opgeslagen als een lijst met platte tekst en het gebruikte bestandsformaat is JSON. Het doel van deze .bak-bestanden is om uw bladwijzers te beschermen door een back-up te bieden die kan worden hersteld in geval van onbedoelde verwijdering of verlies.

Chromium-gebaseerde browsers, waaronder Google Chrome, maken deze back-upbestanden routinematig en geven ze meestal de naam 'Bookmarks.bak'. Ze zijn in wezen een momentopname van uw bladwijzers op een specifiek tijdstip.

## Een .bak-bestand gebruiken om uw bladwijzers te herstellen

1. **Zoek het back-upbestand:** Het bevindt zich meestal in een specifieke map die is gekoppeld aan uw Chromium-profiel. De exacte locatie kan variëren, afhankelijk van uw besturingssysteem.

Op Windows: kijk in `C:\Gebruikers\<YourUsername> \AppData\Local\Chromium\Gebruikersgegevens\Default\Bookmarks.bak`.

Op macOS: Zoek in `~/Library/Application Support/Chromium/Default/Bookmarks.bak`.

Op Linux: Vink `~/.config/chromium/Default/Bookmarks.bak` aan.

3. Zorg ervoor dat uw Chromium-browser gesloten is.
4. Hernoem het bestand "Bookmarks.bak" door de extensie ".bak" te verwijderen, zodat het eenvoudigweg "Bookmarks" heet.
5. Start Chromium.

Door het .bak-bestand te hernoemen naar 'Bladwijzers', gebruikt Chromium het als het huidige bladwijzerbestand en moeten uw vorige bladwijzers worden hersteld.

## Back-up van Chromium-bladwijzers

Het maken van een back-up van uw Chromium-bladwijzers is een verstandige voorzorgsmaatregel om ervoor te zorgen dat u uw belangrijke opgeslagen webpagina's en URL's niet kwijtraakt. Chromium is een open-source browser die dient als basis voor andere browsers zoals Google Chrome en Microsoft Edge. Volg deze stappen om een back-up van uw Chromium-bladwijzers te maken:

## Methode 1: Handmatige back-up

1. **Open Chromium**: Start de Chromium-browser op uw computer.

2. **Toegang tot bladwijzers**: klik op de drie verticale stippen (menupictogram) in de rechterbovenhoek van het browservenster. Beweeg vanuit het vervolgkeuzemenu over 'Bladwijzers' om het bladwijzersubmenu weer te geven.

3. **Bladwijzers exporteren**: klik in het bladwijzersubmenu op 'Bladwijzerbeheer'. Er wordt een nieuw tabblad geopend met uw bladwijzers.

4. **Bladwijzers exporteren**: Klik op het tabblad Bladwijzerbeheer nogmaals op de drie verticale stippen (meestal in de rechterbovenhoek) om het menu Bladwijzerbeheer te openen. Selecteer in dit menu 'Bladwijzers exporteren'.

5. **Kies locatie**: kies waar u het geëxporteerde bladwijzerbestand op uw computer wilt opslaan. De standaardbestandsnaam is 'bookmarks.html', maar u kunt deze desgewenst wijzigen. Bewaar het op een locatie die u zich zult herinneren.

6. **Opslaan**: klik op de knop "Opslaan" of "Exporteren" om uw bladwijzers op te slaan als HTML-bestand.

Er is nu een back-up van uw bladwijzers gemaakt als HTML-bestand. U kunt dit bestand voor bewaring naar een externe schijf of cloudopslag kopiëren.

## Methode 2: Synchroniseren met Google-account (indien van toepassing)

Als u bent ingelogd op een Google-account in Chromium, kunt u ook de ingebouwde synchronisatiefunctie gebruiken om uw bladwijzers veilig en gesynchroniseerd te houden op verschillende apparaten. Op deze manier wordt er automatisch een back-up van uw bladwijzers gemaakt in uw Google-account.

1. **Open Chromium**: Start de Chromium-browser en zorg ervoor dat u bent aangemeld bij uw Google-account.

2. **Synchronisatie inschakelen**: Klik op de drie verticale stippen (menupictogram) in de rechterbovenhoek van het browservenster en ga naar 'Instellingen'.

3. **Synchronisatie en Google-services**: klik op het tabblad Instellingen op 'Synchronisatie en Google-services' in de linkerzijbalk.

4. **Uw gegevens synchroniseren**: Zorg ervoor dat onder 'Synchroniseren' 'Bladwijzers' is ingeschakeld. Hiermee worden uw bladwijzers gesynchroniseerd met uw Google-account.

Er wordt nu automatisch een back-up van uw bladwijzers gemaakt en gesynchroniseerd met uw Google-account. Je kunt ze openen door in te loggen op je Google-account op elk apparaat met Chromium of een andere browser die Google-synchronisatie ondersteunt.

Vergeet niet om regelmatig handmatig een back-up van uw bladwijzers te maken, vooral als u een lokale kopie wilt die niet alleen afhankelijk is van de synchronisatie van uw Google-account.

## Hoe open je een BAK-bestand

Als u de onbewerkte gegevens van uw bladwijzerback-up wilt verkennen, kunt u het bestand "Bookmarks.bak" openen met verschillende teksteditors zoals Microsoft Visual Studio Code (beschikbaar op meerdere platforms), Microsoft Notepad (voor Windows-gebruikers), Apple TextEdit (voor Mac-gebruikers) of een andere teksteditor naar keuze. Als u dit doet, kunt u de bladwijzers en metagegevens in het bestand bekijken.

U kunt het bestand "Bookmarks.bak" openen en de inhoud ervan bekijken met behulp van verschillende tekstbewerkingssoftware en code-editors. Hier zijn enkele veelgebruikte opties:

1. Visual Studio-code (VS-code)
2. Kladblok (Windows)
3. Teksteditor (Mac)
4. Sublieme tekst
5. Kladblok++
6. Atoom
7. nano en Vim (Linux)
8. WordPad (Windows)

## Andere BAK-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.bak** gebruiken.

**Databank**
- [BAK - Databaseback-upbestand](/nl/database/bak/)
- [BAK - Swiftpage Act! Databaseback-up](/nl/database/bak-act/)
- [BAK - Back-up van Microsoft SQL Server-database](/nl/database/bak-sqlserver/)

**Spel**
- [BAK - Terraria World of Spelerback-up](/nl/game/bak-terraria/)

**Overige**
- [BAK - Back-upbestand](/nl/misc/bak-backup/)
- [BAK - Finale 2012 Score Backup](/nl/misc/bak-finale/)
- [BAK - MobileTrans Backup](/nl/misc/bak-mobiletrans/)
- [BAK - VEGAS Video Project Back-up](/nl/misc/bak-vegas/)

**Instellingen**
- [BAK - Back-up van Holo Launcher] (/nl/settings/bak-holo/)

## Referenties
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
