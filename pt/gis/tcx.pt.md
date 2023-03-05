{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de Arquivo TCX - Arquivo XML do Centro de Treinamento",
  "description":"Saiba mais sobre o formato de arquivo TCX e APIs que podem criar e abrir arquivos TCX.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## O que é um arquivo TCX?

Um arquivo TCX (Training Center XML) é um formato de troca de dados usado para compartilhar dados entre dispositivos de fitness. Foi introduzido em 2008 com o produto Training Center da Garmin. Dados de treino como frequência cardíaca, cadência de corrida, cadência de bicicleta, calorias e tempo de volta são armazenados no formato [XML](/pt/web/xml/) dentro do arquivo TCX. Além disso, os dados de resumo sobre a trilha de treino também estão incluídos no arquivo TCX. Os arquivos TCX são semelhantes aos arquivos [FIT](/pt/gis/fit/) criados com dispositivos vestíveis esportivos Garmin.

## Formato de arquivo TCX - Mais informações

Os arquivos TCX são salvos em disco como arquivos XML com cada registro salvo como uma atividade. Uma atividade compreende todos os dados de um treino, como tempo, tempo de volta, Id, frequência cardíaca, intensidade, cadência e informações de faixa que contêm os pares de posição junto com o carimbo de data e hora para essa posição lat-long semelhante ao [GPX](/pt/gis/gpx/).

### Versões de formato de arquivo TCX

Existem duas versões desse formato com seus próprios esquemas XML hospedados pela Garmin. Seguem alguns deles:

* https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
* https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
* https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## Protocolo de dados TCX

Uma versão rápida do formato TCX XML está disponível no Github como [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## Referências ##

* [XML da Central de Treinamento](https://en.wikipedia.org/wiki/Training_Center_XML)
* [Visualizador TCX](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)

