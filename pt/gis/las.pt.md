{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAS - formato de arquivo Lidar LASer",
  "description":"Aprenda sobre o formato de arquivo LAS e APIs que podem criar e abrir arquivos LAS.",
  "linktitle" : "LAS",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## O que é um arquivo .LAS?

O formato de arquivo LAS (Lidar LASer) é um formato de arquivo binário projetado especificamente para armazenar dados de nuvem de pontos lidar. Ele foi desenvolvido e é mantido pela Sociedade Americana de Fotogrametria e Sensoriamento Remoto (ASPRS) como um formato padronizado para troca e interoperabilidade de dados lidar.

Os arquivos LAS armazenam informações detalhadas sobre pontos lidar individuais, incluindo suas coordenadas 3D (x, y e z), valores de intensidade, códigos de classificação e atributos adicionais. O formato suporta retorno discreto e dados lidar de forma de onda completa, permitindo o armazenamento de múltiplos retornos por pulso de laser.

## Formato de arquivo LAS

A estrutura de um arquivo LAS consiste em três seções principais: o cabeçalho do arquivo, os registros de comprimento variável (VLRs) e os registros de dados de ponto.

1. Cabeçalho do arquivo: O cabeçalho do arquivo contém informações essenciais sobre o arquivo LAS, como versão do formato dos dados, formato dos dados do ponto, número de pontos, coordenadas da caixa delimitadora, sistema de referência de coordenadas (CRS) e outros metadados. Ele fornece um resumo dos dados lidar contidos no arquivo.

2. Registros de comprimento variável (VLRs): os VLRs são opcionais e podem armazenar metadados adicionais e informações personalizadas sobre os dados lidar. Os VLRs permitem flexibilidade na extensão do formato para acomodar requisitos específicos do usuário. Exemplos de VLRs incluem informações sobre o sistema de sensores, parâmetros de processamento de dados ou esquemas de classificação.

3. Registros de dados de pontos: Os registros de dados de pontos armazenam as medições lidar reais. Cada registro de dados de ponto representa um único ponto lidar e contém atributos como coordenadas x, y e z, valores de intensidade, códigos de classificação (por exemplo, solo, vegetação, edifícios) e outros atributos definidos pelo usuário. Os registros de pontos também podem armazenar registros de data e hora, contagens de retorno e ângulos de varredura.

Os arquivos LAS suportam diferentes formatos de dados (0 a 10) para acomodar vários tipos de dados lidar e o nível de informação necessário. Por exemplo, o formato 0 representa um formato de ponto simples com informações básicas, enquanto os formatos 1 a 3 fornecem dados mais abrangentes, incluindo informações de forma de onda para cada retorno.

Os arquivos LAS são amplamente suportados por software lidar e ferramentas de processamento, tornando-os um formato padrão para troca e análise de dados lidar. Além disso, os arquivos LAS podem ser compactados usando técnicas de compactação sem perdas para reduzir o tamanho do arquivo e, ao mesmo tempo, preservar a fidelidade dos dados originais. A versão compactada dos arquivos LAS é frequentemente chamada de LAZ, que oferece recursos eficientes de armazenamento e transferência de dados.

## Referências

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
