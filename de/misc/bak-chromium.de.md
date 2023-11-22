{
"Datum": "12.06.2023",
  "keywords": [
"bak",
"bak-Datei",
"BAK Chromium Lesezeichen",
"Was ist eine Bak-Datei",
"Wie öffnet man eine Bak-Datei",
"Datei",
"bak-Dateierweiterung",
"Verlängerung"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "BAK-Dateiformat – Chromium-Lesezeichen-Backup",
  "description":"Erfahren Sie mehr über das BAK Chromium Bookmarks-Format und die APIs, mit denen BAK-Dateien erstellt und geöffnet werden können.",
"linktitle": "BAK Chromium-Lesezeichen",
  "menu": {
    "docs": {
      "identifier": "misc-bak-chromium",
"parent": "misc"
}
},
"lastmod": "12.06.2023"
}

## Was ist eine BAK-Datei?

Eine .bak-Datei im Kontext von Chromium-basierten Webbrowsern wie Google Chrome und Microsoft Edge ist im Wesentlichen eine Sicherungsdatei Ihrer Lesezeichen. Diese Lesezeichen werden als reine Textliste gespeichert und das verwendete Dateiformat ist JSON. Der Zweck dieser .bak-Dateien besteht darin, Ihre Lesezeichen zu schützen, indem sie eine Sicherungskopie bereitstellen, die im Falle einer versehentlichen Löschung oder eines Verlusts wiederhergestellt werden kann.

Chromium-basierte Browser, einschließlich Google Chrome, erstellen diese Sicherungsdateien routinemäßig und geben ihnen normalerweise den Namen "Bookmarks.bak". Sie sind im Wesentlichen eine Momentaufnahme Ihrer Lesezeichen zu einem bestimmten Zeitpunkt.

## So verwenden Sie eine .bak-Datei zum Wiederherstellen Ihrer Lesezeichen

1. **Suchen Sie die Sicherungsdatei:** Sie befindet sich normalerweise in einem bestimmten Ordner, der mit Ihrem Chromium-Profil verknüpft ist. Der genaue Speicherort kann je nach Betriebssystem variieren.

Unter Windows: Suchen Sie in "C:\Benutzer\"<YourUsername> \AppData\Local\Chromium\User Data\Default\Bookmarks.bak`.

Unter macOS: Suchen Sie in "~/Library/Application Support/Chromium/Default/Bookmarks.bak".

Unter Linux: Überprüfen Sie "~/.config/chromium/Default/Bookmarks.bak".

3. Stellen Sie sicher, dass Ihr Chromium-Browser geschlossen ist.
4. Benennen Sie die Datei "Bookmarks.bak" um, indem Sie die Erweiterung ".bak" entfernen, sodass sie einfach "Bookmarks" heißt.
5. Starten Sie Chromium.

Durch Umbenennen der .bak-Datei in "Lesezeichen" verwendet Chromium sie als aktuelle Lesezeichendatei und Ihre vorherigen Lesezeichen sollten wiederhergestellt werden.

## Chromium-Lesezeichen-Backup

Das Sichern Ihrer Chromium-Lesezeichen ist eine kluge Vorsichtsmaßnahme, um sicherzustellen, dass Sie Ihre wichtigen gespeicherten Webseiten und URLs nicht verlieren. Chromium ist ein Open-Source-Browser, der als Basis für andere Browser wie Google Chrome und Microsoft Edge dient. Um Ihre Chromium-Lesezeichen zu sichern, gehen Sie folgendermaßen vor:

## Methode 1: Manuelles Backup

1. **Chromium öffnen**: Starten Sie den Chromium-Browser auf Ihrem Computer.

2. **Auf Lesezeichen zugreifen**: Klicken Sie auf die drei vertikalen Punkte (Menüsymbol) in der oberen rechten Ecke des Browserfensters. Bewegen Sie den Mauszeiger im Dropdown-Menü über "Lesezeichen", um das Untermenü "Lesezeichen" anzuzeigen.

3. **Lesezeichen exportieren**: Klicken Sie im Lesezeichen-Untermenü auf "Lesezeichen-Manager". Dadurch wird eine neue Registerkarte geöffnet, in der Ihre Lesezeichen angezeigt werden.

4. **Lesezeichen exportieren**: Klicken Sie im Lesezeichen-Manager-Tab erneut auf die drei vertikalen Punkte (normalerweise in der oberen rechten Ecke), um das Lesezeichen-Manager-Menü zu öffnen. Wählen Sie in diesem Menü "Lesezeichen exportieren".

5. **Speicherort wählen**: Wählen Sie aus, wo Sie die exportierte Lesezeichendatei auf Ihrem Computer speichern möchten. Der Standarddateiname lautet "bookmarks.html", Sie können ihn jedoch bei Bedarf ändern. Speichern Sie es an einem Ort, der Ihnen in Erinnerung bleibt.

6. **Speichern**: Klicken Sie auf die Schaltfläche "Speichern" oder "Exportieren", um Ihre Lesezeichen als HTML-Datei zu speichern.

Ihre Lesezeichen wurden nun als HTML-Datei gesichert. Sie können diese Datei zur sicheren Aufbewahrung auf ein externes Laufwerk oder einen Cloud-Speicher kopieren.

## Methode 2: Mit Google-Konto synchronisieren (falls zutreffend)

Wenn Sie in Chromium bei einem Google-Konto angemeldet sind, können Sie auch die integrierte Synchronisierungsfunktion verwenden, um Ihre Lesezeichen sicher und geräteübergreifend zu synchronisieren. Auf diese Weise werden Ihre Lesezeichen automatisch in Ihrem Google-Konto gesichert.

1. **Chromium öffnen**: Starten Sie den Chromium-Browser und stellen Sie sicher, dass Sie bei Ihrem Google-Konto angemeldet sind.

2. **Synchronisierung aktivieren**: Klicken Sie auf die drei vertikalen Punkte (Menüsymbol) in der oberen rechten Ecke des Browserfensters und gehen Sie zu "Einstellungen".

3. **Synchronisierung und Google-Dienste**: Klicken Sie im Tab "Einstellungen" in der linken Seitenleiste auf "Synchronisierung und Google-Dienste".

4. **Synchronisieren Sie Ihre Daten**: Stellen Sie unter "Synchronisieren" sicher, dass "Lesezeichen" aktiviert ist. Dadurch werden Ihre Lesezeichen mit Ihrem Google-Konto synchronisiert.

Ihre Lesezeichen werden nun automatisch gesichert und mit Ihrem Google-Konto synchronisiert. Sie können darauf zugreifen, indem Sie sich auf einem beliebigen Gerät mit Chromium oder einem anderen Browser, der die Google-Synchronisierung unterstützt, bei Ihrem Google-Konto anmelden.

Denken Sie daran, Ihre Lesezeichen regelmäßig auch manuell zu sichern, insbesondere wenn Sie eine lokale Kopie wünschen, die nicht ausschließlich auf die Synchronisierung Ihres Google-Kontos angewiesen ist.

## So öffnen Sie eine BAK-Datei

Wenn Sie die Rohdaten Ihrer Lesezeichensicherung untersuchen möchten, können Sie die Datei "Bookmarks.bak" mit verschiedenen Texteditoren wie Microsoft Visual Studio Code (auf mehreren Plattformen verfügbar), Microsoft Notepad (für Windows-Benutzer) und Apple TextEdit öffnen (für Mac-Benutzer) oder einen anderen Texteditor Ihrer Wahl. Dadurch können Sie die in der Datei enthaltenen Lesezeichen und Metadaten anzeigen.

Sie können die Datei "Bookmarks.bak" öffnen und ihren Inhalt mit verschiedenen Textbearbeitungsprogrammen und Code-Editoren anzeigen. Hier sind einige häufig verwendete Optionen:

1. Visual Studio-Code (VS-Code)
2. Notizblock (Windows)
3. TextEdit (Mac)
4. Erhabener Text
5. Notepad++
6. Atom
7. Nano und Vim (Linux)
8. WordPad (Windows)

## Andere BAK-Dateien

Hier sind andere Dateitypen, die die Dateierweiterung **.bak** verwenden.

**Datenbank**
- [BAK – Datenbanksicherungsdatei](/database/bak/)
- [BAK – Swiftpage Act! Datenbanksicherung](/database/bak-act/)
- [BAK – Microsoft SQL Server-Datenbanksicherung](/database/bak-sqlserver/)

**Spiel**
- [BAK – Terraria World oder Player Backup](/game/bak-terraria/)

**Verschiedenes**
- [BAK – Sicherungsdatei](/misc/bak-backup/)
- [BAK – Finale 2012 Score Backup](/misc/bak-finale/)
- [BAK – MobileTrans Backup](/misc/bak-mobiletrans/)
- [BAK – VEGAS Videoprojekt-Backup](/misc/bak-vegas/)

**Einstellungen**
- [BAK – Holo Launcher Backup](/settings/bak-holo/)

## Verweise
* [Chromium Bookmarks](https://www.chromium.org/user-experience/bookmarks/)
