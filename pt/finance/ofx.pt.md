{
  "date" : "2023-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OFX - Formato de arquivo aberto de troca financeira",
  "description":"Aprenda sobre o formato de arquivo OFX e APIs que podem criar e abrir arquivos OFX.",
  "linktitle" : "OFX",
  "menu" : {
    "docs" : {
      "identifier":"finance-ofx",
      "parent" : "finance"
}
},
  "lastmod" : "2023-05-09"
}

## .OFX opção número

Um arquivo OFX (Open Financial Exchange) é um formato de arquivo financeiro usado para troca de informações financeiras entre programas de software e instituições financeiras. Com a evolução das soluções de software para escrituração contábil financeira interna, foram desenvolvidos programas de software que podem se conectar ao seu banco e importar ou exportar dados financeiros com os bancos. Isso inclui dados financeiros, como transações, informações de contas e pagamentos de contas. Programas de software como QuickBooks, Microsoft Money, Intuit e Quicken salvam os dados importados como arquivo OFX.

O tipo de mídia da Internet para o formato de arquivo OFX é application/x-ofx.

## Formato de arquivo OFX

Os arquivos OFX são salvos no formato de arquivo XML (Extensible Markup Language) e usam tags para estruturar os dados. Os arquivos [XML](/pt/web/xml/) são armazenados em formato legível por humanos e podem ser abertos e editados em qualquer editor de texto, como Notepad, Notepad++ ou Apple TextEdit. Os dados armazenados nos arquivos OFX são baseados no padrão **SGML (Standard Generalized Markup Language)**. Os dados armazenados dentro de arquivos OFX normalmente incluem:

* Informações relacionadas a bancos
* Informações de cartão de crédito e débito
* Informações de contas e investimentos
* quaisquer outras transações financeiras

### Exemplo de formato de arquivo OFX

A seguir está a estrutura de dados interna e os dados de amostra de um arquivo OFX de exemplo.

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

Este exemplo de arquivo OFX contém as seguintes informações:

* Informações da conta bancária, como nome do banco, número da conta e saldo
* Lista de transações, incluindo data, tipo e valor de cada transação

Todas essas informações podem ser importadas para um programa de software de finanças pessoais para controlar as transações e despesas da conta.

## Referências ##

* [Câmbio Financeiro Aberto - Pela Wikipedia](https://en.wikipedia.org/wiki/Open_Financial_Exchange)
* [Padrão ISO para troca eletrônica de dados](https://en.wikipedia.org/wiki/ISO_20022)

