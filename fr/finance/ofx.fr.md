{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Format de fichier d'échange financier ouvert",
  "description":"Découvrez le format de fichier OFX et les API permettant de créer et d'ouvrir des fichiers OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## Qu'est-ce qu'un fichier OFX ?

Un fichier OFX (Open Financial Exchange) est un format de fichier financier utilisé pour l'échange d'informations financières entre des logiciels et des institutions financières. Avec l'évolution des solutions logicielles pour la tenue de comptabilité financière interne, des logiciels ont été développés qui peuvent se connecter à votre banque et importer ou exporter des données financières avec les banques. Cela inclut les données financières telles que les transactions, les informations sur les comptes et les paiements de factures. Les logiciels tels que QuickBooks, Microsoft Money, Intuit et Quicken enregistrent les données importées sous forme de fichier OFX.

Le type de média Internet pour le format de fichier OFX est application/x-ofx.

## Format de fichier OFX

Les fichiers OFX sont enregistrés au format de fichier XML (Extensible Markup Language) et utilisent des balises pour structurer les données. Les fichiers [XML](/fr/web/xml/) sont stockés dans un format lisible par l'homme et peuvent être ouverts et modifiés dans n'importe quel éditeur de texte tel que Notepad, Notepad++ ou Apple TextEdit. Les données stockées dans les fichiers OFX sont basées sur la norme **SGML (Standard Generalized Markup Language)**. Les données stockées dans les fichiers OFX incluent généralement :

*Informations liées aux banques
* Informations sur les cartes de crédit et de débit
* Informations sur les comptes et les investissements
* toute autre transaction financière

### Exemple de format de fichier OFX

Voici la structure des données internes et des exemples de données d'un exemple de fichier OFX.

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

Cet exemple de fichier OFX contient les informations suivantes :

* Informations sur le compte bancaire telles que le nom de la banque, le numéro de compte et le solde
* Liste des transactions comprenant la date, le type et le montant de chaque transaction

Toutes ces informations peuvent être importées dans un logiciel de finances personnelles pour suivre les transactions et les dépenses du compte.

## Les références ##

* [Open Financial Exchange - Par Wikipédia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Norme ISO pour l'échange électronique de données](https://en.wikipedia.org/wiki/ISO_20022)

