{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Formato de archivo abierto de intercambio financiero",
  "description":"Obtenga más información sobre el formato de archivo OFX y las API que pueden crear y abrir archivos OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## ¿Qué es un archivo OFX?

Un archivo OFX (Open Financial Exchange) es un formato de archivo financiero utilizado para el intercambio de información financiera entre programas de software e instituciones financieras. Con la evolución de las soluciones de software para la contabilidad financiera interna, se han desarrollado programas de software que pueden conectarse a su banco e importar o exportar datos financieros con los bancos. Esto incluye datos financieros como transacciones, información de cuentas y pagos de facturas. Los programas de software como QuickBooks, Microsoft Money, Intuit y Quicken guardan los datos importados como archivos OFX.

El tipo de medio de Internet para el formato de archivo OFX es application/x-ofx.

## Formato de archivo OFX

Los archivos OFX se guardan en formato de archivo XML (lenguaje de marcado extensible) y utilizan etiquetas para estructurar los datos. Los archivos [XML](/es/web/xml/) se almacenan en formato legible por humanos y se pueden abrir y editar en cualquier editor de texto como Notepad, Notepad++ o Apple TextEdit. Los datos almacenados dentro de los archivos OFX se basan en el estándar **SGML (lenguaje de marcado generalizado estándar)**. Los datos almacenados dentro de archivos OFX suelen incluir:

* Información relacionada con bancos.
* Información de tarjetas de crédito y débito
* Información de cuentas e inversiones.
* cualquier otra transacción financiera

### Ejemplo de formato de archivo OFX

A continuación se muestra la estructura de datos interna y los datos de muestra de un archivo OFX de ejemplo.

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

Este archivo OFX de ejemplo contiene la siguiente información:

* Información de la cuenta bancaria, como nombre del banco, número de cuenta y saldo
* Lista de transacciones incluyendo fecha, tipo y monto de cada transacción

Toda esta información se puede importar a un programa de software de finanzas personales para realizar un seguimiento de las transacciones y gastos de la cuenta.

## Referencias ##

* [Open Financial Exchange - Por Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Estándar ISO para el intercambio electrónico de datos](https://en.wikipedia.org/wiki/ISO_20022)

