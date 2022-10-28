{
  "date" : "2021-03-30",
  "keywords" :[ "PMLZ", "Zipped Palm Markup Language File", "extension", "File", "format", "eBook", "Palm Markup Language" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Erfahren Sie mehr über das PMLZ-Dateiformat, die Palm Markup Language und APIs, die PMLZ-Dateien erstellen und öffnen können.",
  "title" :"PMLZ - Gezippte Palm Markup Language-Datei",
  "linktitle" : "PMLZ",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-30"
}

## Was ist eine PMLZ-Datei?

Palm Inc hat einen eBook-Dateityp eingeführt; bekannt als das PMLZ-Dateiformat, das eine komprimierte Version des Dateiformats [PML](/de/ebook/pml/) ist, weshalb die Dateien mit der Erweiterung .pmlz als **Zipped Palm Markup Language File** bekannt sind. Die PMLZ-Datei ist nur ein Zip-Container einer Datei, die [PDB](/de/ebook/pdb/)-Dateien kompiliert, um Dokumente für **eReader** zu erstellen (bekannt als E-Book-Lesegerät wie ein Tablet-Computer). Die PML-Datei übergibt das Layout an eine PDB-Datei (die verschiedene Datendateien enthält), um sie auf einem Palm-Gerät anzuzeigen. Dagegen ist eine PDB-Datei eine Datenbankdatei, die von verschiedenen Anwendungen verwendet wird, darunter Quicken, Pegasus, Microsoft Visual Studio und Palm Pilot. Kurz gesagt, ein PMLZ ist ein komprimierter Container mit PML- und PDB-Dateien.


## Kenntnisse über Palm Markup Language
Die folgende Tabelle gibt die PML-Befehle an:

|Befehl|Beschreibung|
---|---|
| \p | Neue Seite |
| \ x | Neues Kapitel; verursacht auch einen neuen Seitenumbruch. Schließen Sie den Kapiteltitel (und alle Stilcodes) mit \x und \x | ein
| \Xn | Neues Kapitel, eingerückt um n Stufen (n zwischen 0 und 4 einschließlich) im Kapiteldialog; verursacht keinen Seitenumbruch. Schließen Sie den Kapiteltitel (und alle Stilcodes) mit \Xn und \Xn | ein
| \Cn="Kapiteltitel" | Fügen Sie "Kapiteltitel" in die Kapitelliste ein, mit Ebene n (wie \Xn). Der Text wird nicht auf der Seite angezeigt und erzwingt keinen Seitenumbruch. Dies kann manchmal nützlich sein, um zum Beispiel eine Kapitelmarkierung am Anfang einer Einführung in das Kapitel einzufügen. |
| \c | Zentrieren Sie diesen Textblock; schließen mit \c am Zeilenanfang |
| \r | Textblock rechts ausrichten; schließen mit \r am Anfang der Zeile |
| \i | Block kursiv; schließen mit \i |
| \u | Block unterstreichen; schließen mit \u |
| \o | Overstrike-Block; schließen mit \o |
| \v | Unsichtbarer Text; schließen mit \v (kann für Kommentare verwendet werden) |
| \t | Block einrücken. Am Zeilenanfang beginnen, am Zeilenende | mit \t schließen
| \T="50%" | Rückt den angegebenen Prozentsatz der Bildschirmbreite ein, in diesem Fall 50 %. Wenn die aktuelle Zeichnungsposition bereits hinter der angegebenen Bildschirmposition liegt, wird dieses Tag ignoriert. |
| \w="50%" | Betten Sie eine horizontale Linie mit einer bestimmten prozentualen Breite des Bildschirms ein, in diesem Fall 50 %. Dieses Tag bewirkt einen Zeilenumbruch davor und danach. Die Regel ist zentriert. Das Prozentzeichen ist obligatorisch. |
| \n | Wechseln Sie zur "normalen" Schriftart, die vom Benutzer | vorgegeben wird
| \s | Wechseln Sie zu stdFont; Schließen Sie mit \s, um zur normalen Schriftart zurückzukehren |
| \b | Wechseln Sie zu boldFont; Schließen Sie mit \b, um zur normalen Schriftart zurückzukehren (veraltet; verwenden Sie stattdessen \B) |
| \l | Wechseln Sie zu largeFont; Schließen Sie mit \l, um zur normalen Schriftart zurückzukehren |
| \B | Text als fett markieren. Im Gegensatz zum Tag \b ändert \B die Schriftart nicht, sodass Sie großen fetten Text verwenden können. Sie können \b und \B nicht in derselben PML-Datei mischen. |
| \Sp | Text als hochgestellt markieren. Sollte nicht mit anderen Stilen wie Fett, Kursiv etc. gemischt werden. Hochgestellten Text mit \Sp einschließen. |
| \Sb | Text als Tiefstellung markieren. Sollte nicht mit anderen Stilen wie Fett, Kursiv usw. gemischt werden. Schließen Sie tiefgestellten Text mit \Sb ein. |
| \k | Setzen Sie eingeschlossenen Text in Kapitälchen um; schließen mit \k. Alle Zeichen, die in \k-Tags eingeschlossen sind (einschließlich derjenigen mit Akzenten), werden in Großbuchstaben umgewandelt und mit einer kleineren Punktgröße als ein normaler Großbuchstabe gerendert. |
| \\ | Stellt einen einzelnen Backslash | dar
| \aXXX | Fügen Sie ein Nicht-ASCII-Zeichen ein, dessen Windows-1252-Code dezimal XXX ist. Einzelheiten finden Sie in der PML-Zeichentabelle. |
| \UXXXX | Fügen Sie ein Nicht-ASCII-Zeichen ein, dessen Unicode-Code hexadezimal XXXX ist. Einzelheiten finden Sie in der erweiterten PML-Zeichentabelle. |
| \m="Bildname.png" | Fügen Sie das benannte Bild ein. Siehe den Abschnitt über Bilder unten. |
| \q="#linkanchor"Etwas Text\q | Verweisen Sie auf einen Link-Anker, der sich an einer anderen Stelle im Dokument befindet. Die Zeichenfolge nach der Ankerspezifikation und vor dem nachgestellten \q wird unterstrichen oder anderweitig als Link angezeigt, wenn das Dokument angezeigt wird. |
| \Q="linkanchor" | Geben Sie im Dokument einen Linkanker an. |
| \- | Fügen Sie einen weichen Bindestrich ein. Ein weicher Bindestrich wird nur angezeigt, wenn es notwendig ist, ein Wort über eine Zeile hinweg zu trennen. |
| \Fn="footnote1"1\Fn | Verknüpfen Sie die „1“ mit einer Fußnote mit dem Namen footnote1, die am Ende des PML-Dokuments markiert ist. Siehe den Abschnitt über Fußnoten und Seitenleisten weiter unten. |
| \Sd="sidebar1"Seitenleiste\Sd | Verknüpfen Sie den „Sidebar“-Text mit einer Seitenleiste mit dem Namen sidebar1, die am Ende des PML-Dokuments getaggt ist. Siehe den Abschnitt über Fußnoten und Seitenleisten weiter unten. |
| \Ich | Als Referenzindexelement markieren. Schließen Sie das Indexelement (und alle Stilcodes) mit \I und \I.| ein


## Verweise

* [Palm Markup Language – von MobileRead](https://wiki.mobileread.com/wiki/EReader)
* [E-Reader – Von MobileRead](https://en.wikipedia.org/wiki/E-Reader)

