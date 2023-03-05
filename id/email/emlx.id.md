{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EMLX - Format Berkas Surat Apple",
  "description":"Pelajari tentang format file EMLX dan API yang dapat membuat dan membuka file EMLX.",
  "linktitle" : "EMLX",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## Apa itu file EMLX?

Format file EMLX diimplementasikan dan dikembangkan oleh Apple. Aplikasi Apple Mail menggunakan format file EMLX untuk mengekspor email. Ada juga aplikasi lain yang dapat membuka file EMLX dan mengonversinya ke format file lain.

## Sejarah Singkat Format File EMLX

Sistem operasi Mac OS X mengadopsi program email yang ada, NeXTMail, dibuat oleh NeXT sebagai bagian dari sistem operasi NeXTSTEP. Apple setelah mengakuisisi NeXT meningkatkan fitur-fiturnya dan sekarang menjadi aplikasi email Apple Mail untuk digunakan sebagai klien email default. Email yang diekspor melalui Apple Mail langsung disimpan sebagai file EMLX. Selain itu, ini adalah klien email default untuk file EMLX saat seseorang membukanya dengan mengklik dua kali di Mac OS.

## Format File EMLX

File EMLx adalah file berbasis teks sederhana yang dapat dibuka di editor teks apa pun seperti Notepad. Struktur file EMLX terdiri dari tiga bagian:

* Hitungan byte untuk pesan - Panjang pesan itu sendiri, ditulis dalam ASCII dalam desimal, diakhiri dengan 0x0a
* Pesan itu sendiri
* Pesan Metadata dalam bentuk XML plist

Ini dapat dijelaskan dengan lebih baik dengan bantuan contoh email berikut yang diambil dari Apple Mail sebagai EMLX dan dibuka di editor teks.

### Contoh EMLX

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

Dalam contoh ini, 875 menunjukkan total panjang pesan. Metadata pesan terlampir di<plist> tag dan bendera dijelaskan sebagai berikut:

|Bidang|Uraian|Nilai
---|---|---|
|0|baca|1 << 0
|1|dihapus|1 << 1
|2|menjawab|1 << 2
|3|terenkripsi|1 << 3
|4|ditandai|1 << 4
|5|terbaru|1 << 5
|6|rancangan|1 << 6
|7|awal (tidak digunakan lagi)|1 << 7
|8|diteruskan|1 << 8
|9|diarahkan|1 << 9
|10-15|jumlah lampiran|3F << 10 (6 bit)
|16-22|tingkat prioritas|7F << 16 (7 bit)
|23|ditandatangani|1 << 23
|24|adalah sampah|1 << 24
|25|bukan sampah|1 << 25
|26-28|delta ukuran font|7 << 26 (3 bit)
|29|tingkat surat sampah tercatat|1 << 29
|30|sorot teks di toc|1 << 30
|31|(tidak digunakan)|

## Lihat juga ##

* [EML](/id/email/eml/)
* [MSG](/id/email/msg/)

