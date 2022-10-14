{
  "date" : "2019-12-12",
  "keywords" :[ "GLTF", "Datei", "Erweiterung", "Format", "3D", "Khronos Group 3D" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Erfahren Sie mehr über GLTF-Dateien und APIs, die GLTF-Dateien erstellen und öffnen können.",
  "title" :"GLTF - GL-Übertragungsdateiformat",
  "linktitle" :"GLTF",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine GLTF-Datei?

glTF (GL Transmission Format) ist ein 3D-Dateiformat, das 3D-Modellinformationen im JSON-Format speichert. Die Verwendung von JSON minimiert sowohl die Größe von 3D-Assets als auch die Laufzeitverarbeitung, die zum Entpacken und Verwenden dieser Assets erforderlich ist. Es wurde für die effiziente Übertragung und das Laden von 3D-Szenen und -Modellen durch Anwendungen übernommen. glTF wurde von der Khronos Group 3D Formats Working Group entwickelt und wird von seinen Erstellern auch als [JPEG](/de/image/jpeg/) von 3D bezeichnet.

Das GLTF-Dateiformat definiert ein erweiterbares, gemeinsames Veröffentlichungsformat für 3D-Content-Tools und -Dienste, das Authoring-Workflows rationalisiert und eine interoperable Nutzung von Inhalten in der gesamten Branche ermöglicht. Die Absicht hinter der Erstellung des glTF-Dateiformats war es, ein erweiterbares, gemeinsames Veröffentlichungsformat für 3D-Content-Tools und -Dienste zu definieren, das Authoring-Workflows rationalisieren und eine interoperable Nutzung von Inhalten in der gesamten Branche ermöglichen sollte. Es minimiert die Laufzeitverarbeitung durch Anwendungen, die WebGL und andere APIs verwenden.

## Kurze Geschichte

Die ersten Spezifikationen für das glTF-Dateiformat 1.0 wurden im Oktober 2015 angekündigt. Dies war eine Reihe von Bemühungen, die im März 2012 von Khronos begannen. Ziel dieser Bemühungen war es, die Möglichkeiten rund um die WebGL-Traktion zu bewerten. Als Ergebnis wurde die erste Demo des glTF-Formats basierend auf dem JSON-Format auf dem WebGl-Meetup 2012 vorgestellt. Das Format wurde von Zeit zu Zeit von mehreren Unternehmen übernommen, darunter Cäsium, 3D Tiles, Oculus, Microsoft, Archilogic und andere.

glTF 2.0 wurde am 5. Juni 2017 auf der Web3D 2017 Conference veröffentlicht. Es gibt eine lange Liste von Unternehmen, die danach das glTF-Dateiformat übernommen haben.

## GLTF-Dateiformat

Die Dateiformatspezifikationen für glTF 2.0 sind [online] (https://github.com/KhronosGroup/glTF/tree/master/specification/2.0) als Referenz verfügbar und sollten in jeder Implementierung im Zusammenhang mit Lesen/Schreiben zur Unterstützung von konsultiert werden glTF-Dateiformat.

glTF definiert Assets als JSON-Dateien mit unterstützenden externen Daten. Es repräsentiert 3D-Modelle mit Hilfe von:

* Vollständige Szenenbeschreibung in einer JSON-formatierten .glTF-Datei, die Informationen über Knotenhierarchie, Materialien, Kameras sowie Deskriptorinformationen für Netze, Animationen und andere Konstrukte enthält
* Binärdateien (.bin), die Geometrie- und Animationsdaten sowie andere pufferbasierte Daten enthalten
* Bilddateien ([.jpg](/de/image/jpeg/), [.png](/de/image/png/)) für Texturen

Alle externen Assets wie Bilder werden in externen Dateien gespeichert, auf die über URI verwiesen wird. Diese URIs werden zusammen mit dem GLB-Container gespeichert oder mithilfe von Daten-URIs direkt in JSON eingebettet. Jede gültige glTF muss ihre Version angeben.

glTF wurde entwickelt, um eine kleine Dateigröße, schnelles Laden, vollständige 3D-Szenendarstellung und Erweiterbarkeit zu erreichen. Diese einzigartigen Designziele sind die Hauptgründe für die Popularität des glTF-Dateiformats im 3D-Bereich. Im Folgenden sind die MIME-Typen aufgeführt, die vom glTF-Dateiformat für verschiedene Dateitypen unterstützt werden:

* .gltf-Dateien verwenden model/gltf+json
* .bin-Dateien verwenden application/octet-stream
* Texturdateien verwenden den offiziellen image/*-Typ basierend auf dem spezifischen Bildformat. Zur Kompatibilität mit modernen Webbrowsern werden die folgenden Bildformate unterstützt: image/jpeg, image/png.

### JSON-Codierung

glTF erlegt dem JSON-Dateiformat die folgenden zusätzlichen Einschränkungen auf

Um die clientseitige Implementierung zu vereinfachen, hat glTF zusätzliche Einschränkungen für das JSON-Format und die Codierung.

1. JSON muss die UTF-8-Codierung ohne BOM verwenden.
1. Alle in dieser Spezifikation definierten Zeichenfolgen (Eigenschaftsnamen, Enums) verwenden nur ASCII-Zeichensätze und müssen als Klartext geschrieben werden, z.
1. Namen (Schlüssel) innerhalb von JSON-Objekten müssen eindeutig sein, dh doppelte Schlüssel sind nicht zulässig.

### URIs

Puffer und Bildressourcen werden über URIs referenziert. Die folgenden beiden URI-Typen müssen von den Clients unterstützt werden.

**Daten-URIs:** Die Daten-URIs entsprechen der Definition von RFC 2397 und werden von glTF verwendet, um Ressourcen in JSON einzubetten.

**Relative URI-Pfade:** oder path-noscheme gemäß RFC 3986, [Section 4.2](https://tools.ietf.org/html/rfc3986#section-4.2) – ohne Schema, Autorität oder Parameter. Reservierte Zeichen müssen gemäß RFC 3986, [Section 2.2](https://tools.ietf.org/html/rfc3986#section-2.2) in Prozent codiert sein.

## Verweise ##

* [glTF 2.0 Spezifikationen – Khronos](https://github.com/KhronosGroup/glTF)
* [glTF-Dateiformat – von Wikipedia](https://en.wikipedia.org/wiki/GlTF)

