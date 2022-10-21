{
  "date" : "2021-07-13",
  "keywords" :[ "CER", "Erweiterung", "Datei", "Format", "Web", "Zertifikat", "Sprache" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CER - Zertifikatsdateiformat",
  "description":"Erfahren Sie mehr über das CER-Dateiformat und APIs, die CER-Dateien erstellen und öffnen können.",
  "linktitle" :"CER",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## Was ist eine CER-Datei? ##

Eine Datei mit der Erweiterung .cer ist dafür verantwortlich, einige Informationen über das Eigentümerzertifikat und den spezifischen öffentlichen Schlüssel zu speichern. Dieses Dateiformat kann die privaten Schlüssel nicht speichern und kann nur ein x509-Zertifikat speichern. Die speziell gesicherten Zertifizierungsstellen sind diejenigen, die zu HTTPS gehören, einem vertrauenswürdigen und gesicherten Protokoll zum Surfen
Das CER ist ein Zertifikat Ihres Servers. Es wird normalerweise von der Zertifizierungsstelle für die Domäne empfangen. CER wird meistens als dasselbe wie [CRT](/de/web/crt/) angesehen, obwohl beide das gleiche Format von SSL-Zertifikaten haben, aber unterschiedliche Dateinamenerweiterungen haben.
Diese können auf Betriebssystemen verwendet werden, indem Sie einfach einen Browser öffnen und die Sicherheit des verwendeten Browsers oder der verwendeten Website überprüfen.

## Kurze Geschichte ##

1995 wurde Thawte die erste Zertifizierungsstelle, die das Problem öffentlicher SSL-Zertifikate (Secured Socket Link) außerhalb der USA löste. Danach gibt es eine Reihe solcher Behörden, die von 1995 bis 2020 gegründet wurden.

## CER-Dateiformat ##

Diese Dateien können einfach sein
* Die PKC S#7 umfasst die Base64-ASCII-Codierung
* Die Dateierweiterungen sind p7b oder p7cZ
* Für binäre Inhalte wäre das Zertifikat DER oder pkcs12/pfx.
Es gibt viele Arten von Zertifikatsdateien mit einigen einzigartigen Spezifikationen:
* .pem, Wenn eine Organisation die Verkettung dieses Formats verwendet, ist es bekannt, Zertifikate zu erstellen
* .arm, wenn die Methode zum Extrahieren einer selbstsignierten Zertifizierung unterstützt wird, ist das angegebene Format für diesen Zweck .arm. Es wird in Base-64-ASCII-Codierung dargestellt.
* .der, Es besteht aus binären Daten. Dies bedeutet, dass es nur für ein einzelnes Zertifikat verwendet werden kann
* .pfx (PKC512), besteht aus einem privaten Schlüssel, der einem von der Zertifizierungsstelle ausgestellten Zertifikat oder einem selbstsignierten Zertifikat entspricht. Dieses Format ist bekannt für die Konvertierung einer SSL-Implementierung in die andere.


