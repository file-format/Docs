{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "EMLX - Apple Mail File Format",
  "description":"Learn about EMLX file format and APIs that can create and open EMLX files.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is an EMLX file?

The EMLX file format is implemented and developed by Apple. The Apple Mail application uses the EMLX file format for exporting the emails. There are other applications as well that can open the EMLX files and convert these to other file formats.

## Brief History of EMLX File Format

Mac OS X operating system adopted the existing email program, NeXTMail, created by NeXT as part of the NeXTSTEP operating system. Apple after acquiring NeXT uplifted its features and it became the now Apple Mail email application to be used as default mail client. Emails exported via Apple Mail are directly saved as EMLX files. In addition, it is the default mail client for EMLX files when someone opens these by double-clicking on Mac OS.

## EMLX File Format

EMLx files are simple text based files that can be opened in any text editor like Notepad. The EMLX file structure consists of three parts:

* A byte count for the message - Length of the message itself, written in ASCII in decimal, terminated by 0x0a
* The message itself
* Message Metadata in the form of XML plist

These can be better explained with the help of following sample email extracted from Apple Mail as EMLX and opening in a text editor.

### EMLX Example

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

In this example, the 875 shows the total length of message. The message metadata is enclosed in the <plist> tags and the flags are as described as follow:

|Field|Description|Value
---|---|---|
|0|read|1 << 0
|1|deleted|1 << 1
|2|answered|1 << 2
|3|encrypted|1 << 3
|4|flagged|1 << 4
|5|recent|1 << 5
|6|draft|1 << 6
|7|initial (no longer used)|1 << 7
|8|forwarded|1 << 8
|9|redirected|1 << 9
|10-15|attachment count|3F << 10 (6 bits)
|16-22|priority level|7F << 16 (7 bits)
|23|signed|1 << 23
|24|is junk|1 << 24
|25|is not junk|1 << 25
|26-28|font size delta|7 << 26 (3 bits)
|29|junk mail level recorded|1 << 29
|30|highlight text in toc|1 << 30
|31|(unused)|

## See Also ##

* [EML](/email/eml/)
* [MSG](/email/msg/)
