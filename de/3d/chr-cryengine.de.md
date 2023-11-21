{
"Datum": "2023-10-11",
   "keywords":[
"chr",
"chr-Datei",
"Chr Cryengine-Zeichendatei",
"wie öffnet man eine chr-datei",
"Datei",
"chr-Dateierweiterung",
"Verlängerung",
"Datei"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc":true,
"title": "CHR-Dateiformat – CryENGINE-Zeichendatei",
   "description":"Erfahren Sie mehr über das CHR CryENGINE-Zeichendateiformat und die APIs, mit denen CHR-Dateien erstellt und geöffnet werden können.",
"linktitle": "CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine",
"parent": "3d"
}
},
"lastmod": "2023-10-11"
}

## Was ist eine CHR-Datei?

Die CHR-Datei bezieht sich im Kontext von CryENGINE auf eine **CryENGINE-Zeichendatei**. CryENGINE ist eine von Crytek entwickelte Spiel-Engine. Diese Dateien werden zum Speichern von Charaktermodellen und zugehörigen Daten zur Verwendung in Videospielen und anderen Echtzeitanwendungen verwendet.

## CryENGINE-Charakterdatei

Eine CryENGINE-Zeichendatei enthält normalerweise die folgenden Komponenten:

1. **Charaktermodell**: Dies ist ein 3D-Modell des Charakters, einschließlich seiner Geometrie, Texturen und Animationen. Diese Modelle werden oft mit Software wie Autodesk Maya oder Blender erstellt und dann in CryENGINE importiert.
    




















2. **Animationsdaten**: CryENGINE unterstützt komplexe Animationen für Charaktere, daher kann die Datei ".chr" verschiedene Animationen wie Gehen, Laufen, Springen und mehr enthalten. Diese Animationen werden normalerweise als Keyframe-Daten gespeichert.
    




















3. **Rigging-Informationen**: Rigging bezieht sich auf den Prozess der Erstellung einer Skelettstruktur für ein Charaktermodell, die es ermöglicht, Animationen auf das Modell anzuwenden. Die ".chr"-Datei enthält möglicherweise Informationen über die Knochenhierarchie und darüber, wie das Netz des Charakters mit diesem Skelett verbunden ist.
    




















4. **Material- und Texturdaten**: Informationen über die im Charaktermodell verwendeten Materialien und zugehörige Texturkarten können in der ".chr"-Datei enthalten sein. CryENGINE unterstützt physikbasiertes Rendering, sodass diese Materialien sehr detailliert sein können.
    




















5. **Physikdaten**: Wenn der Charakter mit der Spielwelt interagieren soll, kann die Datei ".chr" physikalische Daten wie Kollisionsformen oder Einschränkungen für die Ragdoll-Physik enthalten.
    




















6. **Konfigurationseinstellungen**: Verschiedene Konfigurationseinstellungen im Zusammenhang mit dem Verhalten des Charakters in der Spielwelt, wie z. B. KI-Verhalten oder Skriptereignisse, können ebenfalls Teil der ".chr"-Datei sein.

## CryENGINE

CryENGINE ist eine leistungsstarke Spiele-Engine, die von Crytek, einem deutschen Videospielunternehmen, entwickelt wurde. Es ist für seine hochmodernen Grafikfunktionen bekannt und wurde zur Entwicklung einiger visuell beeindruckender und technologisch fortschrittlicher Videospiele verwendet. Hier sind einige wichtige Funktionen und Informationen zu CryENGINE:

1. **Grafik und Rendering**: CryENGINE ist bekannt für seine fortschrittlichen Grafikfunktionen. Es unterstützt Funktionen wie globale Echtzeitbeleuchtung, hochwertige dynamische Beleuchtung und Schatten, physikalisch basierte Rendering (PBR) und hochauflösende Texturen. Diese Funktionen tragen dazu bei, visuell beeindruckende und realistische Spielwelten zu schaffen.
    




















2. **Physik-Engine**: CryENGINE enthält eine integrierte Physik-Engine, die realistische Interaktionen zwischen Objekten in der Spielwelt ermöglicht. Es unterstützt Funktionen wie Starrkörperphysik, Weichkörperphysik und Ragdoll-Physik und eignet sich daher für die Erstellung dynamischer und immersiver Umgebungen.
    




















3. **Gelände und Vegetation**: CryENGINE bietet Werkzeuge zum Erstellen großer und detaillierter Außenumgebungen. Es unterstützt Geländebearbeitung, Vegetationsplatzierung und dynamische Wettersysteme und ermöglicht es Entwicklern, weitläufige und realistische Außenumgebungen zu erstellen.
    




















