{
  "date" : "2021-06-14",
  "keywords" :[ "SAV", "extensão", "sav file", "sav file format", "Database File Type", "Database File Format", "o que é um sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo SAV e APIs que podem criar e abrir arquivos SAV.",
  "title" :"SAV - Arquivo de Dados SPSS",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## O que é um arquivo SAV?
O arquivo SAV é um arquivo de dados criado pelo Statistical Package for the Social Sciences (SPSS), que é um aplicativo amplamente utilizado por pesquisadores de mercado, pesquisadores de saúde, empresas de pesquisa, governo, pesquisadores de educação, organizações de marketing, mineradores de dados para análise estatística. O SAV salvo em um formato binário proprietário e consiste em um conjunto de dados, bem como um dicionário que representa o conjunto de dados, salva os dados em linhas e colunas.

## Formato de arquivo SAV
O formato de arquivo SAV tornou-se relativamente estável, mas não podemos dizer que é estático. A compatibilidade com versões anteriores e posteriores está disponível opcionalmente quando necessário, mas não é mantida adequadamente. Os dados em um arquivo SAV são categorizados nas seguintes seções:

### Cabeçalho do arquivo
Consiste em 176 bytes. Os primeiros 4 bytes indicam a string **$FL2** ou **$FL3** na codificação de caracteres usada para o arquivo. Os últimos três bytes representam que os dados no arquivo são compactados usando **ZLIB**. A próxima string de 60 bytes começa com **@(#) SPSS DATA FILE** e também determina o sistema operacional e a versão do SPSS que criou o arquivo. O cabeçalho então continua com campos de seis dígitos, contendo o número de variáveis por observação e um código de dígito para compactação, e termina com dados de caracteres indicando a data e hora de criação e um rótulo de arquivo.
### Registros de descritores de variáveis
O registro contém uma sequência fixa de campos, classificando o tipo e o nome da variável juntamente com as informações de formatação utilizadas pelo SPSS. Cada registro de variável pode conter opcionalmente um rótulo de variável de até 120 caracteres e até três especificações de valor ausente.
### Rótulos de valor
Os rótulos de valor são opcionais e armazenados em pares de registros com tags inteiras 3 e 4. O primeiro registro que é tag 3 possui uma sequência de pares de campos, cada par contendo um valor e o rótulo de valor associado. O segundo registro que é o tag 4, representa a quais variáveis o conjunto de valores/rótulos se aplica.
### Documentos
Registros únicos ou múltiplos com tag de inteiro 6. Documentação opcional. contém linhas de 80 caracteres.
### Registros de extensão
Registros únicos ou múltiplos com tag de inteiro 7. Os registros de extensão fornecem informações que podem ser ignoradas com segurança, mas preservadas, em muitas situações, permitem que arquivos escritos por softwares mais recentes preservem a compatibilidade com versões anteriores. Os registros de extensão têm tags de subtipo inteiro.
### Terminador de dicionário
Grave somente com tag de inteiro 999. Separa o dicionário das observações dos dados.
### Observações de dados
Considera-se que os dados estão em ordem de observação, por exemplo, todos os valores de variáveis para a primeira observação, seguidos por todos os valores para a segunda observação, etc. O formato do registro de dados varia dependendo do código de compactação no registro do cabeçalho do arquivo. A parte de dados de um arquivo .sav pode ser descompactada:
- **código 0**: compactado por bytecode
- **código 1**: compactado usando a compactação ZLIB
 







## Referências ##

* [SPSS System Data File Format Family (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)

