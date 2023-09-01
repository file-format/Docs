{
  "date" : "2020-11-11",
  "keywords" :[ "BAK", "extensão", "arquivo", "formato de arquivo", "Tipo de arquivo BAK", "Extensão de arquivo BAK", "Tipo de arquivo de banco de dados", "Formato de arquivo de banco de dados", "Arquivos de banco de dados" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo BAK e APIs que podem criar e abrir arquivos BAK.",
  "title" :"Formato de arquivo BAK - Arquivo de backup de banco de dados",
  "linktitle" : "BAK",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-12-04"
}

## O que é um arquivo BAK?

Um arquivo com extensão .bak geralmente é um arquivo de backup usado por diferentes ferramentas de software para armazenar backups de dados. Da perspectiva do banco de dados, um arquivo BAK é usado pelo Microsoft SQL Server para armazenar o conteúdo de um banco de dados. Todos os dados e arquivos associados ao banco de dados são armazenados neste formato de arquivo para serem recuperados caso o banco de dados se torne corrompido ou inválido por qualquer motivo. Os arquivos de backup podem ser armazenados e indexados em outros servidores para fins de segurança. Vários aplicativos podem criar arquivos BAK, como SQL Server Management Studio, Transact-SQL e Windows PowerShell.

## Formato de arquivo BAK

Os detalhes internos de um arquivo BAK não são conhecidos, mas é amplamente assumido que ele é baseado no Microsoft Tape Format (MTF). As especificações MTF estão disponíveis e podem ser referenciadas para entender a estrutura do arquivo. O documento fornece detalhes sobre armazenamento MTF para qualquer pessoa que tenha um conhecimento geral sobre operações de gerenciamento de armazenamento, unidades de fita e sistemas de arquivos.

### Conjuntos de dados

Um conjunto de dados é uma coleção de objetos gravados em uma mídia de armazenamento (fita, disco óptico etc.) durante o backup ou restauração de dados. Os conjuntos de dados são compostos por várias mídias em caso de grande volume de dados.

### Elementos Fundamentais do MTF

Um arquivo MTF consiste em alguns elementos fundamentais que constituem seus blocos de construção. Esses elementos são:

#### Blocos de Descritores

Os blocos descritores (DBLK) são usados para controle de formato e constituem as bases primárias de um arquivo MTF. Um único arquivo MTF define vários DBLKs para cada função exclusiva. Cada DBLK é um bloco de dados de comprimento variável que é dividido nas seguintes quatro partes:

* `Common Block Header` - Estrutura de comprimento fixo que é comum a todos os DBLKs. Este é o único cabeçalho de bloco que é necessário.
* `DBLK Type Information` - Bloco de comprimento fixo específico para o tipo de DBLK que está sendo definido
* `Dados do sistema operacional` - dados específicos que são definidos com base no tipo de DBLK e sistemas operacionais
* `Informações DBLK` - Informações específicas de DBLK de comprimento variável que não podem ser salvas com as informações de DBLK de comprimento fixo.

 {{< figure src="../bak.png" alt="Formato de arquivo de backup do Microsoft SQL" >}}

#### Fluxo de dados

Os fluxos de dados em um arquivo MTF são usados para encapsulamento e alinhamento de dados. É composto por um Stream Header, seguido pelos Stream Data. Um cabeçalho de fluxo pode encapsular apenas um único tipo de dados de fluxo.

{{< figure src="../bak_datastream.png" alt="Formato de arquivo de backup do Microsoft SQL" >}}

#### Marcas de arquivo

Uma marca de arquivo é usada para separação lógica e acesso rápido em uma mídia. As marcas de arquivo são emuladas pelo driver de dispositivo ou pelo uso do bloco Soft Filemark Descriptor caso o dispositivo que está sendo usado não forneça marcas de arquivo.

## Referências ##

* [[MS-BCP]: Formato de cópia em massa](https://learn.microsoft.com/en-us/openspecs/sql_data_portability/ms-bcp/54965c4d-34c7-400d-b970-1007984315a5)

