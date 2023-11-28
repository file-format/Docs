{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Buka Format File Pertukaran Keuangan",
  "description":"Pelajari tentang format file OFX dan API yang dapat membuat dan membuka file OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Apa itu file OFX?

File OFX (Open Financial Exchange) adalah format file keuangan yang digunakan untuk pertukaran informasi keuangan antara program perangkat lunak dan lembaga keuangan. Dengan evolusi solusi perangkat lunak untuk pembukuan akuntansi keuangan internal, program perangkat lunak telah dikembangkan yang dapat terhubung ke bank Anda dan mengimpor atau mengekspor data keuangan dengan bank. Ini termasuk data keuangan seperti transaksi, informasi rekening, dan pembayaran tagihan. Program perangkat lunak seperti QuickBooks, Microsoft Money, Intuit, dan Quicken menyimpan data yang diimpor sebagai file OFX.

Jenis media Internet untuk format file OFX adalah application/x-ofx.

## Format File OFX

File OFX disimpan dalam format file XML (Extensible Markup Language) dan menggunakan tag untuk menyusun data. File [XML](/id/web/xml/) disimpan dalam format yang dapat dibaca manusia dan dapat dibuka serta diedit di editor teks apa pun seperti Notepad, Notepad++, atau Apple TextEdit. Data yang disimpan di dalam file OFX didasarkan pada standar **SGML (Standard Generalized Markup Language)**. Data yang disimpan di dalam file OFX biasanya meliputi:

* Informasi terkait bank
* Informasi Kartu Kredit dan Debit
* Informasi akun dan investasi
* transaksi keuangan lainnya

### Contoh Format File OFX

Berikut adalah struktur data internal dan contoh data dari contoh file OFX.

```
<?xml version="1.0" encoding="UTF-8" standalone="no"?>
<?OFX OFXHEADER="200" VERSION="211" SECURITY="NONE" OLDFILEUID="NONE" NEWFILEUID="12345678901234567890123456789012"?>
<OFX>
  <SIGNONMSGSRSV1>
    <SONRS>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Sign On</MESSAGE>
      </STATUS>
      <DTSERVER>20230510120000</DTSERVER>
      <LANGUAGE>ENG</LANGUAGE>
      <FI>
        <ORG>BANK NAME</ORG>
        <FID>123456789</FID>
      </FI>
    </SONRS>
  </SIGNONMSGSRSV1>
  <BANKMSGSRSV1>
    <STMTTRNRS>
      <TRNUID>1000000001</TRNUID>
      <STATUS>
        <CODE>0</CODE>
        <SEVERITY>INFO</SEVERITY>
        <MESSAGE>Successful Transaction</MESSAGE>
      </STATUS>
      <STMTRS>
        <CURDEF>USD</CURDEF>
        <BANKACCTFROM>
          <BANKID>987654321</BANKID>
          <ACCTID>123456789</ACCTID>
          <ACCTTYPE>CHECKING</ACCTTYPE>
        </BANKACCTFROM>
        <BANKTRANLIST>
          <DTSTART>20230501000000</DTSTART>
          <DTEND>20230510000000</DTEND>
          <STMTTRN>
            <TRNTYPE>DEBIT</TRNTYPE>
            <DTPOSTED>20230503000000</DTPOSTED>
            <TRNAMT>-100.00</TRNAMT>
            <FITID>1000000001</FITID>
            <NAME>Grocery Store</NAME>
          </STMTTRN>
          <STMTTRN>
            <TRNTYPE>CREDIT</TRNTYPE>
            <DTPOSTED>20230505000000</DTPOSTED>
            <TRNAMT>2000.00</TRNAMT>
            <FITID>1000000002</FITID>
            <NAME>Paycheck</NAME>
          </STMTTRN>
        </BANKTRANLIST>
        <LEDGERBAL>
          <BALAMT>5000.00</BALAMT>
          <DTASOF>20230510000000</DTASOF>
        </LEDGERBAL>
      </STMTRS>
    </STMTTRNRS>
  </BANKMSGSRSV1>
</OFX>
```

Contoh file OFX ini berisi informasi berikut:

* Informasi rekening bank seperti nama bank, nomor rekening, dan saldo
* Daftar transaksi termasuk tanggal, jenis, dan jumlah setiap transaksi

Semua informasi ini dapat diimpor dalam program perangkat lunak keuangan pribadi untuk melacak transaksi dan pengeluaran akun.

## Referensi ##

* [Pertukaran Keuangan Terbuka - Oleh Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Standar ISO untuk Pertukaran Data Elektronik](https://en.wikipedia.org/wiki/ISO_20022)

