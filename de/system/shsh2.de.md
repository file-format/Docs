{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHSH2-Datei – iOS SHSH-Blob-Dateiformat",
  "description":"Erfahren Sie, was eine SHSH2-Datei ist.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Was ist eine SHSH2-Datei?

Eine SHSH2-Datei, auch SHSH-Blob oder ECID SHSH genannt, ist eine digitale Signatur, die von Apple zur Authentifizierung und Überprüfung von Firmware-Updates für iOS-Geräte wie iPhones, iPads und iPods verwendet wird. Es enthält eine eindeutige Kennung für das Gerät, die als ECID (Exclusive Chip ID) bekannt ist. Es enthält auch Informationen über die auf dem Gerät installierte Firmware-Version.

## SHSH2-Dateiformat – Weitere Informationen

SHSH2-Dateien werden im Binärdateiformat auf Disc gespeichert und die internen Dateistrukturdetails dieses Dateiformats sind nicht öffentlich verfügbar.

Wenn eine neue Version von iOS auf einem Apple-Gerät wie iPhone, iPad oder Mac installiert wird, wird eine SHSH2-Datei generiert. Diese SHSH2-Datei wird an Apple-Server gesendet, die diese digitale Signaturdatei lesen und überprüfen. Basierend auf diesen Informationen erlaubt oder verhindert der Server die Installation.

Das Gleiche passiert, wenn ein Update angefordert wird. Wenn ein Benutzer über iTunes oder eine andere Software ein Update oder eine Wiederherstellung seines Geräts anfordert, prüfen die Server von Apple, ob die SHSH2-Datei mit der ECID und der Firmware-Version des Geräts übereinstimmt, bevor das Update fortgesetzt werden kann.

## Verweise

* [SHSH Blob – Von Wikipedia](https://en.wikipedia.org/wiki/SHSH_blob)
* [TSS Saver](https://tsssaver.1conan.com/v2/)

