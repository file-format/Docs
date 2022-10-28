{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PDF/UA-Dateiformat",
  "description":"Erfahren Sie mehr über das PDF/UA-Dateiformat und APIs, die PDF/UA-Dateien erstellen und öffnen können.",
  "linktitle" : "UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# Was ist eine PDF/UA-Datei? #

PDF/UA wurde im August 2012 als [ISO-Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) veröffentlicht und ist bei weitem die erste vollständige Definition eines Anforderungskatalogs für allgemein zugängliche PDF-Dokumente. Der Begriff „allgemein zugänglich“ bezieht sich auf das Verständnis, dass die in einem [PDF](/de/pdf/)-Dokument enthaltenen Informationen für jeden im Allgemeinen und für Menschen mit Behinderungen im Besonderen gleichermaßen und unabhängig zugänglich sein sollten. Die Einführung des PDF/UA-Standards kann als wichtiger Schritt zur Erstellung von Tools und Anwendungen zum Erstellen und Lesen von PDF-Inhalten angesehen werden.

## Anforderungen an das Dateiformat ##

PDF/UA hat einige bestimmte Anforderungen an seiner Basis, die als Essenz dieses Standards dienen. Diese basieren im Wesentlichen auf dem Tagging von PDFs, was bedeutet, dass alle PDF/UA-Dokumente ordnungsgemäß mit Tags versehen sein müssen. Außerdem müssen die Tags semantisch angemessen und in logischer Reihenfolge sein. Dadurch wird sichergestellt, dass das mit PDF/UA-Spezifikation erstellte Enddokument zuverlässiger und zugänglicher ist. Dies kann PDF-Autoren in Frage stellen, ob sie alles über all diese Anforderungen wissen müssen? Glücklicherweise ist es nicht so, da die PDF/UA-Konformitätstools die Verantwortung für das Hinzufügen und Bewahren der Barrierefreiheit des PDFs übernehmen.

Die Anforderungen an das Dateiformat für PDF/UA lauten wie folgt.

* Inhalt wird auf zwei Arten kategorisiert: sinnvoller Inhalt und Artefakte wie z. B. dekorative Seitenelemente. Alle sinnvollen Inhalte müssen getaggt und in den Strukturbaum aller Tags innerhalb eines Dokuments integriert werden. Artefakte hingegen brauchen nur als solche gekennzeichnet zu werden.
* Sinnvolle Inhalte müssen mit Tags gekennzeichnet sein und zusammen mit den anderen Tags im Dokument einen vollständigen Strukturbaum bilden.
* Sinnvolle Inhalte müssen mit den entsprechenden semantischen Tags gekennzeichnet werden.
* Der durch die Dokument-Tags erstellte Strukturbaum muss die logische Lesereihenfolge des Dokuments widerspiegeln.
* Es dürfen nur die in PDF 1.7 definierten Standard-Tags verwendet werden; Wenn andere Tags verwendet werden, muss in einem Rollenzuweisungseintrag festgehalten werden, welches Standard-Tag jeweils repräsentiert wird.
* Informationen dürfen nicht ausschließlich visuell vermittelt werden (z. B. Kontrast, Farbe oder Position auf der Seite).
* Flackernde, blinkende oder blinkende Inhalte sind nicht gestattet, weder als von JavaScript gesteuerte Effekte noch als Teil von Videos, die in das PDF eingebettet sind.
* Ein Dokumenttitel muss angegeben werden, und das Dokument muss so eingerichtet werden, dass der Titel (und nicht der Dateiname) im Fenstertitel erscheint.
* Die Sprache aller Inhalte ist zu beachten, Sprachänderungen müssen ausdrücklich als solche gekennzeichnet werden.

## PDF/UA-Konformität ##

Der PDF/UA-Standard definiert Spezifikationen für Inhalte, Lesegeräte und unterstützende Technologien. Diese drei Aspekte werden anhand der Inhalte des Dokuments miteinander verknüpft. Die Konformitätsanforderungen für diese sind unten aufgeführt.

## Konforme Dateien ##

Dateien, die dem PDF/UA-Standard entsprechen, sollten Funktionen enthalten, die gemäß den [PDF 1.7-Spezifikationen] (http://www.adobe.com/go/pdfreference) gültig sind. Allerdings sollten Features ausgeschlossen werden, die PDF/UA ausdrücklich verbietet.

## Konforme Lesegeräte ##

Ein konformes Lesegerät muss die Regeln der PDF 1.7-Spezifikationen befolgen. Konkret soll es unterstützen:

* alle Tags, Attribute und Schlüsselwerte, die für die Zugänglichkeit angegeben sind. Es sollte auch in der Lage sein, digitale Signaturen, Anmerkungen und optionale Inhalte zu verarbeiten und darzustellen.
* Verarbeitung und Darstellung digitaler Signaturen, Anmerkungen und optionaler Inhalte
* Navigieren Sie auf verschiedene Weise durch das Dokument

## Konforme Hilfstechnologie ##

Zur Unterstützung der PDF/UA-Features ist eine konforme Hilfstechnologie zwingend erforderlich. Diese beinhalten beispielsweise Eigenschaften des Inhalts und des Readers und sollten eine Navigation über Seitenbeschriftungen, Dokumentstruktur oder Gliederung ermöglichen. Es sollte dem Benutzer auch ermöglichen, den Standard-Navigationszoom zu überschreiben.

## Verweise ##

* [PDF/UA - Von Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA in Kürze](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

