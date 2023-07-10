{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo EDB - um arquivo de banco de dados do Exchange Mail",
  "description":"Saiba mais sobre o formato de arquivo EDB e APIs que podem criar e abrir arquivos EDB.",
  "linktitle" : "EDB",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2020-09-16"
}

## O que é um arquivo EDB?

Um arquivo com extensão de arquivo .edb é um banco de dados de caixa de correio criado pelo Microsoft Exchange Server para armazenar dados relacionados a email. EDB, Exchange Database, armazena mensagens que estão em processo e não SMTP. EDB também são conhecidos como arquivos de banco de dados ESE (Extensible Storage Engine) e armazenam arquivos usando a estrutura b-tree. Sendo arquivos de armazenamento, os arquivos EDB podem ser convertidos em outros formatos de arquivo de armazenamento de correio, como [PST](/pt/email/pst/) e [OST](/pt/email/ost/).

## Formato de arquivo EDB

Não há especificações de formato de arquivo EDB oficial/aberto disponíveis que possam ser referenciadas. Algum progresso foi feito para a engenharia reversa do formato do arquivo, resultando na decodificação de especificações parciais. De acordo com estes, um arquivo EDB consiste em:
* File Header - Contém informações do cabeçalho do arquivo de banco de dados
* Páginas de tamanho fixo - Contém o banco de dados que consiste em tabelas e índices

### Cabeçalho do arquivo de banco de dados
O cabeçalho do arquivo de banco de dados reside na primeira página do banco de dados e tem pelo menos 668 bytes. O cabeçalho do arquivo contém `File Format Version` e `File Type` além de outros campos.

#### Tipos de arquivo
|Tipo|Descrição
---|---|
|0| Banco de dados|
|1| Transmissão|

`Nota:` Identificadores para esses tipos não são conhecidos.

#### Versão do formato de arquivo
O formato original do EDB começou em abril de 1997 e continuou evoluindo para mudanças posteriores.

|Data da Revisão|Versão|Revisão|descrição
---|---|---|---|
|Abr 1997| 0x00000620|0x00000000| Formato original do sistema operacional Beta.|
|Maio de 1997 |0x00000620|0x00000001| Adicione colunas no catálogo para indexação condicional e OLD.|
|Jun 1997|0x00000620|0x00000002|Adicionar o sinalizador fLocalizedText no BID.|
|Out 1997|0x00000620|0x00000003|Adicionar SPLIT_BUFFER às páginas raiz da árvore de espaço.|
|Jan 1998|0x00000620|0x00000002|Reverta a revisão para que o ESE97 permaneça compatível com versões futuras.|
||0x00000620|0x00000003|Adicionar novas colunas marcadas ao catálogo ("CallbackData" e "CallbackDependencies").|
|Maio de 1998|0x00000620|0x00000004|Suporte a valor super longo (SLV): signSLV, fSLVExists in dbheader.|
|Maio de 1998|0x00000620|0x00000005|Nova árvore de espaço SLV.|
|Out 1998|0x00000620|0x00000006|Mapa espacial SLV.|
|Dezembro de 1998|0x00000620|0x00000007|IDXSEG de 4 bytes.|
|Jan 1999|0x00000620|0x00000008|Novo formato de coluna de modelo.|
|Jun 1999|0x00000620|0x00000009|Colunas de modelo ordenadas. Usado no Windows XP SP3|
||0x00000620|0x0000000b|Contém o cabeçalho da página com a soma de verificação ECCUsed in Exchange|
||0x00000620|0x0000000c|Usado no Windows Vista (SP0)|
||0x00000620|0x00000011|Suporte para páginas de 2 KiB, 16 KiB e 32 KiB. Cabeçalho de página estendido com somas de verificação ECC adicionais. Compressão de coluna. Dicas de espaço. Usado no Windows 7 (SP0)|
|Maio de 1999|0x00000623|0x00000000|Novo Gerenciador de Espaço.|

### Arquivos de banco de dados

O arquivo de banco de dados EDB contém o esquema para todas as tabelas do banco de dados. Além disso, também inclui registros para todas as tabelas do banco de dados e índices para as tabelas. Sua localização é determinada pelos seguintes identificadores.

* JetCreateDatabase
* JetCreateDatabase2
* JetAttachDatabase
* JetAttachDatabase2

Com base nisso, o estado do banco de dados pode ser avaliado da seguinte forma.

|Valor|Identificador|Descrição
---|---|---|
|1|JET_dbstateJustCreated|O banco de dados acabou de ser criado.|
|2|JET_dbstateDirtyShutdown|O banco de dados requer que a recuperação física ou temporária seja executada para se tornar utilizável ou móvel. Não se deve tentar mover bancos de dados nesse estado.|
|3|JET_dbstateCleanShutdown|O banco de dados está em um estado limpo. O banco de dados pode ser anexado sem nenhum arquivo de log.|
|4|JET_dbstateBeingConverted|O banco de dados está sendo atualizado.|
|5|JET_dbstateForceDetachInternal|Este valor é introduzido no WindowsXP|
 

## Referências
* [Especificações do arquivo de banco de dados (EDB) do mecanismo de armazenamento extensível (ESE)](https://github.com/libyal/libesedb/tree/main/documentation)

