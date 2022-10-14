{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "Datei", "Erweiterung", "Dateiformat", "Programmiersprache Rust", "Programmierhandbuch", "RS-Beispiel", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Rust-Programmierdatei",
  "description":"Erfahren Sie mehr über das RS-Dateiformat und APIs, die RS-Dateien erstellen und öffnen können.",
  "linktitle" :"RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## Was ist eine RS-Datei?

Eine Datei mit der RS-Erweiterung gehört zur Programmiersprache Rust, es handelt sich um eine universelle Programmiersprache auf hoher Ebene, die für Leistung und Sicherheit entwickelt wurde, insbesondere für sicheres Verhalten. Rust ist syntaktisch ähnlich zu С++, kann aber die Speichersicherheit garantieren, indem es einen Ausleihprüfer verwendet, um Referenzen zu validieren. Die Rust-Sprache bietet Speichersicherheit ohne Müllsammlung, und die Referenzzählung ist optional.

## RS-Dateiformat ##

Rust wurde ursprünglich von Graydon Hoare bei Mozilla Research entworfen, mit Beiträgen von Dave Herman, Brendân Eich und anderen. Es wird zunehmend in der Industrie eingesetzt, und Microsoft hat mit der Sprache für sichere und sicherheitskritische Softwarekomponenten experimentiert.

Rust wurde seit 2016 jedes Jahr in der Stасk Оverflow Develорer Survey zur „beliebtesten Programmiersprache“ gewählt, obwohl es in der Umfrage von 2021 nur von 7 % der Befragten verwendet wurde. Zusammen mit herkömmlicher statischer Typisierung unterstützte Rust vor Version 0.4 auch Tyrestates.

Das Typensystem hat Behauptungen vor und nach Programmaussagen durch die Verwendung einer speziellen Prüfaussage modelliert. Diskrepanzen können eher zur gleichen Zeit als zur Laufzeit entdeckt werden, wie es bei Behauptungen im С- oder С++-Code der Fall sein könnte. Das Typestatement-Konzept war nicht nur Rust vorbehalten, da es zuerst in der Sprache NIL eingeführt wurde. Typstates wurden entfernt, weil sie in der Praxis wenig verwendet wurden, obwohl die gleiche Funktionalität erreicht werden kann, indem man Rusts Move-Semantik nutzt.

Die Rust-Programmiersprache hilft Ihnen, schnellere und zuverlässigere Software zu schreiben. Ergonomie auf hohem Niveau und Steuerung auf niedrigem Niveau stehen oft im Widerspruch zum Design der Programmiersprache; Rost fordert diesen Konflikt heraus. Durch das Ausbalancieren von leistungsstarker technischer Kompetenz und einer großartigen Entwicklererfahrung gibt Ihnen Rust die Möglichkeit, Low-Level-Details (wie z.

 

## Kurze Geschichte ##

Die Sprache entstand aus einem persönlichen Projekt, das 2006 von Mozilla-Mitarbeiter Graydon Hore begonnen wurde, der erklärte, dass das Projekt möglicherweise nach der Familie der Rostpilze benannt wurde. Mozilla begann das Projekt 2009 zu sponsern und kündigte es 2010 an. Rust 1.0, die erste stabile Veröffentlichung, wurde am 15. Mai 2015 veröffentlicht Releases, dann mit Beta-Releases getestet, die sechs Wochen dauern. Am 6. April 2021 kündigte Google die Unterstützung für Rust in Android Open Source als Alternative zu С/С++ an.

## Technische Spezifikation ##

Rust soll eine Sprache für hochgradig übereinstimmende und hochsichere Systeme und die Programmierung im Großen sein, das heißt, das Erstellen und Aufrechterhalten von Grenzen, die die Integrität großer Systeme bewahren. Dies hat zu einem Feature-Set mit Schwerpunkt auf Sicherheit, Kontrolle des Speicherlayouts und Übereinstimmung geführt.


Die Rust-Sprache ist so konzipiert, dass sie speichersicher ist. Nullzeiger, baumelnde Zeiger oder Datenrennen sind nicht zulässig. Datenwerte können nur über einen festen Satz von Formularen initialisiert werden, die alle erfordern, dass ihre Eingaben bereits initialisiert sind. Um Zeiger zu replizieren, die entweder gültig oder NULL sind, wie z. B. in verknüpften Listen oder binären Baumdatenstrukturen, bietet die Rust-Core-Bibliothek einen Optionstyp. Rust hat eine Syntax hinzugefügt, um Lebensdauern zu verwalten. Unsicherer Code kann einige dieser Einschränkungen mit dem unsicheren Schlüsselwort untergraben.


Die Rust-Sprache verwendet keine automatische Garbage Collection. Speicher und andere Ressourcen werden durch die Ressourcenerfassung verwaltet, die eine Initialisierungskonvention mit optionaler Referenzzählung ist.


Rust bietet eine deterministische Ressourcenverwaltung mit sehr geringem Overhead. Rust bevorzugt die Stapelzuweisung von Werten und führt kein implizites Boxen durch. Es gibt das Konzept der Referenzen (unter Verwendung des Symbols), das keine Referenzzählung zur Laufzeit beinhaltet. Die Sicherheit solcher Zeiger wird gleichzeitig überprüft, wodurch baumelnde Zeiger und andere Formen undefinierten Verhaltens verhindert werden.


Rust hat ein Eigentümersystem, bei dem alle Werte einen eindeutigen Eigentümer haben. Werte können durch unveränderliche Referenzen mit &T, durch veränderliche Referenzen mit & mut T oder nach Werten mit T übergeben werden. Der Rust Compiler erzwingt diese Regeln zur Kompilierzeit und prüft auch, ob alle Referenzen gültig sind.


## Beispiel für ein RS-Dateiformat ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Bezug ##

* [RS - von Wikipedia](https://en.wikipedia.org/wiki/Rust_(programming_language))



