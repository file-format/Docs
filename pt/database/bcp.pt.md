{
  "date" : "2020-11-11",
  "keywords" :[ "BCP", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo BCP e APIs que podem criar e abrir arquivos BCP.",
  "title" :"BCP - Formato de arquivo de cópia em massa do SQL Server",
  "linktitle" : "BCP",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-08-12"
}

## O que é um arquivo BCP?

BCP (Bulk Copy Format) é o formato de dados técnicos do Microsoft SQL Server que define estruturas de dados para armazenar diferentes valores de tipo de dados de banco de dados para importação/exportação. O formato define totalmente a interpretação de cada coluna de dados para que o conjunto de valores especificado no arquivo de dados possa ser lido. O utilitário [BCP](https://docs.microsoft.com/en-us/previous-versions/sql/sql-server-2008-r2/ms162802(v=sql.105)) usa o formato de arquivo BCP para ler dados de tal arquivo e identificá-lo.


## Formato de arquivo BCP

O arquivo de formato BCP é um documento XML que define a ordem das colunas, nome e tipo de dados. Ele permite que os usuários importem/exportem grandes quantidades de dados do arquivo de dados especificando esses campos. Isso é útil na importação em massa de valores de dados de arquivos de dados. O número e a ordem dos campos de dados no arquivo de dados podem ser diferentes daqueles nas colunas da tabela de destino. É quando o arquivo de formato de dados BCP ajuda, especificando a ordem e o tipo de colunas para importar os dados.

A estrutura do arquivo de formato é representada no formato a seguir.

```
<BCPFORMAT ...>
    <RECORD>
       <FIELD ID = "fieldID" xsi:type = "fieldType" [...] />
    </RECORD>
    <ROW>
       <COLUMN SOURCE = "fieldID" NAME = "columnName" xsi:type = "columnType" [...]  />
    </ROW>
 </BCPFORMAT>
```

### Tipos de dados BCP

|Tipo de Dados|Intervalo|Representação|
---|---|---|
|BigInt|-263 (-9.223.372.036.854.775.808) a 263-1 (9.223.372.036.854.775.807)|`BigInt = ["-"]1*19DIGIT`|
|Binary|1 a 8000 bytes|formato de string Unicode codificado em hexadecimal `Binary = 32000OCTET`|
|Bit|0 ou 1|string Unicode simples Bit = "0" / "1"|
|Char|1 a 8000|Formato de String Unicode, Char = 16000OCTET|
|CLRUDT|VarBinary|CLRUDT = 0*nOCTET com n = 4 x (2.147.483.647)|
|Data|0001-01-01 a 9999-12-31|formato de string AAAA-MM-DD|
|DataHora|1753-01-01 00:00:00.000 a 9999-12-31 23:59:59.997| Unicode AAAA-MM-DD hh:mm:ss[.nnn] formato de string|
|DataHora2|0001-01-01 00:00:00.0000000 a 9999-12-31 23:59:59.9999999.| Unicode AAAA-MM-DD hh:mm:ss[.nnnnnnn] formato de string|
|DateTimeOffset|0001-01-01 00:00:00.0000000 a 9999-12-31 23:59:59.9999999 no fuso horário UTC (Coordinated Universal Time)| Unicode AAAA-MM-DD hh:mm:ss[.nnnnnnn] [{+|-}hh:mm] formato de string|
|Decimal|-1038 + 1 a 1038 – 1|Formato de string Unicode `Decimal = ["-"] 0*38DIGIT [".."0*38DIGIT]`|
|Float|-1,79E+308 a -2,23E-308; 0; de 2.23E-308 a 1.79E+308|Formato de string Unicode|
|Image|sequência de bytes que variam de 0 a 231 – 1 (2.147.483.647)|formato de string Unicode codificado em hexadecimal|
|Int|-231 (-2.147.483.648) a 231 – 1 (2.147.483.647)|Formato de string Unicode|

## Referências

* [Formato BCP - Microsoft](https://docs.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