4. **Charakteranimation**: CryENGINE enthält robuste Tools für die Charakteranimation. Es unterstützt komplexe Charakter-Rigs, Gesichtsanimationen und ein Blend-Tree-System, das es Entwicklern ermöglicht, lebensechte Charakterbewegungen und Animationen zu erstellen.
    




















5. **KI-System**: Die Engine verfügt über ein KI-System, das die Erstellung intelligenter NPCs (Nicht-Spieler-Charaktere) und feindlicher KI ermöglicht. Entwickler können KI-Verhalten und -Interaktionen skripten, um herausfordernde und immersive Spielerlebnisse zu schaffen.
       





















6. **Skripting**: CryENGINE verwendet eine Skriptsprache namens "Schematyc", die es Entwicklern ermöglicht, Gameplay-Logik und Interaktionen zu erstellen. Darüber hinaus unterstützt es C++ für fortgeschrittenere Programmieranforderungen.

## Von CryENGINE verwendete Dateiformate

Hier sind einige gängige Dateitypen im Zusammenhang mit CryENGINE:

1. **cryproj**: CryENGINE-Projektdateien. In diesen Dateien werden projektspezifische Einstellungen und Konfigurationen für ein bestimmtes Spielprojekt gespeichert.
    




















2. **.level**: Leveldateien enthalten 3D-Spielweltdaten, einschließlich Gelände, Objekte, Beleuchtung und andere levelspezifische Einstellungen. Levels sind ein grundlegender Bestandteil des Spieldesigns in CryENGINE.
    




















3. **.cgf**: Zeichengeometrieformat. Diese Dateien enthalten 3D-Modelldaten für Charaktere, Objekte und andere Spielressourcen. CGF-Dateien können Geometrie-, Texturen- und Animationsdaten enthalten.
    




















4. **.chrparams**: Zeichenparameterdateien. In diesen Dateien werden Einstellungen und Konfigurationen für Charaktermodelle und deren Animationen gespeichert.
    




















5. **.dds**: DirectX-Texturformat. CryENGINE verwendet üblicherweise DDS-Dateien zum Speichern von Texturen, einschließlich Diffus-Maps, Normal-Maps und anderen Texturtypen.
    




















6. **.cryshader**: CryENGINE-Shader-Dateien. Diese Dateien definieren, wie Materialien und Objekte in der Spielwelt gerendert werden, indem sie Shader, Materialeigenschaften und mehr angeben.
    




















7. **.crytif**: Texturinformationsdatei. Diese Dateien speichern zusätzliche Informationen zu Texturen, wie z. B. Komprimierungseinstellungen, Mipmaps und andere texturbezogene Details.
    




















8. **.cdf**: Zeichendefinitionsdatei. CDF-Dateien werden verwendet, um Charakter-Assets und ihre Eigenschaften zu definieren, einschließlich Anhängen, Animationszuständen und charakterbezogenen Einstellungen.
    




















9. **.dds**: CryENGINE verwendet auch DDS-Dateien (DirectDraw Surface) für verschiedene Textur-Maps, wie z. B. Normal-Maps, Specular-Maps und Diffus-Maps.
    




















10. **.anim**: Animationsdateien. Diese Dateien speichern Animationsdaten für Charaktere und Objekte, einschließlich Keyframes, Knochenpositionen und Animationssequenzen.
    




















11. **.xml**: XML-Dateien können für verschiedene Konfigurationen und Datendefinitionen innerhalb von CryENGINE verwendet werden, wie z. B. Spiellogik, KI-Verhalten und mehr.
    




















12. **.pak**: [PAK-Dateien](/game/pak/) sind Archivdateien, die zum Packen von Spielressourcen und -ressourcen verwendet werden, um die Verteilung und das Laden des Spiels effizienter zu gestalten.

## Wie öffne ich eine CHR-Datei?

Zu den Programmen, die CHR-Dateien öffnen, gehören:

- **Crytek CryENGINE SDK** (kostenlose Testversion) für Windows

**SubType:** 3D-Bilddateien

## Andere CHR-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.chr** verwenden.

**3D**
- [CHR – CryENGINE-Charakterdatei](/3d/chr-cryengine/)
- [CHR – 3ds Max-Zeichendatei](/3d/chr-3ds/)

**Schriftart und Spiel**
- [CHR – Borland-Zeichensatz](/font/chr/)
- [CHR - Doki Doki Literature Club! Charakterdatei](/game/chr-doki/)

## Verweise
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

