{
  "date" : "2021-03-01",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RDL - Arquivo de linguagem de definição de relatório",
  "keywords" :[ "rdl", "linguagem de definição de relatório", "XmlTextWriter", "XSD", "elemento RDL"],
  "description":"Saiba mais sobre o formato de arquivo RDL, que é uma representação XML de uma definição de relatório do SQL Server Reporting Services.",
  "linktitle" : "RDL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-01"
}

## O que é um arquivo RDL? ##

A RDL (Report Definition Language) é um benchmark definido pela Microsoft para definição de relatórios. Um arquivo RDL consiste em um ou vários elementos RDL. Considerando que um elemento RDL consiste em seu tipo de dados e cardinalidade. Um elemento pode ser simples ou complexo. O elemento simples não tem nenhum elemento filho ou atributos, enquanto um elemento complexo tem filhos e atributos opcionais.

## Definição de esquema XML RDL
Um arquivo XML Schema Definition (XSD) valida o arquivo RDL. O esquema define as regras para onde os elementos RDL podem ocorrer em um arquivo .rdl. Um elemento RDL pode ser simples ou complexo. Um elemento simples não possui elementos filhos ou atributos e um elemento complexo possui filhos e, opcionalmente, atributos.

## Criando RDL
Como o RDL é aberto e extensível por natureza, muitos aplicativos e ferramentas podem ser criados para gerar arquivos RDL com base em seu esquema XML. Uma das maneiras mais simples de criar RDL a partir de um aplicativo é usar as classes do Microsoft .NET Framework do namespace **System.Xml** e do namespace System.Linq. Particularmente, a classe **XmlTextWriter** pode ser usada para escrever RDL. Você pode gerar uma definição de relatório completa do início ao fim em qualquer aplicativo .NET Framework usando **XmlTextWriter**. Os desenvolvedores também podem adicionar itens de relatório personalizados com propriedades personalizadas para estender o RDL.

## Tipos de RDL
A tabela a seguir lista os tipos e atributos usados em elementos RDL.

|Tipo|Descrição|
---|---|
|Binário |Uma propriedade com um valor binário codificado em base 64.|
|Booleano| Uma propriedade com true ou false como o valor do objeto. A menos que especificado de outra forma, o valor de um objeto booleano opcional omitido é False.|
|Data |Uma propriedade com um valor de data ou data/hora totalmente especificado especificado no formato de data ISO8601: AAAA-MM-DD[THH:MM[:SS[.S]]].|
|Enum |Uma propriedade com um valor de texto de string que deve ser um de uma lista de valores designados.|
|Float |Uma propriedade com um valor float. Um ponto (.) é usado como separador decimal opcional.|
|Integer |Uma propriedade com um valor inteiro (int32).|
|Language |Uma propriedade com um valor de texto que contém um código de idioma e cultura, como "en-us" para inglês dos EUA. O valor deve ser um idioma específico ou um idioma neutro para o qual um idioma padrão é definido no Microsoft .NET Framework.|
|Nome |Uma propriedade com um valor de texto de cadeia. Os nomes devem ser exclusivos dentro do namespace do item. Se não for especificado, o namespace de um item é o objeto que contém um nome mais interno.|
|NormalizedString |Uma propriedade com um valor de texto de string que foi normalizado.|
|Tamanho |Um elemento de tamanho deve conter um número (com um caractere de ponto usado como separador decimal opcional). O número deve ser seguido por um designador para uma unidade de comprimento CSS, como cm, mm, pol, pt ou pc. Um espaço entre o número e o designador é opcional. Para obter mais informações sobre designadores de tamanho, consulte Referência de unidades e valores CSS.Em RDL, o valor máximo para Tamanho é 160 pol. O tamanho mínimo é 0 pol.|
|String |Uma propriedade com um valor de texto de string.|
|UnsignedInt |Uma propriedade com um valor inteiro não assinado (uint32).|
|Variante |Uma propriedade com qualquer tipo XML simples.|

## Tipos de dados RDL
Em RDL, a Enumeração DataType define o tipo de dados de um atributo, expressão ou parâmetro. A tabela a seguir mostra como os tipos de dados CLR correspondem aos tipos de dados RDL.

|Tipo(s) CLR |Tipo de dados correspondente|
---|---|
|Booleano| Booleano|
|DateTime, DateTimeOffset |DateTime|
|Int16, Int32, UInt16, Byte, SByte |Integer|
|Singular, Duplo |Float|
|String, Char, GUID, Timespan |String|


## Referências ##

- [Report Definition Language (Wikipedia)](https://en.wikipedia.org/wiki/Report_Definition_Language)
- [Report Definition Language (SSRS)](https://learn.microsoft.com/en-us/sql/reporting-services/reports/report-definition-language-ssrs)

