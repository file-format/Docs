{
  "date" : "2022-06-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NPK-Dateiformat",
  "description":"Erfahren Sie mehr über das NPK-Dateiformat und APIs, die NPK-Dateien erstellen und öffnen können.",
  "linktitle" : "NPK",
  "menu" : {
    "docs" : {
"identifier":"compression-npk",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-21"
}

## Was ist eine NPK-Datei?

Eine NPK-Datei ist eine Software-Upgrade-Paketdatei, die von **MikroTik**-Routern zum Upgrade des Router-Betriebssystems verwendet wird. Es kommt als komprimiertes Binärarchiv, das in den Router geladen wird, um Software-Updates zu installieren. Zu den in NPK-Dateien enthaltenen Informationen gehören Netzwerkinformationen wie IP-Adresse und IP-Dienst, Verbindungsinformationen (Ethernet-Schnittstellen und serieller Port), E-Mail-Setup, Bridge-Konfiguration und lokale Benutzerverwaltung.

## NPK-Dateiformat

NPK-Dateien werden als komprimiertes Binärarchiv gespeichert. Es ist ein geschlossenes Dateiformat, das nur von MikroTik selbst verwendet wird. Es ist nicht beabsichtigt, RouterOS-Add-Ons über Drittanbieter zu erstellen. NPK-Dateien werden von MikroTik selbst verwaltet und aktualisierte Versionen derselben können von den Download-Bereichen der [MikroTik](https://mikrotik.com/download)-Website heruntergeladen werden.

Wenn eine NPK-Datei auf einen Router hochgeladen wird, tritt das Betriebssystem des Routers erst in Kraft, wenn es neu gestartet wird. Daher ist ein Neustart erforderlich, damit das Betriebssystem des Routers aktualisiert werden kann.

## Verweise

* [MikroTik - Aktualisieren des Router-Betriebssystems](https://mikrotik.com/download)
* [So erstellen Sie NPK-Dateien](https://forum.mikrotik.com/viewtopic.php?t=87126)

