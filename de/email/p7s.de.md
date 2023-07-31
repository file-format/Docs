{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S-Datei - Digital signierte E-Mail-Nachricht",
  "description":"Erfahren Sie mehr über das P7S-Dateiformat und APIs, die P7S-Dateien erstellen und öffnen können.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## Was ist eine P7S-Datei?

Eine P7S-Datei ist eine digitale Signatur, die mit einer digital signierten E-Mail empfangen wird. Das Vorhandensein dieser Datei als Anhang der E-Mail bestätigt, dass die E-Mail von einer authentischen Quelle stammt. Dadurch wird sichergestellt, dass der Absender ein E-Mail-Signaturzertifikat auf seinem Computer installiert hat. Wenn eine solche signierte E-Mail vom Computer des Benutzers gesendet wird, wird die P7S-Datei angehängt, die den Namen des Absenders enthält. E-Mail-Clients, die signierte E-Mails unterstützen, können die Informationen des Absenders sehen.

## P7S-Dateiformat – Weitere Informationen

S/MIME (Secure/Multipurpose Internet Mail Extensions) P7S-Dateien enthalten die Informationen im Nur-Text-Format, das für Menschen lesbar ist. E-Mail-Clients wie Microsoft Outlook, Apple Mail und Mozilla Thunderbird unterstützen das Lesen der digital signierten Informationen aus einer S/MIME-E-Mail. Durch das Signieren einer E-Mail wird die Identität des Absenders überprüft und dem Empfänger mitgeteilt, dass die Nachricht authentisch ist. Wenn E-Mails von E-Mail-Clients heruntergeladen werden (entweder als [EML](/de/email/eml/) oder [MSG](/de/email/msg/)), werden diese P7S-Dateien an diese E-Mails angehängt gefunden.

Eine P7S-Datei enthält die folgenden Informationen:

* Herkunftsquelle der E-Mail
* Datum und Uhrzeit des Versands,
* Ob es während der Übertragung geändert wurde

Diese Informationen werden mithilfe der Public-Key Cryptography Standard #7 (PKCS7)-Technologie eingebettet, um die verschlüsselten Signaturen digital an die E-Mail anzuhängen.

## Verweise ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

