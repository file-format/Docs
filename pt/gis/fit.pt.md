{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fit File Format - Garmin Activity File",
  "description":"Saiba mais sobre o formato de arquivo FIT e APIs que podem criar e abrir arquivos FIT.",
  "linktitle" : "FIT",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2022-05-06"
}

## O que é um arquivo FIT?

Um arquivo FIT é um arquivo GIS criado por dispositivos vestíveis esportivos Garmin. Ele é usado para registrar as atividades da pessoa quando ela se move usando esses dispositivos. Os dados de atividade incluem localização e hora conforme registrado pelo dispositivo GPS. Os arquivos FIT também são usados para transferir os dados de atividade registrados usando APIs da web. Essa é a razão pela qual os arquivos FIT são o formato de arquivo mais comumente usado para compartilhar dados de condicionamento físico com outras plataformas de condicionamento físico. Outros formatos de arquivo comuns incluem [GPX](/pt/gis/gpx/), TCX e [KML](/pt/gis/kml/).

## Formato de arquivo FIT - Mais informações

Os arquivos FIT são salvos em disco como arquivos binários com as informações registradas pelos dispositivos Garmin para a atividade. As informações armazenadas em um arquivo FIT incluem:

* Data hora
* Tipos de esporte
* Dados de volta e divisão
* Trilha GPS
* Dados do sensor
* Eventos para sessão ativa

Os dados da atividade podem ser gravados no arquivo em tempo real ou exportados assim que a gravação da atividade estiver concluída.

### Mensagens de Atividade FIT

Um arquivo de atividade FIT pode incluir alguns tipos de mensagens obrigatórios. A seguir estão as mensagens necessárias para um arquivo de atividade.

|Mensagem|Propósito|
---|---|
|ID do arquivo| A mensagem ID do arquivo é exigida por todos os tipos de arquivo FIT e espera-se que seja a primeira mensagem no arquivo. Para arquivos de atividade, a propriedade Type deve ser definida como 4.|
|Atividade| Uma única mensagem de atividade é necessária em um arquivo de atividade FIT. Incluídas na mensagem Activity estão as propriedades Local Timestamp e Session Count. O carimbo de data/hora local é usado para determinar o deslocamento de fuso horário que pode ser aplicado a todos os carimbos de data/hora no arquivo. A maioria dos dispositivos grava arquivos FIT em tempo real e a contagem de sessões será desconhecida até o final da gravação. Devido a isso, a mensagem de atividade geralmente será a última mensagem no arquivo.|
|Sessão| Os arquivos de atividade conterão uma ou mais mensagens de sessão. Uma mensagem de sessão é um tipo de mensagem de resumo. Start Time, Total Elapsed Time, Total Timer Time e Timestamp são campos obrigatórios para todas as mensagens de resumo.|
|Volta| As mensagens de volta representam voltas ou intervalos dentro da sessão. Uma mensagem de volta é um tipo de mensagem de resumo. Start Time, Total Elapsed Time, Total Timer Time e Timestamp são campos obrigatórios para todas as mensagens de resumo.|
|Gravar| As mensagens de gravação incluem coordenadas GPS, velocidade, distância, frequência cardíaca, potência, etc.|

## Recursos úteis do arquivo FIT

* [Decodificando arquivos de atividade FIT](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
* [Codificando arquivos de atividade FIT](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 

## Referências ##

* [Arquivo de atividade FIT](https://developer.garmin.com/fit/file-types/activity/)

