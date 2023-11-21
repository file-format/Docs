{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Formato file aperto per lo scambio finanziario",
  "description":"Informazioni sul formato file OFX e sulle API che possono creare e aprire file OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Cos'è un file OFX?

Un file OFX (Open Financial Exchange) è un formato di file finanziario utilizzato per lo scambio di informazioni finanziarie tra programmi software e istituti finanziari. Con l'evoluzione delle soluzioni software per la contabilità finanziaria interna, sono stati sviluppati programmi software in grado di connettersi alla vostra banca e importare o esportare dati finanziari con le banche. Ciò include dati finanziari come transazioni, informazioni sull'account e pagamenti di fatture. Programmi software come QuickBooks, Microsoft Money, Intuit e Quicken salvano i dati importati come file OFX.

Il tipo di supporto Internet per il formato file OFX è application/x-ofx.

## Formato file OFX

I file OFX vengono salvati in formato file XML (Extensible Markup Language) e utilizzano tag per strutturare i dati. I file [XML](/it/web/xml/) sono archiviati in formato leggibile dall'uomo e possono essere aperti e modificati in qualsiasi editor di testo come Blocco note, Notepad++ o Apple TextEdit. I dati archiviati nei file OFX si basano sullo standard **SGML (Standard Generalized Markup Language)**. I dati archiviati all'interno dei file OFX in genere includono:

* Informazioni relative alle banche
* Informazioni sulla carta di credito e debito
* Informazioni su conti e investimenti
*qualsiasi altra operazione finanziaria

### Esempio di formato file OFX

Di seguito è riportata la struttura dei dati interni e i dati di esempio di un file OFX di esempio.

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

Questo file OFX di esempio contiene le seguenti informazioni:

* Informazioni sul conto bancario come nome della banca, numero di conto e saldo
* Elenco delle transazioni inclusa data, tipo e importo di ciascuna transazione

Tutte queste informazioni possono essere importate in un programma software di finanza personale per tenere traccia delle transazioni e delle spese del conto.

## Riferimenti ##

* [Open Financial Exchange - Da Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Standard ISO per lo scambio elettronico di dati](https://en.wikipedia.org/wiki/ISO_20022)

