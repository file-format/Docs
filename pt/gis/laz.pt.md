{
  "date" : "2023-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LAZ - Arquivo compactado de troca de dados LIDAR",
  "description":"Aprenda sobre o formato de arquivo LAZ e APIs que podem criar e abrir arquivos LAZ.",
  "linktitle" : "LAZ",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2023-07-18"
}

## O que é um arquivo LAZ?

O formato de arquivo LAZ é uma versão compactada do formato de arquivo LAS (Lidar LASer), projetado especificamente para armazenar dados de nuvem de pontos lidar. Os arquivos LAZ retêm os mesmos dados e estrutura dos arquivos LAS, mas empregam técnicas de compactação sem perdas para reduzir o tamanho do arquivo, preservando a fidelidade dos dados originais.

## Formato de arquivo LAZ - Breve história

O formato de arquivo LAZ foi desenvolvido para atender à crescente demanda por armazenamento e transmissão eficientes de grandes conjuntos de dados lidar. Ao compactar arquivos LAS, os arquivos LAZ reduzem significativamente seu tamanho, tornando-os mais fáceis de gerenciar e transferir. A compressão é obtida empregando uma combinação de diferentes algoritmos, como codificação de entropia e codificação de comprimento variável, para representar atributos de pontos lidar de uma forma mais compacta.

## Formato de arquivo LAZ

Apesar da compactação, os arquivos LAZ mantêm a capacidade de restaurar totalmente os dados LAS originais sem qualquer perda de informações. Isso significa que uma vez que um arquivo LAZ é descompactado, ele pode ser processado e analisado da mesma forma que um arquivo LAS descompactado. O processo de compactação e descompactação normalmente é realizado usando software especializado ou bibliotecas que suportam o formato LAZ.

O formato de arquivo LAZ mantém compatibilidade com arquivos LAS, garantindo a interoperabilidade entre software lidar e ferramentas de processamento. Isso significa que os aplicativos que podem ler e processar arquivos LAS normalmente podem lidar com arquivos LAZ sem quaisquer modificações. Além disso, os arquivos LAZ ainda incluem o cabeçalho do arquivo, registros de comprimento variável (VLRs) e registros de dados de pontos, preservando a mesma estrutura dos arquivos LAS.

## Vantagens do formato de arquivo LAZ

**Tamanho de arquivo reduzido:** A compactação LAZ reduz significativamente o tamanho do arquivo dos conjuntos de dados lidar, tornando-os mais gerenciáveis e fáceis de armazenar e transferir.

**Integridade de dados:** A compactação LAZ não tem perdas, o que significa que os dados descompactados são uma réplica exata dos dados LAS originais, garantindo nenhuma perda de informações ou precisão.

**Interoperabilidade:** os arquivos LAZ são compatíveis com arquivos LAS, permitindo integração perfeita com software e fluxos de trabalho lidar existentes.

**Processamento eficiente:** Devido ao seu tamanho reduzido, os arquivos LAZ podem ser carregados e processados mais rapidamente, melhorando o tempo geral de processamento e análise.

O formato de arquivo LAZ tornou-se amplamente adotado na comunidade lidar como um padrão para armazenamento e troca de dados lidar compactados. Ele oferece um equilíbrio entre compactação eficiente de dados e integridade de dados, facilitando o manuseio de grandes conjuntos de dados lidar, mantendo a precisão e a qualidade dos dados originais.

## Referências

 * https://www.bluemarblegeo.com/knowledgebase/global-mapper-19/LiDAR_Support_in_Global_Mapper.htm
