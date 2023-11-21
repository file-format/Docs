{
"Datum": "27.09.2023",
  "keywords": [
"cfg",
"cfg-Datei",
"cfg Wesnoth Markup Language-Datei",
"Was ist eine CFG-Datei",
"Wie öffnet man eine CFG-Datei",
"Datei",
"cfg-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "CFG-Dateiformat – Wesnoth Markup Language-Datei",
  "description":"Erfahren Sie mehr über das CFG Wesnoth Markup Language-Dateiformat und die APIs, mit denen CFG-Dateien erstellt und geöffnet werden können.",
"linktitle": "CFG Wesnoth",
  "menu": {
    "docs": {
      "identifier": "game-cfg-wesnoth",
"parent": "Spiel"
}
},
"lastmod": "27.09.2023"
}

## Was ist eine CFG-Datei?

Die CFG-Datei ist auch als **"Wesnoth Markup Language" (WML)** bekannt. Es handelt sich um eine benutzerdefinierte Auszeichnungssprache, die hauptsächlich im Spiel "Battle for Wesnoth" verwendet wird, einem rundenbasierten Strategiespiel. WML wird verwendet, um verschiedene Aspekte des Spiels zu definieren und anzupassen, darunter Szenarien, Kampagnen, Einheiten und mehr. Es ist eine Möglichkeit für Modder und Entwickler, Inhalte für das Spiel zu erstellen.

Es ist in einem Format geschrieben, das einer Kombination aus XML und einfachem Scripting ähnelt. Hier finden Sie einen Überblick über einige häufig vorkommende Elemente und Strukturen, die Sie möglicherweise in einer WML-Datei finden:

1. **Tags:** WML verwendet Tags, um verschiedene Elemente im Spiel zu definieren. Tags sind in spitze Klammern eingeschlossen. Zum Beispiel:

```
[unit]
    type=Elvish Archer
    hitpoints=25
[/unit]
```
    










2. **Attribute:** Innerhalb von Tags können Sie Attribute definieren, um Eigenschaften oder Werte anzugeben, die mit dem Element verknüpft sind. Im obigen Beispiel sind "Typ" und "Hitpoints" Attribute.
    










3. **Arrays und Arrays von Arrays:** Sie können Arrays von Daten und sogar Arrays von Arrays erstellen, um Listen von Einheiten, Geländetypen oder anderen Spielelementen zu definieren.
    










4. **Bedingte Anweisungen:** WML unterstützt bedingte Anweisungen, um den Spielfluss zu steuern. Zum Beispiel:

```
[if]
    condition=have_unit
    variable=x,y
[/if]
```
    










5. **Schleifen:** Sie können Schleifen verwenden, um Listen von Elementen zu durchlaufen oder Aktionen wiederholt auszuführen.
    










6. **Beinhaltet:** Sie können andere WML-Dateien in eine Haupt-WML-Datei einbinden, um Ihre Inhalte zu organisieren und zu modularisieren.
    










7. **Ereignishandler:** Sie können Ereignishandler definieren, um Aktionen auszulösen, wenn bestimmte Ereignisse im Spiel auftreten.
    











Hier ist ein vereinfachtes Beispiel einer WML-Datei, die eine benutzerdefinierte Einheit definiert:

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

## Die Schlacht um Wesnoth

"The Battle for Wesnoth" ist ein beliebtes rundenbasiertes Open-Source-Strategiespiel. Es ist für mehrere Plattformen verfügbar, darunter Mac, Windows, Linux und mehr. Das von einer engagierten Freiwilligengemeinschaft entwickelte Spiel ist für sein tiefgründiges und fesselndes Gameplay sowie seine reichhaltige Fantasiewelt bekannt.

Zu den Hauptmerkmalen von "The Battle for Wesnoth" gehören:

1. **Fantasy-Setting:** Das Spiel spielt in einer Fantasy-Welt mit verschiedenen Rassen, darunter Menschen, Elfen, Zwerge, Orks und mehr. Die Geschichte und das Geschichtenerzählen des Spiels sind ein wesentlicher Bestandteil seines Reizes.
    










2. **Rundenbasierte Strategie:** Das Gameplay ist rundenbasiert, wobei sich die Spieler Zeit nehmen, ihre Bewegungen auf sechseckigen Gittern zu planen und auszuführen. Es kombiniert taktischen Kampf mit strategischer Entscheidungsfindung.
    










3. **Kampagnen:** Das Spiel bietet eine große Auswahl an Einzelspieler-Kampagnen, jede mit eigener Handlung, Charakteren und Herausforderungen. Spieler können verschiedene Erzählungen und Szenarien erkunden.
    










4. **Multiplayer:** "Wesnoth" unterstützt den Online-Multiplayer, sodass Spieler in strategischen Schlachten gegeneinander antreten können. Zu den Mehrspielermodi gehören kooperatives Spielen und kompetitive Spiele.

## Wie öffne ich eine CFG-Datei?

CFG-Dateien, die üblicherweise mit der im Spiel "The Battle for Wesnoth" verwendeten Wesnoth Markup Language (WML) verknüpft sind, können problemlos mit jedem Standard-Texteditor bearbeitet werden. Diese Dateien enthalten in WML geschriebenen, für Menschen lesbaren Code, der verschiedene Aspekte des Spiels definiert, darunter Szenarien, Einheiten und Kampagnen.

Während Sie zum Ändern von CFG-Dateien jeden Texteditor verwenden können, verfügen einige erweiterte Texteditoren wie Emacs und Vi über WML-Syntaxhervorhebungs-Plugins. Diese Plugins bieten hilfreiche Farbcodierung und Formatierung, um Benutzern die Unterscheidung verschiedener Elemente und Strukturen im WML-Code zu erleichtern.

Zu den Programmen, die CFG-Dateien öffnen oder darauf verweisen, gehören:

- Die Schlacht um Wesnoth (kostenlos) für (Windows, MAC, Linux)
- Microsoft Notepad

## Andere CFG-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.cfg** verwenden.

**Einstellungen**
- [CFG – Celestia-Konfigurationsdatei](/settings/cfg-celestia/)
- [CFG – Citrix Server-Verbindungsdatei](/settings/cfg-citrix/)
- [CFG – MAME-Konfigurationsdatei](/settings/cfg-mame/)
- [CFG – LightWave-Konfigurationsdatei](/settings/cfg-lightwave/)

**Spiel**
- [CFG – Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG – MUGEN-Konfigurationsdatei](/game/cfg-mugen/)
- [CFG – Quell-Engine-Konfigurationsdatei](/game/cfg-sourceengine/)

**System & Sonstiges**
- [CFG – CFG-Datei](/system/cfg/)
- [CFG – Cal3D-Modellkonfigurationsdatei](/misc/cfg-cal3d/)

## Verweise
* [The Battle for Wesnoth](https://en.wikipedia.org/wiki/The_Battle_for_Wesnoth)
