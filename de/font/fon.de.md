{
  "date" : "2020-08-20",
  "keywords" :[ "Fon-Datei", "Fon-Dateiformat", "Was ist eine Fon-Datei", "Datei", "Fon-Beispiel", "Fon-Dateierweiterung", "Erweiterung", "Format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"FON - Schriftbibliotheksdatei",
  "description":"Erfahren Sie mehr über das FON-Dateiformat und APIs, die FON-Dateien erstellen und öffnen können.",
  "linktitle" :"FON",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-30"
}

## Was ist eine FON-Datei?

Eine Datei mit der Erweiterung .fon ist eine Microsoft Windows 3.x-Schriftbibliothek, die eigentlich eine ausführbare Datei ist, aber in .fon umbenannt wurde. Es ist eine Sammlung von [.fnt](/de/font/fnt/)-Dateien an sich und Anwendungen referenzieren sie beim Zugriff auf Systemschriftarten. Aus diesem Grund fungiert es als Ressourcendatei. Es kann unter Windows OS mit der Anwendung Microsoft Windows Font View geöffnet werden.

## FON-Dateiformat

Eine FON-Datei enthält Font-Ressourcen und hat das Dateiformat Resource (.res). Das .res-Dateiformat gibt den Dateiheader sowie Datenabschnittsspezifikationen an. Eine .fnt-Datei ist auch eine Ressourcendatendatei, die in einer Ressourcendatei enthalten ist. FON-Dateien haben ein binäres Dateiformat und einen Anwendungs-/Oktettstrom-MIME-Typ.

Schriftartressourcen werden im Gegensatz zu anderen Arten von Ressourcen nicht zu den Ressourcen einer Anwendung hinzugefügt. Stattdessen werden sie den EXE-Dateien hinzugefügt und in .fon-Dateien umbenannt, was zu Bibliotheksdateien anstelle von Anwendungen führt. Mehrere einzelne Schriftarten bilden Komponenten einer Schriftartgruppe, wobei jede Gruppe einer Ressourcengruppenstruktur folgt. Schriftartressourcen verwenden diese Ressourcengruppenstrukturen. Der Gruppenkopf enthält alle Informationen, die für den Zugriff auf eine bestimmte Schriftart aus der Gruppe erforderlich sind. Eine Schriftartkomponentenressource hat das folgende Format.
```
    [Normal resource header (type = 8)]

    [Complete contents of the .FNT file follow as the resource body (see [.fnt](/de/font/fnt/) file)
```
Eine einzelne .rc-Ressourcendatei kann gemischte Ressourcendeklarationen haben. Schriftgruppen können sich an beliebiger Stelle in der Ressourcendatei befinden und müssen nicht zusammenhängend sein. Programme, die .RES-Dateien erstellen, müssen den manuellen Eintrag von FONTDIR hinzufügen. Es folgt die Struktur des Gruppenkopfs.

```
[Normaler Ressourcenheader (Typ = 7)]

WORD NumberOfFonts; // Gesamtzahl in der .RES-Datei
```     
The remaining data is repeated for every font in the .RES file.

```
WORD fontOrdinal;
struct FontDirEntry {
WORD dfVersion;
DWORD dfGröße;
char dfCopyright[60];
WORT dfTyp;
WORT dfPunkte;
WORD dfVertRes;
WORD dfHorizRes;
WORD dfAscent;
WORD dfInternalLeading;
WORD dfExternalLeading;
BYTE dfKursiv;
BYTE dfUnderline;
BYTE dfStrikeOut;
WORT dfGewicht;
BYTE dfCharSet;
WORD dfPixWidth;
WORD dfPixHeight;
BYTE dfPitchAndFamily;
WORD dfAvgWidth;
WORT dfMaxWidth;
BYTE dfFirstChar;
BYTE dfLastChar;
BYTE dfDefaultChar;
BYTE dfBreakChar;
WORT dfWidthBytes;
DWORD dfDevice;
DWORD dfFace;
DWORD dfReserviert;
char szGerätename[];
char szFaceName [];
};
```

## References

 * [Font File Format](https://jeffpar.github.io/kbarchive/kb/065/Q65123/)

