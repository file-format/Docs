{
  "date" : "2021-08-17",
  "keywords" :[ "arquivo udf", "formato de arquivo udf", "o que é um arquivo udf", "arquivo", "exemplo udf", "extensão de arquivo udf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo UDF e APIs que podem criar e abrir arquivos UDF.",
  "title" :"UDF - Arquivo de formato de disco universal",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## O que é um arquivo UDF?
O arquivo com extensão .udf é um formato de imagem de disco normalmente usado para salvar arquivos em mídia óptica; pode ser usado para gravar DVDs, CDs e outras mídias ópticas; armazena uma coleção de arquivos usando a estrutura de diretórios especificada no padrão UDF; permite que os arquivos sejam excluídos e modificados no disco de destino mesmo depois de gravados. A Optical Storage Technology Association definiu o sistema de arquivos UDF como um padrão para formar um sistema de arquivos comum para todas as mídias óticas, como mídia ótica regravável e mídia somente leitura.

## Formato de arquivo UDF
O formato de arquivo UDF é um sistema de arquivos aberto e neutro de fornecedor para armazenamento de dados de computador para uma ampla variedade de mídias. Ele tem sido usado comumente para DVDs e formatos de disco óptico mais recentes. Normalmente, o software domina um sistema de arquivos UDF em um processo em lote e o grava em mídia ótica em uma única passagem. No entanto, quando ele grava pacotes em mídia regravável, o UDF permite que os arquivos sejam criados, excluídos e alterados no disco, semelhante a um sistema de arquivos de uso geral em mídias removíveis, como unidades flash ou disquetes.
### Especificações UDF
O padrão UDF define as três variações de sistema de arquivos a seguir:

- **Plain Build**: Este é o formato original suportado em todas as revisões de UDF. Introduzido na primeira versão do padrão, esse formato pode ser usado em qualquer tipo de disco que permita acesso aleatório de leitura ou gravação, como DVD+RW, discos rígidos e mídia DVD-RAM.
- **Compilação de IVA**: Usado especificamente para gravar em mídia de gravação única. O VAT é uma estrutura adicional no disco que permite a escrita de pacotes; ou seja, remapear blocos físicos quando arquivos ou outros dados no disco são modificados ou excluídos. Para mídia de gravação única, o disco inteiro é virtualizado, tornando a natureza de gravação única transparente para o usuário; o disco pode ser tratado da mesma forma que um disco regravável.
- **Compilação poupada (RW)**: Usada especificamente para gravar em mídia regravável. Ele adiciona uma Sparing Table extra para gerenciar as falhas que eventualmente ocorrerão em partes do disco que foram regravadas várias vezes. Esta tabela salva o controle de setores desgastados e os remapeia para os que estão funcionando. O gerenciamento de defeitos do UDF não se aplica a sistemas que já implementam outra forma de gerenciamento de defeitos, como o Mount Rainier (MRW) para discos ópticos ou um controlador de disco para um disco rígido.
 




## Referências


* [Windows Imaging Format - pela Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


