{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Torrent-Dateiformat - BitTorrent-Datei",
  "description":"Erfahren Sie mehr über TORRENT-Dateien und APIs, die TORRENT-Dateien erstellen und öffnen können.",
  "linktitle" :"Torrent",
  "menu" : {
    "docs" : {
"identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## Was ist eine TORRENT-Datei?

Eine TORRENT-Datei ist eine Textdatei, die von BitTorrent und anderen P2P-Programmen (Peer-to-Peer) zum Herunterladen und Austauschen von Inhalten verwendet wird. Die herunterladbaren Inhalte können Dokumente, Videos, Spiele, Filme und andere im Internet verfügbare Medien umfassen. Es enthält Metadateninformationen über Inhalt und Speicherort der herunterzuladenden Medien. Software wie BitTorrent verwendet Informationen aus dieser Datei wie Name, Dateigröße und Ordnerstruktur zum Herunterladen von Daten. Torrent-Dateien können online in andere Dateiformate wie [PDF](/de/pdf/) konvertiert werden.

## Was ist Torrenting? Das TORRENT-Dateiformat für den Datenaustausch

Torrenting ist das Konzept des Austauschs (Herunter- und Hochladen) von Datendateien über das BitTorrent-Netzwerk. Im Gegensatz zu herkömmlichen Servern, auf denen Daten hochgeladen werden, damit andere darauf zugreifen und sie herunterladen können, werden Torrent-Dateien abgerufen und über das Torrent-Netzwerk gesendet. Wenn ein Benutzer eine .torrent-Datei in Anwendungen wie BitTorrent öffnet, beginnt die Software damit, den Inhalt der Datei bitweise herunterzuladen. Wenn mehrere Benutzer dieselbe Datei haben, teilt BitTorrent die Downloads unter allen Benutzern auf, um den Downloadvorgang zu beschleunigen. Gleichzeitig wird der Computer des Benutzers, der die Datei herunterlädt, auch zur Quelle der Datei, um sie an andere Benutzer zu senden, die ebenfalls dieselbe Datei herunterladen.

### Struktur einer TORRENT-Datei

Eine Torrent-Datei ist eine Kombination aus einer Liste von Dateien und Metadateninformationen zu allen herunterzuladenden Teilen der Datei. Es enthält die folgenden Informationen in Form von Schlüsseln.

- `announce` — Die URL des Trackers, die anderen Peers bekannt gegeben wird, um sie über die Verfügbarkeit der Datei zu informieren
- `info` — Dies wird einem Wörterbuch zugeordnet, dessen Schlüssel davon abhängen, ob eine oder mehrere Dateien geteilt werden:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — Größe der Datei in Byte.
- `path` — eine Liste von Strings, die Unterverzeichnisnamen entsprechen, wobei der letzte der eigentliche Dateiname ist
- `length` — die Größe der Datei in Bytes (nur wenn eine Datei geteilt wird)
- `name` — Dateiname, wo die Datei gespeichert werden soll
- `piece length` — Anzahl der Bytes pro Stück. Dies ist üblicherweise 28 KiB = 256 KiB = 262.144 B.
- `pieces` — eine Hash-Liste, die eine Verkettung des SHA-1-Hash jedes Stücks ist.

## Ist Torrenting sicher und legal?

Das Torrenting-Protokoll für den Datenaustausch zwischen P2P-Benutzern ist sicher, da es nur das Mittel zum Teilen jeder Art von Datei ist. Somit ist das Protokoll selbst nicht unsicher oder illegal. Die über das Netzwerk geteilten Inhalte können jedoch Dateien oder Medien enthalten, die den rechtlichen Status der geteilten Dokumente verletzen können. In einem solchen Fall kann der Austausch solcher Daten rechtliche Schritte gegen die Parteien nach sich ziehen, die an der öffentlichen Weitergabe solcher Dateien beteiligt sind.

## Verweise

* [TORRENT-Datei - Wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

