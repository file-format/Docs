{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das PYC-Dateiformat und APIs, die PYC-Dateien erstellen und öffnen können.",
  "title" :"PYC-Dateiformat - Python-kompilierte Datei",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## Was ist eine PYC-Datei?

Eine PYC-Datei ist eine kompilierte Ausgabedatei, die aus Quellcode generiert wird, der in der Programmiersprache Python geschrieben ist. Wenn die PY-Datei mit dem Python-Interpreter ausgeführt wird, wird sie zur Ausführung in Bytecode konvertiert. Gleichzeitig wird der kompilierte Bytecode auch als .pyc-Datei gespeichert, um ihn gegebenenfalls zu einem späteren Zeitpunkt aus dem Cache wiederzuverwenden.

## Struktur des PYC-Dateiformats

PYC-Dateien sind im Bytecode und ihre Dateiformatspezifikationen sind nicht öffentlich verfügbar. Untersuchungen einiger Quellen zeigen jedoch, dass die [Struktur einer PYC-Datei](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) besteht aus:

* „Eine magische Vier-Byte-Zahl“ – Einfach zwei Bytes, die sich bei jeder Änderung des Marshalling-Codes ändern, und dann zwei Bytes von 0d0a.
* „Ein Vier-Byte-Änderungszeitstempel“ – Unix-Änderungszeitstempel der Quelldatei, die die .pyc-Datei generiert hat, damit sie neu kompiliert werden kann, wenn sich die Quelle ändert.
* „Ein gemarshalltes Codeobjekt“ – die Ausgabe von marshal.dump des Codeobjekts, das ein Ergebnis der Kompilierung der Quelldatei ist.

## Verweise

* [Die Struktur von .pyc-Dateien](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)

