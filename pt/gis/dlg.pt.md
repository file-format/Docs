{
  "date" : "2021-07-30",
  "keywords" :[ "arquivo dlg", "formato de arquivo dlg", "o que é um arquivo dlg", "arquivo", "exemplo dlg", "extensão de arquivo dlg", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLG - Shapefile Shape Index Format",
  "description":"Saiba mais sobre o formato de arquivo DLG e APIs que podem criar e abrir arquivos DLG.",
  "linktitle" : "DLG",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-30"
}

## O que é um arquivo DLG?
Um arquivo com extensão .dlg contém o Digital Line Graph que é um recurso de mapa cartográfico mostrado em forma de vetor digital que é administrado pelo US Geological Survey (USGS). Os arquivos DLG estão disponíveis em dois formatos diferentes:
1. **Formato opcional**: Um formato simples de usar que incorpora um comprimento de registro lógico de 80 bytes, o sistema de coordenadas de solo UTM e as ligações de topologia contidas em elementos de linha, nó e área.
2. **Formato Padrão de Transferência de Dados Espaciais (SDTS)**: um formato que facilita a transferência de dados espaciais entre diferentes sistemas de computador.

## Formato de arquivo DLG
O formato de arquivo DLG é projetado para mapas USGS e são transmitidos em escala grande, intermediária e pequena com até nove categorias diferentes de recursos. Os arquivos DLG vêm em formatos opcionais e padrão de transferência de dados espaciais (SDTS) com estrutura topológica para uso em aplicativos de mapeamento e GIS.
### Especificações do formato de arquivo DLG
Os arquivos DLG são distribuídos em três escalas diferentes:

1. **Grande escala** - normalmente correspondem a:
- O USGS 7,5 por 7,5 minutos
- Série de mapas de quadrângulo topográfico em escala 1:24.000 e 1:25.000
- Escala 1:63.360 para o Alasca
- Escala 1:30.000 para Porto Rico
 

2. **Escala intermediária** - derivada do USGS:

- 30 por 60 minutos

- Série de mapas em escala 1:100.000
3. **Pequena escala** - derivado dos mapas seccionais em escala USGS 1:2.000.000 do Atlas Nacional dos Estados Unidos
### Categorias de dados
Nove categorias diferentes de camadas, ou recursos, estão disponíveis em arquivos DLG:
1. Sistema de Levantamento de Terras Públicas (PLSS)
2. Limites (BD)
3. Transporte (TR)
4. Hidrografia (HY)
5. Hipsografia (HP)
6. Características não vegetativas (NV)
7. Controle e marcadores de levantamento (SM)

8. Recursos artificiais (MS)

9. Cobertura de superfície vegetativa (SC)

Os arquivos DLG de grande escala oferecem todas as nove camadas, enquanto os de escala intermediária oferecem as cinco camadas de PLSS, BD, TR, HY e HP. DLGs de pequena escala oferecem as cinco camadas de PLSS, BD, TR, HY e MS.

## Referências

* [Gráfico de linhas digitais - pela Wikipedia)](https://en.wikipedia.org/wiki/Digital_line_graph)


