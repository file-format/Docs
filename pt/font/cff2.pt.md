{
  "date" : "2020-08-20",
  "keywords" :[ "arquivo cff2", "formato de arquivo cff2", "o que é um arquivo cff2", "arquivo", "exemplo cff2", "extensão de arquivo cff2", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFF2 - Formato de arquivo de fonte compacta versão 2",
  "description":"Saiba mais sobre o formato de arquivo CFF2 e APIs para criar e abrir arquivos CFF2.",
  "linktitle" : "CFF2",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## O que é um arquivo CFF2?

O formato de arquivo CFF2 é a versão 2.0 do formato de arquivo CFF e permite o armazenamento eficiente de contornos de glifos e metadados semelhantes ao formato de arquivo CFF. O CFF2 difere do CFF porque se destina a ser usado no contexto de uma fonte OpenType como uma tabela 'sfnt' com a tag CFF2. Ele não pode ser usado como um programa autônomo e depende de dados em outras tabelas OpenType.

## Formato de arquivo CFF2

As [especificações de formato de arquivo CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) contém detalhes sobre layout de dados internos, tipos de dados, tabelas e outras informações internas sobre o formato de arquivo. Ele pode ser referido para referência do desenvolvedor. Alguns dos detalhes sobre estes são os seguintes.

### Layout de dados

Os dados binários do formato de arquivo CFF2 são organizados logicamente como várias estruturas de dados separadas. O layout dentro dos dados binários é mostrado na tabela a seguir.

|Entrada |Comentários|
---|---|
|Cabeçalho |Localização fixa|
|Top DICT| Local fixo|
|Global Subr ÍNDICE| Localização fixa|
|Variação |Loja|
|FDSelect |Apresentar apenas se houver mais de um Font DICT no Font DICT INDEX.|
|Fonte DICT INDEX ||
|Matriz de fonte DICT| Incluído na fonte DICT INDEX.|
|DICT Privado| Um por fonte DICT.|

Apenas as três primeiras estruturas são baseadas em localizações fixas. Os demais são alcançados por meio de deslocamentos e sua ordem pode ser alterada.

### Tipos de dados

O formato de arquivo CFF2 usa os seguintes tipos de dados.

|Nome |Intervalo |Descrição|
---|---|---|
|uint8 |0 a 255 |número sem sinal de 8 bits|
|uint16 |0 a 65535| número sem sinal de 16 bits|
|uint32 |0 a 4294967295| número sem sinal de 32 bits|
|Deslocamento |varia| Deslocamentos de 1, 2, 3 ou 4 bytes (especificados pelo campo OffSize em uma tabela de índice)|
|OffSize |1 a 4| Número sem sinal de 1 byte especifica o tamanho de um campo ou campos de deslocamento|

Ele armazena todos os dados numéricos de vários bytes e campos de deslocamento em ordem de bytes big-endian. O formato CFF2 está livre de bytes de preenchimento, pois não respeita nenhuma restrição de alinhamento.

### Dados DICT

Os arquivos CFF2 contêm os dados do dicionário de fontes como pares de valores-chave em um formato tokenizado compacto. As chaves do dicionário são codificadas como operadores de 1 ou 2 bytes e os valores do dicionário são codificados como operandos numéricos de tamanho variável. Existem três estruturas que usam o formato de dados DICT: `Top DICT`, `Font DICT` e `Private DICT`. Vários tipos de operandos inteiros de tamanhos variados são definidos e codificados conforme mostrado na tabela a seguir (o primeiro byte do operando é b0, o segundo é b1 e assim por diante).

|Tamanho |intervalo b0 |Intervalo de valores |Cálculo do valor|
---|---|---|---|
|1 |32 a 246| -107 a +107 |b0 - 139|
|2 |247 a 250| +108 a +1131 |(b0 - 247) * 256 + b1 + 108|
|2 |251 a 254| -1131 a -108| -(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 a +32767| b1 << 8 | b2|
|5 |29| -(2^31) a +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Cabeçalho

Os dados binários começam com um cabeçalho com o formato mostrado na Tabela abaixo.

|Tipo |Nome |Descrição|
---|---|---|
|uint8| majorVersão| Formate a versão principal. Defina como 2.|
|uint8| menorVersão| Formate a versão menor. Defina como zero.|
|uint8| headerSize| Tamanho do cabeçalho (bytes).|
|uint16| topDictLength| Comprimento da estrutura Top DICT em bytes.|

## Referências

* [Formato de arquivo CFF2](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

