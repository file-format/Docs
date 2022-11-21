{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo osm", "o que é um arquivo osm", "arquivo", "exemplo osm", "extensão de arquivo osm", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OSM - Formato de arquivo OpenStreetMap",
  "description":"Saiba mais sobre o formato de arquivo OSM e APIs que podem criar e abrir arquivos OSM.",
  "linktitle" : "OSM",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo OSM?

O OpenStreetMap (OSM) é uma enorme coleção de armazenamentos voluntários de informações geográficas em diferentes tipos de arquivos, usando diferentes esquemas de codificação para converter esses dados em bits e bytes. OSM é um esforço colaborativo para a criação de um mapa do mundo editável gratuitamente. A principal saída desse esforço colaborativo são os dados geográficos, e não o mapa em si. As restrições no uso ou disponibilidade de informações geográficas em grande parte do mundo desencadeiam a necessidade de criar um OSM. Os dados disponíveis do OSM estão prontos para substituir o Google Maps por aplicativos clássicos (Facebook, Craigslist etc.) fontes de dados.

## Breve história ##

Inspirado pelo sucesso da Wikipedia, em 2004, Steve Coast, um empresário britânico, criou este projeto de mapeamento do mundo baseado na comunidade no Reino Unido. Ele inicialmente se concentrou em mapear o Reino Unido. A OpenStreetMap Foundation foi criada em abril de 2006 para apoiar a evolução, expansão e circulação de geoespacial gratuito para qualquer pessoa. Em dezembro de 2006, o Yahoo ajudou o OpenStreetMap com sua fotografia aérea para a produção de mapas. Dados completos de estradas para a Holanda e dados de estradas principais para a Índia e a China foram fornecidos ao OSM em abril de 2007 pela Automotive Navigation Data (AND). Em dezembro de 2007, a Universidade de Oxford foi a organização mais proeminente que integrou os dados do OpenStreetMap em seu site principal. Desde então, mais de 2 milhões de usuários cadastrados contribuem com dados neste projeto usando dispositivos GPS, fotografia aérea e levantamentos manuais. Esses dados contribuídos pela comunidade são disponibilizados sob a Open Database License. Uma organização sem fins lucrativos registrada na Inglaterra, OpenStreetMap Foundation, manteve o site OSM.

## Formato de arquivo OSM ##

Existem muitas maneiras e formatos de arquivo para armazenar dados geográficos, mas o formato de arquivo **OSM** é restrito ao OpenStreetMap. O OSM é um formato padrão especialmente projetado para ser transportado facilmente pela Internet. Um formato ordenado estruturado, codificado em XML constitui um arquivo .osm. No OpenStreetMap existem quatro elementos pivô para armazenar a estrutura de dados topológicos:

{{< figure src="../OSM.png" alt="Formato de arquivo OSM" >}}


|Nós|Formas|Relações|Tags
---|---|---|---|
|<ul><li> Representa a posição geográfica armazenada como pares de latitude e longitude.</li><li> Usado para representar feições do mapa sem tamanho, como picos de montanhas.</li></ul> |<ul><li> Listas ordenadas de nós, significando uma polilinha ou um polígono</li><li> Representam recursos lineares, como estradas e rios, e zonas, como áreas de estacionamento, selvas e parques.</li></ul> |<ul><li> Listas ordenadas de nós e vias representam sua relação como barreiras e curvas em estradas, rodovias abrangem diferentes vias existentes e áreas com buracos.</li></ul> |<ul><li> Armazenar metadados sobre os objetos do mapa.* Sempre anexado a qualquer nó, caminho ou relação</li></ul>


As tags são usadas para caracterizar as características físicas do terreno (edifícios e estradas, etc.) no OpenStreetMap. Cada tag relaciona uma característica geográfica da feição representada por aquele nó ou relação específica. Neste sistema de marcação gratuito, para descrever uma feição, um número ilimitado de atributos pode ser incluído em um mapa. Combinações específicas de chave e valor endossadas por usuários registrados atuam como padrões informais para as tags usadas com frequência. No entanto, novas tags podem ser criadas sempre que novos aspectos exigirem a análise de atributos das feições não mapeados anteriormente. A maioria dos recursos usa apenas um pequeno número de tags para descrição.

Três tipos de arquivos são usados pelo OSM para armazenar seus dados principais.

O OSM lida com todos esses arquivos com as informações sobre seus detalhes de formatação. Mas os mesmos objetos internos são produzidos por esses arquivos. Para arquivos de dados, o sinalizador visível em objetos OSM é sempre verdadeiro, o que não é o caso de arquivos de histórico e alterações.

Em uso comum, há uma diversidade de formatos de arquivo OSM. Os formatos de arquivo definem a codificação do conteúdo no disco ou fio em bits e bytes. O OSM é capaz de ler e escrever no máximo desses formatos.

**XML**

O formato OSM original é baseado em XML. Os dados de retorno da API principal do banco de dados OSM estão no formato XML.

**PBF**

A codificação de buffers de protocolo está no formato binário e um dos formatos mais compactos.

**O5M/O5C**

Formato binário baseado em formato mais simples, mas relativamente menos usado. O OSM pode ler, mas não pode gravar este formato.

**OPL**

Um formato simples proposto para uso com ferramentas de linha de comando padrão do UNIX. Perto de arquivos CSV, permite uma entidade OSM em uma linha.

**DEPURAR**

Um formato baseado em texto destinado a criar para depuração. O OSM pode gravar esse formato, mas não pode ler.

**BURACO NEGRO**

Um formato fictício que descarta todos os dados. O OSM pode gravar este formato, mas não pode ler.

## Armazenamento de dados OSM ##

O banco de dados principal **PostgreSQL** do OSM mantém a cópia principal dos dados do OSM com extensão PostGIS. Para cada primitivo de dados, o banco de dados principal mantém uma tabela cujas linhas armazenam objetos individuais. Todas as edições atualizam este banco de dados e todos os outros formatos são formados usando este banco de dados. Vários pools de banco de dados para download são criados para transferir dados de um lugar para outro. Dois formatos, um usando XML e outro usando Protocol Buffer Binary Format (PBF) definem esses pools. Os dados completos são armazenados em um arquivo chamado planet.osm

## Compressão em arquivos OSM ##

Formatos baseados em texto (XML, OPL e Debug) usam compactação gzip ou bzip2 opcionalmente.

## Referências ##

* [Manual de formatos de arquivo OSM](https://osmcode.org/file-formats-manual/#file-types)
* [OpenStreetMap](https://en.wikipedia.org/wiki/OpenStreetMap#History)
* [Aprenda OSM](https://learnosm.org/en/osm-data/getting-data/)

