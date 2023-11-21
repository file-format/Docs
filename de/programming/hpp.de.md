{
"Datum": "08.06.2023",
  "keywords": [
"hpp-Datei",
"Was ist eine HPP-Datei",
"Was enthält die HPP-Datei",
"HPP-Dateibeispiel",
"Was ist das Format der HPP-Datei?",
"Datei",
"hpp-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "HPP-Dateiformat – C++-Header-Datei",
  "description":"Erfahren Sie mehr über das HPP-Format und APIs, mit denen HPP-Dateien erstellt und geöffnet werden können.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
"parent": "Programmierung"
}
},
"lastmod": "08.06.2023"
}

## Was ist eine HPP-Datei?

Das Dateiformat ".hpp" wird häufig für Header-Dateien in der Programmiersprache C++ verwendet. Header-Dateien enthalten typischerweise Deklarationen und Definitionen von Funktionen, Klassen, Variablen und Konstanten, die von anderen Quellcodedateien in C++-Projekten verwendet werden.

Der Zweck der Verwendung von Header-Dateien besteht darin, eine Möglichkeit bereitzustellen, gemeinsamen Code über mehrere Quellcodedateien hinweg zu teilen, ohne den Code selbst zu duplizieren. Wenn die C++-Quelldatei auf Deklarationen oder Definitionen aus der Header-Datei zugreifen muss, schließt sie die Header-Datei mithilfe der Präprozessoranweisung "#include" ein.

Die Dateierweiterung ".hpp" wird häufig verwendet, um anzuzeigen, dass es sich bei einer Datei um eine C++-Headerdatei handelt. Es ist nicht erforderlich, diese spezielle Erweiterung für Header-Dateien zu verwenden. Möglicherweise stoßen Sie auch auf Header-Dateien mit ".h" oder anderen Erweiterungen. Die Wahl der Erweiterung hängt größtenteils von Konventionen und persönlichen Vorlieben ab.

Wenn eine C++-Quelldatei eine Header-Datei mit "#include" einschließt, kombiniert der Compiler effektiv den Inhalt der Header-Datei mit der Quelldatei, bevor er ihn als Einheit kompiliert. Dadurch kann die Quelldatei auf Deklarationen und Definitionen in der Header-Datei zugreifen und dem Compiler die erforderlichen Informationen zur Typprüfung und Codegenerierung bereitstellen.

## Was enthält die HPP-Datei?

Hier sind einige allgemeine Inhalte, die Sie möglicherweise in der Datei ".hpp" finden:

- **Funktionsdeklarationen:** Header-Dateien enthalten häufig Funktionsdeklarationen ohne deren tatsächliche Implementierungen. Diese Deklarationen stellen Informationen über den Namen, den Rückgabetyp und die Parameter der Funktion bereit, sodass andere Quellcodedateien die Funktion verwenden können, ohne Implementierungsdetails kennen zu müssen.
- **Klassendeklarationen:** Header-Dateien können Klassendeklarationen enthalten, einschließlich Klassennamen, Mitgliedsvariablen, Mitgliedsfunktionen und Zugriffsspezifizierern. Durch die Aufnahme der Klassendeklaration in die Header-Datei können andere Quellcodedateien Objekte dieser Klasse erstellen und auf ihre Mitglieder zugreifen.
- **Konstantendeklarationen:** Header-Dateien können Konstanten definieren, z. B. globale Variablen oder Aufzählungswerte, die für die gemeinsame Nutzung durch mehrere Quellcodedateien gedacht sind. Auf diese Konstanten kann zugegriffen werden, indem die Header-Datei in andere Quelldateien eingebunden wird, sodass diese die definierten Konstanten verwenden können.
- **Typdefinitionen:** Header-Dateien können Typdefinitionen mit dem Schlüsselwort "typedef" oder Typaliase mit dem Schlüsselwort "using" enthalten. Diese Definitionen erstellen neue Namen für vorhandene Typen und machen den Code dadurch lesbarer und wartbarer.
- **Inline-Funktionsdefinitionen:** In einigen Fällen können Header-Dateien Inline-Funktionsdefinitionen enthalten. Inline-Funktionen sind kleine Funktionen, die vor Ort erweitert werden, anstatt als separate Funktion aufgerufen zu werden. Durch das Einfügen einer Inline-Funktionsdefinition in die Header-Datei kann der Compiler den Funktionsaufruf direkt durch den Funktionskörper ersetzen, was möglicherweise die Leistung verbessert.

## Beispiel für eine HPP-Datei

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Was ist das Format der HPP-Datei?

HPP ist eine reine Textdatei, folgt jedoch den allgemeinen Regeln und der Syntax der Programmiersprache C++. Hier ist eine Aufschlüsselung des allgemeinen Formats und der Struktur der ".hpp"-Datei:

- **Header-Schutz:** Typischerweise beginnt eine ".hpp"-Datei mit Header-Schutz, um mehrere Einschlüsse derselben Datei zu verhindern. Dies wird durch Präprozessordirektiven wie "#ifndef", "#define" und "#endif" erreicht. Der Header-Guard stellt sicher, dass der Inhalt der Datei während des Kompilierungsprozesses nur einmal einbezogen wird.
- **Include-Anweisungen:** Nach Header-Guards können Sie andere erforderliche Header-Dateien mit der Anweisung "#include" einschließen. Dazu können Standardbibliotheksheader oder andere benutzerdefinierte Header gehören, die für Ihren Code erforderlich sind.
- **Deklarationen und Definitionen:** Der Hauptinhalt der Datei ".hpp" sind die Deklarationen und in einigen Fällen Definitionen von Klassen, Funktionen, Konstanten, Typaliasen und anderen Elementen. Beispielsweise können Sie Klassen mit dem Schlüsselwort "class", Funktionen mit ihrem Rückgabetyp, Namen und Parameterliste und Konstanten mit dem Schlüsselwort "const", gefolgt von ihrem Typ und Namen, deklarieren.
- **Inline-Funktionsdefinitionen:** In bestimmten Fällen können Sie Inline-Funktionsdefinitionen direkt in die Datei ".hpp" einfügen. Inline-Funktionen werden normalerweise im Klassenkörper definiert, was bedeutet, dass die Funktionsdefinition zusammen mit ihrer Deklaration enthalten ist. Dies kann erreicht werden, indem der Funktionsdefinition das Schlüsselwort "inline" vorangestellt wird.
- **Namespace-Deklarationen:** Wenn Sie Namespaces in Ihrem Code verwenden, können Sie diese in der Datei ".hpp" deklarieren. Dies geschieht mit dem Schlüsselwort "namespace", gefolgt vom Namespace-Namen und dem Einschließen des relevanten Codes in den Namespace-Block.

## Verweise
* [Header-Dateien (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

