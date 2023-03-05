{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Apple Mail-Dateiformat",
  "description":"Erfahren Sie mehr über das EMLX-Dateiformat und APIs, die EMLX-Dateien erstellen und öffnen können.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Was ist eine EMLX-Datei?

Das EMLX-Dateiformat wird von Apple implementiert und entwickelt. Die Apple Mail-Anwendung verwendet das EMLX-Dateiformat zum Exportieren der E-Mails. Es gibt auch andere Anwendungen, die die EMLX-Dateien öffnen und diese in andere Dateiformate konvertieren können.

## Kurze Geschichte des EMLX-Dateiformats

Das Mac OS X-Betriebssystem übernahm das vorhandene E-Mail-Programm NeXTMail, das von NeXT als Teil des NeXTSTEP-Betriebssystems erstellt wurde. Apple hat nach der Übernahme von NeXT seine Funktionen verbessert und es wurde die jetzt Apple Mail-E-Mail-Anwendung, die als Standard-E-Mail-Client verwendet werden kann. Über Apple Mail exportierte E-Mails werden direkt als EMLX-Dateien gespeichert. Darüber hinaus ist es der Standard-E-Mail-Client für EMLX-Dateien, wenn jemand diese per Doppelklick auf Mac OS öffnet.

## EMLX-Dateiformat

EMLx-Dateien sind einfache textbasierte Dateien, die in jedem Texteditor wie Notepad geöffnet werden können. Die EMLX-Dateistruktur besteht aus drei Teilen:

* Eine Byteanzahl für die Nachricht - Länge der Nachricht selbst, in ASCII dezimal geschrieben, mit 0x0a abgeschlossen
* Die Nachricht selbst
* Nachrichten-Metadaten in Form von XML-Plist

Diese lassen sich besser mit Hilfe der folgenden Beispiel-E-Mail erklären, die aus Apple Mail als EMLX extrahiert und in einem Texteditor geöffnet wird.

### EMLX-Beispiel

```
875       
X-Spam-Checker-Version: SpamAssassin 3.3.2 (2011-06-06) on ******.*********.***
X-Spam-Level:
X-Spam-Status: No, score#-3.2 required#4.2 tests#BAYES_00,RP_MATCHES_RCVD,
        SPF_PASS,TVD_SPACE_RATIO autolearn#ham version#3.3.2
Received: from [127.0.0.1](******.*********.*** [***.**.**.**])
        by ******.*********.*** (8.14.5/8.14.5) with ESMTP id r2TN8m4U099571
        for <****@*********.***>; Fri, 29 Mar 2013 19:08:48 -0400 (EDT)
        (envelope-from ****@*********.***)
Subject: very simple
From: Sender <****@*********.***>
Content-Type: text/plain; charset#us-ascii
Message-Id: <4E83618E-BB56-404F-8595-87352648ADC7@*********.***>
Date: Fri, 29 Mar 2013 19:09:06 -0400
To: Reciever <****@*********.***>
Content-Transfer-Encoding: 7bit
Mime-Version: 1.0 (Apple Message framework v1283)
X-Mailer: Apple Mail (2.1283)

message Foo
--
Sender
http://www.la-grange.net/karl/

<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version#"1.0">
<dict>
        <key>date-sent</key>
        <real>1364598546</real>
        <key>flags</key>
        <integer>8590195713</integer>
        <key>original-mailbox</key>
        <string>imap://********@127.0.0.1:11143/mail/2013/03</string>
        <key>remote-id</key>
        <string>41147</string>
        <key>subject</key>
        <string>very simple</string>
</dict>
</plist>
```

In diesem Beispiel zeigt 875 die Gesamtlänge der Nachricht an. Die Metadaten der Nachricht sind in der enthalten<plist> Tags und die Flags sind wie folgt beschrieben:

|Feld|Beschreibung|Wert
---|---|---|
|0|lesen|1 << 0
|1|gelöscht|1 << 1
|2|beantwortet|1 << 2
|3|verschlüsselt|1 << 3
|4|markiert|1 << 4
|5|neueste|1 << 5
|6|Entwurf|1 << 6
|7|anfänglich (nicht mehr verwendet)|1 << 7
|8|weitergeleitet|1 << 8
|9|umgeleitet|1 << 9
|10-15|Anhanganzahl|3F << 10 (6 Bits)
|16-22|Prioritätsstufe|7F << 16 (7 Bit)
|23|signiert|1 << 23
|24|ist Schrott|1 << 24
|25|ist kein Müll|1 << 25
|26-28|Schriftgrößen-Delta|7 << 26 (3 Bit)
|29|Junk-Mail-Level aufgezeichnet|1 << 29
|30|Text in toc hervorheben|1 << 30
|31|(unbenutzt)|

## Siehe auch ##

* [EML](/de/email/eml/)
* [MSG](/de/email/msg/)

