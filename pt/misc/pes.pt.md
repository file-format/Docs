{
  "date" : "2021-07-29",
  "keywords" :[ "arquivo pes", "formato de arquivo pes", "o que é um arquivo pes", "arquivo", "exemplo pes", "extensão de arquivo pes", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PES - Formato de bordado Brother PE",
  "description":"Saiba mais sobre o formato de arquivo PES e APIs que podem criar e abrir arquivos PES.",
  "linktitle" : "PES",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## O que é um arquivo de bordado PES?

O arquivo de bordado PES é um arquivo de desenho que contém instruções para as máquinas de bordar/costurar. Foi desenvolvido pela Brother Industries para suas máquinas de bordar, mas posteriormente foi formalizado como formato de arquivo geral. Os arquivos PES são usados por máquinas de costura para ler instruções para costurar padrões em tecido. Esses arquivos servem a dois propósitos; primeiro fornecendo informações de design para o aplicativo PE-Design desenvolvido pela Brother Industries e segundo, fornecendo o nome do design, cores e códigos da máquina de bordar como "stop", "jump" e "trim".

## Formato de arquivo PES - Mais informações

Um arquivo PES é salvo no disco em formato de arquivo binário. Ele contém várias seções que possuem informações de costura armazenadas usando o método predefinido. O formato do arquivo PES é o seguinte.

* Dados de versão - Fornece informações de versão e pode ser qualquer valor `#PES0001`, `#PES0020`, `#PES0030`, `#PES0040`, `#PES0050`, `#PES0055`, `#PES0060`
* PEC Seek Value - Um inteiro little-endian de 4 bytes seguindo imediatamente os dados da versão e representa o valor de busca para a seção PEC que contém detalhes do projeto Informações
* Seção PSE - Contém informações de design relevantes para o Brother PE-Design e pode ser outras aplicações de costura
* Seção PCE - Pode estar em qualquer lugar no arquivo PSE, mas referenciado pelo PEC Seek Value.

## Tipo de máquina de costura usando arquivo PES

Os arquivos PES são criados principalmente pelo software PE-Design usado com as máquinas de costura Brother. Algumas outras máquinas que podem suportar arquivos PES incluem máquinas de bordar domésticas Babylock e Bernina.

## Como converter arquivos PSE?

O aplicativo de software PE-Design pode [converter arquivo PSE](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl =pes+arquivo) para outros formatos, como .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd ou .xxx. Isso pode ser feito usando o aplicativo PE-Design abrindo o arquivo e selecionando o formato de conversão.

## Referências

* [Projeto PE - Manual de instruções](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)

