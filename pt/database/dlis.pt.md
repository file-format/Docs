{
  "date" : "2023-01-16",
  "keywords" : [ "DLIS", "what is a DLIS file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Saiba mais sobre o formato de arquivo DLIS e APIs que podem criar e abrir arquivos DLIS.",
  "title" : "Formato de arquivo DLIS - arquivo de dados de registro de poço",
  "linktitle" : "DLIS",
  "menu" : {
    "docs" : {
      "identifier":"database-dlis-pt",
      "parent" : "database"
}
},
  "lastmod" : "2020-01-16"
}

## O que é um arquivo .DLIS?

O formato de arquivo .dlis é um formato de arquivo padrão para armazenamento e troca de dados de registro de poços na indústria de petróleo e gás. O formato foi desenvolvido pelo comitê Logging Industry Data Standard (LIDS) e significa Digital Log Information Standard. O formato foi projetado para armazenar dados de registro de poço de uma forma que seja fácil de ler, gravar e trocar entre diferentes sistemas.

Os arquivos DLIS contêm um conjunto de registros lógicos que descrevem os dados de registro do poço e suas características, como o tipo de dados de registro (por exemplo, resistividade, raios gama), as unidades de medição e a localização dos dados no poço. Os dados de log reais são armazenados em arquivos binários separados e referenciados pelos registros lógicos no arquivo DLIS.

## Breves informações sobre dados de registro de poço

Os dados de perfil do poço são um registro de medições feitas em diferentes profundidades em um poço, normalmente durante o processo de perfuração ou após o poço ter sido perfurado. Essas medições podem incluir várias propriedades físicas, químicas e/ou geofísicas da rocha e dos fluidos no poço. Alguns exemplos de dados de registro de poço incluem:

- Resistividade elétrica: uma medida da capacidade da rocha em resistir ao fluxo de uma corrente elétrica
- Raio gama: uma medida da radioatividade natural da rocha
- Porosidade: medida da quantidade de espaços abertos ou poros na rocha
- Sonic: uma medida do tempo que uma onda sonora leva para viajar através da rocha
- Densidade: uma medida da massa de uma rocha por unidade de volume
- Litologia: uma medida do tipo ou formação rochosa

Os dados de registro de poço são usados para diversos fins na indústria de petróleo e gás, como:

- Identificação da localização e qualidade das formações contendo hidrocarbonetos
- Avaliar o potencial de produção de um poço
- Planejar e monitorar a conclusão e estimulação de um poço
- Monitorando o comportamento do poço ao longo do tempo

## Relação com PPDM

PPDM (Professional Petroleum Data Management) é um padrão de gerenciamento de dados da indústria de petróleo e gás que fornece um modelo de dados comum para gerenciar dados de poço e produção. O modelo de dados PPDM define um conjunto de objetos de dados padrão e relacionamentos que podem ser usados para organizar e gerenciar dados de registro de poço, incluindo dados DLIS.

O modelo de dados PPDM inclui objetos de dados para dados de poço e de produção, como poços, cabeçalhos de poço, registros de poço e dados de produção. Também inclui relacionamentos entre esses objetos de dados, como o relacionamento entre um poço e os registros de poço associados a ele.

O modelo de dados PPDM fornece uma maneira consistente e padrão do setor para organizar e gerenciar dados de registro de poço, incluindo dados DLIS. Permite que diferentes organizações compartilhem e troquem dados usando um modelo de dados comum, melhorando a interoperabilidade dos dados e reduzindo os custos de integração de dados.

O uso conjunto do modelo de dados PPDM e dos dados DLIS torna possível armazenar e gerenciar dados de registro de poço de maneira consistente com os padrões da indústria e facilmente acessíveis a outros sistemas e aplicações.


