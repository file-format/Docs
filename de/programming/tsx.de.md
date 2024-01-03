{
  "date" : "2023-12-28",
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TSX-Datei – React TypeScript-Datei – Was ist eine .tsx-Datei und wie öffnet man sie?",
  "description":"Erfahren Sie mehr über die TSX React TypeScript-Datei und wie Sie sie öffnen.",
  "linktitle" : "TSX",
  "menu" : {
    "docs" : {
      "identifier": "programming-de-tsx",
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-12-28"
}

## Was ist eine TSX-Datei?

Die Dateierweiterung „.tsx“ wird häufig mit TypeScript-Dateien verknüpft, die **React**-Code enthalten. **TypeScript ist eine Obermenge von JavaScript**, die der Sprache statische Typisierung hinzufügt, und **React ist eine JavaScript-Bibliothek zum Erstellen von Benutzeroberflächen**. Wenn Entwickler gemeinsam mit React und TypeScript arbeiten, verwenden sie häufig die Erweiterung „.tsx“ für ihre Dateien, um anzugeben, dass sie sowohl TypeScript als auch JSX (Reacts Syntaxerweiterung für JavaScript) enthalten.

## TSX-Dateibeispiel

Mit TypeScript können Sie Typen für Ihre Variablen, Funktionsparameter und mehr definieren. TypeScript-Code wird häufig in einer „.tsx“-Datei angezeigt, in der die Arten von Requisiten, Zuständen und anderen Variablen angegeben werden, die in React-Komponenten verwendet werden.

„
// Beispiel: TypeScript-Code in einer React-Komponente
Schnittstelle MyComponentProps {
   Name: Zeichenfolge;
   Alter: Anzahl;
}
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
   // Komponentenlogik hier
   return <div>{name} ist {age} Jahre alt.</div>;
};
„

## JSX (React-Syntax-Erweiterung)

JSX ist eine von React empfohlene Syntaxerweiterung für JavaScript. Es ähnelt XML/HTML und wird verwendet, um zu beschreiben, wie die Benutzeroberfläche aussehen soll.

„
// Beispiel: JSX in einer React-Komponente
const MyComponent: React.FC<MyComponentProps> = ({ name, age }) => {
   return <div>{name} ist {age} Jahre alt.</div>;
};
„

Die „.tsx“-Datei enthält normalerweise die Definition einer React-Komponente unter Verwendung von Funktionskomponenten oder Klassenkomponenten.

„
// Beispiel: Komponentendefinition in einer „.tsx“-Datei reagieren
const MyComponent: React.FC = () => {
   return <div>Hallo, Reagiere!</div>;
};
„

Am Anfang der Datei werden häufig Importanweisungen angezeigt, die die erforderlichen Abhängigkeiten und Module einbinden.

„
// Beispiel: Anweisungen in eine „.tsx“-Datei importieren
import React aus 'react';
„

## Wie öffne ich eine TSX-Datei?

TSX-Dateien sind reine Textdateien, sodass Sie sie in jedem Texteditor öffnen können, z. B. Notizblock. Dabei handelt es sich jedoch um Codierungsdateien, die von der IDE geöffnet werden sollen, z. B. Visual Studio-Code.