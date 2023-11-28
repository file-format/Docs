{
"datum": "27-09-2023",
  "keywords": [
"cfg",
"cfg-bestand",
"cfg wesnoth markup-taalbestand",
"wat is een cfg-bestand",
"hoe cfg-bestand te openen",
"bestand",
"cfg-bestandsextensie",
"verlenging"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title":"CFG-bestandsindeling - Wesnoth Markup Language-bestand",
  "description":"Meer informatie over het CFG Wesnoth Markup Language-bestandsformaat en API's waarmee CFG-bestanden kunnen worden gemaakt en geopend.",
"linktitle":"CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent" : "game"
}
},
"laatste mod": "27-09-2023"
}

## Wat is een CFG-bestand?

CFG-bestand is ook bekend als de **"Wesnoth Markup Language" (WML)**. Het is een aangepaste opmaaktaal die voornamelijk wordt gebruikt in het spel "Battle for Wesnoth", een turn-based strategiespel. WML wordt gebruikt om verschillende aspecten van het spel te definiëren en aan te passen, waaronder scenario's, campagnes, eenheden en meer. Het is een manier voor modders en ontwikkelaars om inhoud voor de game te creëren.

Het is geschreven in een formaat dat lijkt op een combinatie van XML en eenvoudige scripting. Hier is een overzicht van enkele veelvoorkomende elementen en structuren die u in een WML-bestand kunt tegenkomen:

1. **Tags:** WML gebruikt tags om verschillende elementen in het spel te definiëren. Tags staan tussen punthaken. Bijvoorbeeld:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Attributen:** Binnen tags kunt u attributen definiëren om eigenschappen of waarden op te geven die aan het element zijn gekoppeld. In het bovenstaande voorbeeld zijn 'type' en 'hitpoints' attributen.
    










3. **Matrices en arrays van arrays:** U kunt arrays met gegevens en zelfs arrays van arrays maken om lijsten met eenheden, terreintypen of andere spelelementen te definiëren.
    










4. **Voorwaardelijke uitspraken:** WML ondersteunt voorwaardelijke uitspraken om het verloop van het spel te controleren. Bijvoorbeeld:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Loops:** U kunt loops gebruiken om door lijsten met items te bladeren of herhaaldelijk acties uit te voeren.
    










6. **Inclusief:** U kunt andere WML-bestanden opnemen in een hoofd-WML-bestand om uw inhoud te ordenen en te modulariseren.
    










7. **Gebeurtenishandlers:** U kunt gebeurtenishandlers definiëren om acties te activeren wanneer specifieke gebeurtenissen in het spel plaatsvinden.
    











Hier is een vereenvoudigd voorbeeld van een WML-bestand dat een aangepaste eenheid definieert:

```
[unit_type]
    id=my_custom_unit
    name="Custom Unit"
    description="A unit created using WML."
    image="units/my_custom_unit.png"
    hitpoints=30
    movement_type=foot
[/unit_type]
```

## De strijd om Wesnoth

"The Battle for Wesnoth" is een populair en open-source turn-based strategiespel. Het is beschikbaar voor meerdere platforms, waaronder Mac, Windows, Linux en meer. De game is ontwikkeld door een toegewijde gemeenschap van vrijwilligers en staat bekend om zijn diepgaande en boeiende gameplay, maar ook om zijn rijke fantasiewereld.

De belangrijkste kenmerken van "The Battle for Wesnoth" zijn onder meer:

1. **Fantasiesetting:** De game speelt zich af in een fantasiewereld met verschillende rassen, waaronder mensen, elfen, dwergen, orcs en meer. De kennis en het verhaal van de game vormen een integraal onderdeel van de aantrekkingskracht ervan.
    










2. **Turn-based strategie:** De gameplay is turn-based, waarbij spelers de tijd nemen om hun bewegingen op zeshoekige rasters te plannen en uit te voeren. Het combineert tactische gevechten met strategische besluitvorming.
    










3. **Campagnes:** De game biedt een breed scala aan campagnes voor één speler, elk met zijn eigen verhaallijn, personages en uitdagingen. Spelers kunnen verschillende verhalen en scenario's verkennen.
    










4. **Multiplayer:** "Wesnoth" ondersteunt online multiplayer, waardoor spelers tegen elkaar kunnen strijden in strategische gevechten. Multiplayer-modi omvatten coöperatief spel en competitieve wedstrijden.

## Hoe open je een CFG-bestand?

CFG-bestanden, die gewoonlijk worden geassocieerd met de Wesnoth Markup Language (WML) die wordt gebruikt in het spel "The Battle for Wesnoth", kunnen eenvoudig worden bewerkt met elke standaard teksteditor. Deze bestanden bevatten voor mensen leesbare code geschreven in WML, die verschillende aspecten van het spel definieert, waaronder scenario's, eenheden en campagnes.

Hoewel je elke teksteditor kunt gebruiken om CFG-bestanden te wijzigen, hebben sommige geavanceerde teksteditors zoals Emacs en Vi WML-syntaxisaccentuerende plug-ins beschikbaar. Deze plug-ins bieden handige kleurcodering en opmaak, zodat gebruikers gemakkelijker verschillende elementen en structuren binnen de WML-code kunnen onderscheiden.

Programma's die CFG-bestanden openen of ernaar verwijzen, omvatten

- De strijd om Wesnoth (gratis) voor (Windows, MAC, Linux)
- Microsoft Kladblok

## Andere CFG-bestanden

Hier volgen andere bestandstypen die de bestandsextensie **.cfg** gebruiken.

**Instellingen**
- [CFG - Celestia-configuratiebestand] (/nl/settings/cfg-celestia/)
- [CFG - Citrix-serververbindingsbestand](/nl/settings/cfg-citrix/)
- [CFG - MAME-configuratiebestand] (/nl/settings/cfg-mame/)
- [CFG - LightWave-configuratiebestand] (/nl/settings/cfg-lightwave/)

**Spel**
- [CFG - Wesnoth Markup Language-bestand] (/nl/game/cfg-wesnoth/)
- [CFG - MUGEN-configuratiebestand] (/nl/game/cfg-mugen/)
- [CFG - Bronengineconfiguratiebestand](/nl/game/cfg-sourceengine/)

**Systeem en Diversen**
- [CFG - CFG-bestand](/nl/system/cfg/)
- [CFG - Cal3D-modelconfiguratiebestand] (/nl/misc/cfg-cal3d/)

## Referenties
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
