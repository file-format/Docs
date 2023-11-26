{
"Datum": "2023-10-11",
   "keywords":[
"Shader",
"Shader-Datei",
"Shader Quake 3 Engine Shader-Datei",
"So öffnen Sie eine Shader-Datei",
"Datei",
"Shader-Dateierweiterung",
"Verlängerung",
"Datei"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title": "SHADER-Dateiformat – Quake 3 Engine Shader-Datei",
   "description":"Erfahren Sie mehr über das Shader-Dateiformat und die APIs von SHADER Quake 3 Engine, mit denen SHADER-Dateien erstellt und geöffnet werden können.",
"linktitle": "SHADER Quake",
   "menu":{
      "docs":{
         "identifier":"game-shader-quake",
"parent": "game"
}
},
"lastmod": "2023-10-11"
}

## Was ist eine SHADER-Datei?

Das SHADER-Dateiformat wird in der **Quake 3-Engine** verwendet, um Shader für Texturen und Materialien im Spiel zu definieren. Shader werden verwendet, um anzugeben, wie eine Oberfläche gerendert werden soll, einschließlich ihres Aussehens, ihres Reflexionsvermögens, ihrer Transparenz und anderer visueller Eigenschaften.

## Quake 3 Engine SHADER-Datei

Hier ist ein grundlegender Überblick über die Struktur und Syntax der Quake 3-Engine-Shader-Datei:

```Plain Text
// Comments can be added with double slashes

// A shader is defined with "shader" keyword followed by shader name
shader shader_name
{
    // Properties and stages of shader are defined within curly braces

    // The properties for this shader are specified using key-value pairs
    // Common properties include surfaceparm, cull, deformvertexes, q3map_*, etc.

    // Example properties:
    surfaceparm nolightmap
    cull disable

    // Stages of shader are defined using stage keyword
    stage
    {
        // The properties for this stage are also specified using key-value pairs

        // Example stage properties:
        texture texture_filename
        // texture is used to specify image file for this stage

        // Additional properties for this stage can include blending modes,
        // scrolling, scaling and other texture manipulation settings.
        // These can be specified with key-value pairs.

        // Example stage properties:
        blendFunc GL_DST_COLOR GL_SRC_COLOR
        // Specifies a blending mode

        tcMod scroll 0.1 0.1
        // Scrolls texture in S and T direction

        tcMod scale 2 2
        // Scales texture

        // You can have multiple stages within a shader, each with its own properties
    }
}
```

In der Shader-Datei der Quake 3-Engine können Sie mehrere Shader definieren, jeder mit seinen eigenen Eigenschaften und Stufen. Diese Shader werden verwendet, um das Erscheinungsbild verschiedener Texturen und Materialien in der Spielwelt zu definieren. Die Engine verwendet diese Informationen, um Oberflächen mit bestimmten visuellen Effekten und Verhaltensweisen zu rendern.

Shader-Dateien in der Quake 3-Engine sind einfache Textdateien, die Anweisungen dazu enthalten, wie Texturen und Materialien im Spiel angezeigt werden sollen. Diese Dateien können mit einem normalen Texteditor geöffnet und bearbeitet werden und befinden sich normalerweise im Verzeichnis **"/scripts"** im .PK3-Paket des Spiels.

## Quake 3-Engine

Die Quake 3-Engine ist eine äußerst einflussreiche und vielseitige Spiel-Engine, die von id Software entwickelt wurde. Es wurde erstmals mit der Veröffentlichung des Spiels "Quake III Arena" im Jahr 1999 eingeführt und wurde seitdem in verschiedenen anderen Spielen verwendet. Die Engine ist für ihre fortschrittliche Grafik, Multiplayer-Fähigkeiten und Modifizierbarkeit bekannt.

Hier sind einige wichtige Funktionen und Aspekte der Quake 3-Engine:

1. **Grafik-Engine:** Die Quake 3-Engine war seinerzeit für ihre hochmoderne Grafiktechnologie bekannt. Es führte erweiterte Funktionen wie gekrümmte Oberflächen, Shader und dynamische Beleuchtung ein, die Ende der 1990er Jahre bahnbrechend waren.
    





2. **Multiplayer-Fokus:** Quake 3 Arena wurde in erster Linie als Multiplayer-Ego-Shooter konzipiert. Der Netzwerkcode der Engine und die Unterstützung für Online-Multiplayer-Spiele waren außergewöhnlich, was sie zu einer beliebten Wahl für kompetitives Online-Spielen machte.
    





3. **Modifizierbarkeit:** Die Quake 3-Engine ist für ihre Modifizierbarkeit bekannt. id Software hat den Engine-Quellcode unter der Open-Source-GNU General Public License (GPL) veröffentlicht. Dies förderte die Erstellung zahlreicher Mods und benutzerdefinierter Karten und führte zu einer lebendigen Modding-Community.
    





4. **Skriptbasiertes Gameplay:** Die Engine verwendete ein skriptbasiertes System zur Definition von Spielregeln und -verhalten, was es Moddern und Mappern relativ einfach macht, benutzerdefinierte Spielmodi und einzigartige Erlebnisse zu erstellen.
    





5. **Unterstützung für benutzerdefinierte Inhalte:** Die Engine von Quake 3 unterstützte benutzerdefinierte Inhalte, einschließlich Texturen, Modelle und Sounddateien, was ein hohes Maß an Anpassung in vom Benutzer erstellten Karten und Mods ermöglichte.
    





6. **Leveldesign:** Die Engine nutzte ein pinselbasiertes Leveldesignsystem, bei dem Karten durch das Herausschneiden von Räumen aus festen Pinseln erstellt wurden. Dieser Ansatz war gut dokumentiert und für Leveldesigner benutzerfreundlich.


Im Laufe der Jahre wurde die Quake 3-Engine als Grundlage für viele andere Spiele und Mods verwendet, darunter unter anderem "Return to Castle Wolfenstein", "Star Wars Jedi Knight II: Jedi Outcast" und "Urban Terror". Es hat ein bleibendes Erbe in der Welt der Spieleentwicklung hinterlassen und das Ego-Shooter-Genre mitgeprägt. Während inzwischen neuere und fortschrittlichere Engines auf den Markt gekommen sind, wird die Quake 3-Engine weiterhin für ihren Beitrag zur Spielebranche geschätzt.

## Wie öffne ich eine SHADER-Datei?

Zu den Programmen, die SHADER-Dateien öffnen oder darauf verweisen, gehören:

- **id Software Quake 3** (kostenpflichtig) für (Windows, Mac, Linux)
- Microsoft Notepad
- Notepad++
- Jeder Texteditor

## Andere SHADER-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.shader** verwenden.

**Spieldateien**
- [SHADER – Godot Engine Shader-Datei](/game/shader-godot/)
- [SHADER – Quake 3 Engine Shader-Datei](/game/shader-quake/)
- [SHADER – Unity Shader Asset](/game/shader-unity/)

## Verweise
- [id Tech 3](https://en.wikipedia.org/wiki/Id_Tech_3)

