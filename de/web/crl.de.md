{
  "date" : "2022-09-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CRL-Datei - Zertifikatssperrliste",
  "description":"Erfahren Sie mehr über das CRL-Dateiformat und APIs, die CRL-Dateien erstellen und öffnen können.",
  "linktitle" :"CRL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-09-01"
}

## Was ist eine CRL-Datei?

Eine CRL-Datei (Certificate Revocation List) ist eine schwarze Liste digitaler X.509-Zertifikate, die von einer Zertifizierungsstelle (CA) vor dem ihnen zugewiesenen Widerrufsdatum widerrufen werden. Es enthält Informationen über die Ausgabe und das Widerrufsdatum, mit denen die Sicherheitsadministratoren betroffene digitale Zertifikate sperren können. CRL enthält keine abgelaufenen Zertifikate, da ihr Hauptzweck darin besteht, über nicht vertrauenswürdige und ungültige Zertifikate zu informieren.

Zu den Anwendungen, die CRL-Dateien öffnen können, gehören OpenSSL, Microsoft IIS Server und Citrix NetScaler.

## CRL-Dateiformat – Weitere Informationen

CRL-Dateien enthalten Informationen im X.509-Standard, der auch seine Semantik für die gemeinsame Nutzung öffentlicher Schlüsselinformationen definiert. Andere in einer CRL-Datei enthaltene Informationen können das Zeitlimit, für das die Zertifikate gesperrt wurden, den Grund für die Sperrung, die Seriennummer des gesperrten Zertifikats und den Zeitstempel umfassen.


### Die wichtigsten Gründe dafür, dass Zertifikate zu CRL hinzugefügt werden

Es kann mehrere Gründe dafür geben, dass das Zertifikat Ihrer Website widerrufen und zur CRL hinzugefügt wird. Einige von ihnen könnten sein;

1. Der private Schlüssel Ihres Zertifikats wurde kompromittiert
1. Ihr Zertifikat ist ungültig oder wurde von der Zertifizierungsstelle falsch ausgestellt
1. Mit dem Zertifikat verbundene Organisationsdetails werden geändert und CA stellt ein neues Zertifikat aus
1. Jeder andere unvermeidbare Grund, aus dem das Zertifikat widerrufen wurde

## Verweise

* [National Institute of Standards and Technology (NIST)](https://csrc.nist.gov/glossary/term/CRL)
* [RFC 5280 der Internet Engineering Task Force (IETF)](https://tools.ietf.org/html/rfc5280)
* [Zertifikatswiderrufsliste](https://en.wikipedia.org/wiki/Certificate_revocation_list)

