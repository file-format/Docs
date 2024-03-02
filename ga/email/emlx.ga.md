{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMLX - Formáid Comhaid Apple Mail",
  "description": "Foghlaim faoi fhormáid comhaid EMLX agus APIs ar féidir leo comhaid EMLX a chruthú agus a oscailt.",
  "linktitle": "EMLX",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-eml-gax"
}
},
  "lastmod": "2019-09-10"
}

## Cad is comhad EMLX ann?

Tá formáid comhaid EMLX curtha i bhfeidhm agus forbartha ag Apple. Úsáideann feidhmchlár Apple Mail formáid comhaid EMLX chun na ríomhphoist a onnmhairiú. Tá feidhmchláir eile ann freisin ar féidir leo na comhaid EMLX a oscailt agus iad seo a thiontú go formáidí comhaid eile.

## Stair Achomair ar Formáid Chomhaid EMLX

Ghlac córas oibriúcháin Mac OS X leis an gclár ríomhphoist reatha, NeXTMail, cruthaithe ag NeXT mar chuid de chóras oibriúcháin NeXTSTEP. D'ardaigh Apple tar éis dó Next a fháil a ghnéithe agus ba é an feidhmchlár ríomhphoist Apple Mail anois é le húsáid mar chliant ríomhphoist réamhshocraithe. Déantar ríomhphoist a onnmhairítear trí Apple Mail a shábháil go díreach mar chomhaid EMLX. Ina theannta sin, is é an cliant ríomhphoist réamhshocraithe do chomhaid EMLX nuair a osclaíonn duine iad seo trí chliceáil faoi dhó ar Mac OS.

## Formáid Chomhaid EMLX

Is comhaid téacs-bhunaithe simplí iad comhaid EMLx is féidir a oscailt in aon eagarthóir téacs ar nós Notepad. Tá trí chuid i struchtúr comhaid EMLX:

* Comhaireamh beart don teachtaireacht - Fad na teachtaireachta féin, scríofa in ASCII mar dheachúil, arna críochnú ag 0x0a

* An teachtaireacht féin

* Meiteashonraí Teachtaireachta i bhfoirm plist XML


Is féidir iad seo a mhíniú níos fearr le cabhair ó ríomhphost samplach a bhaintear as Apple Mail mar EMLX agus a oscailt in eagarthóir téacs a leanúint.

### Sampla EMLX

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

Sa sampla seo, taispeánann an 875 fad iomlán na teachtaireachta. Tá meiteashonraí na teachtaireachta faoi iamh sa<plist> tá cur síos ar na clibeanna agus na bratacha mar seo a leanas:

| Réimse | Cur síos | Luach
---|---|---|
|0|léamh|1 <<0
|1|scriosta|1 << 1
|2|fhreagair|1 << 2
|3|chriptithe|1 << 3
|4|bratach|1 << 4
|5|le déanaí|1 << 5
|6|dréacht|1 << 6
|7|tús (gan úsáid a thuilleadh)|1 << 7
|8|ar aghaidh|1 << 8
|9|atreoraithe|1 << 9
|10-15|comhaireamh iatán|3F << 10 (6 ghiotán)
|16-22|leibhéal tosaíochta|7F << 16 (7 ngiotán)
|23|sínithe|1 << 23
|24|is dramhlach é|1 << 24
|25|nach dramh é|1 << 25
|26-28|clómhéid deilt|7 << 26 (3 ghiotán)
|29|Leibhéal an dramhphoist taifeadta |1 << 29
|30|aibhsigh an téacs in toc|1 << 30
|31|(gan úsáid)|

## Féach freisin ##

* [EML](/ríomhphost/eml/)

* [MSG](/ríomhphost/msg/)


