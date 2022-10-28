{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP-Datei - LaTeX MetaPost-Datei",
  "description":"Erfahren Sie mehr über das MP-Dateiformat und APIs, die MP-Dateien erstellen und öffnen können.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
"identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Was ist eine MP-Datei?

Eine MP-Datei ist eine Vektorbilddatei, die von der MetaPost-Programmiersprache generiert wird, um Bilder zu erstellen. Im MP-Dateiformat erstellte Vektorbilder werden als [EPS](/de/image/eps/)-Dateien (Encapsulated PostScript) gespeichert. Darüber hinaus wird MetaPost mit TeX- und Metafont-Frameworks ausgeliefert, und MP-Dateien können aus den TEX- und LTX-Dateien generiert werden, die von diesen Anwendungen verwendet werden. MP-Dateien enthalten Zeichnungsanweisungen und mathematische algorithmische Zeichnungen zum Rendern der EPS-Ausgabedatei. Die PDFTex-Engine kann das erstellte EPS verwenden, um [PDF](/de/pdf/)-Dateien direkt zu generieren.

## MP-Dateiformat

MP-Dateien werden als Binärdateien auf Disc gespeichert und erzeugen eine EPS-Ausgabe, wenn sie in das Ausgabe-Vektorbild-Dateiformat exportiert werden. Mit MetaPost erstellte Zeichnungen werden in formatierter Form in mit LaTex erstellte technische Dokumente und Zeitschriftenveröffentlichungen eingebunden.

### MetaPost MP-Dateibeispiel

Es folgt ein Beispiel, auf das von [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost) verwiesen wird, das einen Pfeil und den Buchstaben „A“ direkt über der Mitte des enthält Pfeil.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Verweise ##

* [MetaPost von Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Latex-Beispiel Metapost von Berkeley Educational Wiki] (https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

