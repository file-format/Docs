{
  "date" : "2019-10-11",
  "keywords" :[ "ma", "ma file", "ma file format", "file format", "3d", "ma file download", ".ma file", ".ma"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo MA e APIs que podem abrir e criar arquivos MA.",
  "title" :"Formato de arquivo MA",
  "linktitle" : "MA",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-06-04"
}

## O que é um arquivo MA?

Um arquivo com extensão .ma é um arquivo de projeto 3D criado com o aplicativo Autodesk Maya. Ele contém uma grande lista de comandos textuais para especificar informações sobre o arquivo. Um arquivo **.ma** pode ser aberto e editado em qualquer editor de texto para corrigir quaisquer problemas com os comandos caso um arquivo seja corrompido. Esses arquivos contêm informações para definir as informações da cena 3D, como geometria, iluminação, animação e renderização.

## Formato de arquivo MA

Os arquivos MA são salvos no disco no formato de texto ASCII, ao contrário dos arquivos MB que são salvos no formato de arquivo binário no disco. Uma referência detalhada para o formato de arquivo MA está disponível em [Autodesk Maya Documentation](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001) e pode ser consultada para referência do desenvolvedor.

### Cabeçalho do arquivo MA

O cabeçalho do arquivo MA começa com uma seção de comentários que fornece as informações de criação do arquivo e a data de modificação. Os leitores de arquivos do Maya ignoram esse bloco, pois ele é usado apenas para fins informativos. Um cabeçalho deve começar com os primeiros seis caracteres como "//Maya".

O cabeçalho do arquivo ASCII se parece com o seguinte.

```
//Maya ASCII 1.0 scene
//Name: solstice.ma
//Last modified: Sun, Dec 21, 97 10:18:26 AM
```
### Referências de arquivo

A seção de referências de arquivo de um arquivo .ma contém informações sobre todos os outros arquivos do Maya que estão sendo referenciados nesse arquivo. Cada arquivo referenciado pode ser lido usando um único comando de arquivo contido no mesmo arquivo. A sintaxe do comando file quando usado para referência é:

```
file -r -rpr prefixString fileName;
```
ou

```
file -r -ns nameSpace fileName
```
Aqui está uma string de exemplo.

```
file -r -rpr "solar" "/u/sally/work/solar.ma";
```
Este exemplo mostra que o objeto sol contido no arquivo `solar` seria acessível neste arquivo usando o nome "solar_sun".

### Requisitos

A seção de requisitos de um arquivo .ma consiste em uma série de comandos necessários e informa a May informações como versão e informações de plug-in que são necessárias para ler os arquivos. Um exemplo de seção de requisitos é o seguinte.

```
requires maya "2.0";
requires specialPlugIn "1.2";
```


A próxima seção especifica os requisitos. Isso consiste em uma série de comandos require. Esta seção do arquivo informa ao Maya qual software é necessário para carregar o arquivo corretamente. Especificamente, qual versão do Maya e quais plug-ins.

## Download do arquivo MA
É um pouco difícil encontrar e baixar o arquivo MA de um modelo 3d. Portanto, você pode baixar um arquivo MA de amostra aqui:

- [Amostra.ma](../amostra.ma)


## Referências

* [Organização de arquivos Maya ASCII - Autodesk](https://download.autodesk.com/us/maya/2010help/index.html?url=Glossary_M_ma_file_format.htm,topicNumber=d0e192001)

