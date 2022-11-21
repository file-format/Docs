{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo remo", "formato de arquivo remo", "o que é um arquivo remo", "arquivo", "exemplo de remo", "extensão de arquivo remo", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - Formato de arquivo de arquivo OpenSimulator",
  "description":"Saiba mais sobre o formato de arquivo OAR e APIs que podem criar e abrir arquivos OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## O que é um arquivo OAR?

Um arquivo com extensão .oar é um arquivo usado pelo aplicativo OpenSimulator, que é um servidor de aplicativos 3D de código aberto para criar um ambiente virtual acessível a vários usuários pela rede. O formato de arquivo OAR fornece os dados de ativos necessários para carregar totalmente o terreno, texturas de objetos e inventários em um sistema diferente. O OpenSimulator também possui hypergrid opcional que permite aos usuários visitar outras instalações do OpenSimulator na web. Os arquivos OAR possuem aplicativo/remo do tipo MIME da Internet e contém um ou mais arquivos arquivados.


## Formato de arquivo OAR

OAR são arquivos binários que são armazenados em formato de arquivo compactado. A versão mais recente do formato de arquivo OAR é a [versão 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) que tem grandes alterações em relação à [versão 0.8] anterior (http://opensimulator.org/wiki/OAR_Format_0 .8). A versão mais recente suporta o armazenamento de várias regiões em um único OAR e não é compatível com versões do OpenSimulator anteriores à 0.7.5. Um arquivo OAR é um arquivo tar compactado em gzip (tar.gz) no formato tar original do unix (não USTAR).

## Exemplo de regiões OAR
Os arquivos AOR podem conter várias regiões. A estrutura do arquivo é a seguinte (este exemplo contém 4 regiões):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## Arquivo OAR.xml

O arquivo de controle de arquivamento contém um número de versão principal para definir a compatibilidade com futuras alterações de formato. A presença de ativos em formato OAR é indicada pelo elemento booleano<assets_included> . As informações sobre as regiões incluídas estão contidas em um manifesto presente no arquivo de controle. Um exemplo de Archive.xml é o seguinte.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Referências

* [Formato OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

