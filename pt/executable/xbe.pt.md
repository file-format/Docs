{
  "date" : "2021-08-31",
  "keywords" :[ "arquivo xbe", "formato de arquivo xbe", "o que é um arquivo xbe", "arquivo", "exemplo xbe", "extensão de arquivo xbe", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo XBE e APIs que podem criar e abrir arquivos XBE.",
  "title" :"XBE - Arquivo de pacote de aplicativos iOS",
  "linktitle" : "XBE",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-31"
}

## O que é um arquivo XBE?
Um arquivo com extensão .xbe é um aplicativo executável de um disco de videogame Xbox. Os arquivos XBE são os principais arquivos que são executados no sistema Xbox e não devem ser abertos normalmente em um computador, mas podem ser abertos em um PC usando um programa de emulação do Xbox. Esses arquivos geralmente são criados por desenvolvedores de jogos e, em seguida, assinados pela Microsoft. A estrutura do arquivo é semelhante aos arquivos do Windows PE, mas algumas alterações importantes de acordo com as configurações do XBox são aplicadas para torná-lo executável no XBox.

## Formato de arquivo XBE
O arquivo XBE é composto por um cabeçalho de imagem, uma coleção de cabeçalhos de seção, um certificado, dados de armazenamento local de thread, uma coleção de versões de biblioteca, bitmap da Microsoft e as seções que contêm o código e os recursos.

### Cabeçalho da imagem
O cabeçalho da imagem contém as informações que explicam onde os outros componentes do executável estão localizados no arquivo e como o executável deve ser tratado e carregado.

### Tabela TLS
A Tabela TLS consiste em todas as informações necessárias ao XBE para configurar corretamente o armazenamento local de thread. É basicamente exclusivo do diretório TLS encontrado em arquivos PE32 e pode ser copiado diretamente de lá. Esta tabela pode ser omitida, se o arquivo XBE não usar nenhum armazenamento local de thread, e o respectivo campo no cabeçalho da imagem definido como zero.

| Deslocamento | Tamanho | Nome | Descrição |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Início de dados brutos | Endereço absoluto (ou seja, não um RVA) de início dos dados da variável TLS na imagem do programa. |
| 0x0004 | 0x0004 | Fim dos dados brutos | Endereço absoluto (ou seja, não um RVA) do final dos dados da variável TLS na imagem do programa. |
| 0x0008 | 0x0004 | Endereço do Índice | Endereço absoluto (ou seja, não um RVA) da variável de índice TLS. |
| 0x000C | 0x0004 | Endereço de Retornos | Endereço absoluto (ou seja, não um RVA) da tabela de funções de retorno de chamada TLS terminada em nulo. |
| 0x0010 | 0x0004 | Tamanho do preenchimento zero | O número de bytes após os dados brutos que devem ser definidos como zero na memória. |
| 0x0014 | 0x0004 | Características | Descreve o alinhamento. |

### Certificado

Um certificado é obrigatório para cada executável do Xbox que contém informações sobre os títulos:
 


- Hora e data em que o certificado foi criado
- ID do título
- Nome do título
- IDs de títulos alternativos
- Tipos permitidos de mídia a partir dos quais o executável pode ser executado (HD, DVD, CD, etc.)
- Região do jogo
- Classificações do jogo
- Número do disco
- Versão
- Dados brutos de chave LAN usados para System Link
- Dados brutos da chave de assinatura (usados para assinar jogos salvos)
- Chaves de assinatura alternativas
- Tamanho original do certificado
- Nome do serviço online (não presente nos primeiros executáveis)
- Sinalizadores de segurança em tempo de execução (não presentes nos primeiros executáveis)
 


### Tipos de mídia permitidos
Tipos de mídia que são permitidos pelo executável para execução. Os seguintes valores são conhecidos:
| Tipo de mídia | Valor |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDIA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDIA_MASK | 0x00FFFFFF |

### Seções
As seções são expressas pelos cabeçalhos de seção. Os cabeçalhos das seções começam logo após o certificado e contêm informações onde no arquivo as seções reais existem. Pelo menos duas seções estão sempre presentes em um executável do Xbox:


- .texto


- .rdata


## Referências



* [Xbe - XBox Executável](https://xboxdevwiki.net/Xbe)


