{
  "date" : "2021-07-28",
  "keywords" :[ "arquivo ntf", "formato de arquivo ntf", "o que é um arquivo ntf", "arquivo", "exemplo ntf", "extensão de arquivo ntf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - Arquivos de formato de transferência nacional",
  "description":"Saiba mais sobre o formato de arquivo NTF e APIs que podem criar e abrir arquivos NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## O que é um arquivo NTF?
Os arquivos com extensão .ntf são chamados de Arquivos **National Transfer Format (NTF)**; usado principalmente pelo UK Ordnance Survey (OS); especificamente para a transferência de dados geoespaciais. É administrado pela British Standards Institution. Tornou-se o formato de transferência padrão para dados digitais do Ordnance Survey. A projeção National Grid do Reino Unido, que é um tipo de Transverse Mercator, contém todas as informações georreferenciadas para arquivos NTF.

## Formato de arquivo NTF
O formato de arquivo NTF é de propriedade da Ordnance Survey no Reino Unido; suportado pela biblioteca GDB para importação. A versão atual do formato de arquivo NTF é 2.0. Este formato de arquivo foi introduzido para resolver uma limitação do segmento vetorial **PCIDSK** que possui apenas um campo de atributo por estrutura, mas há uma variedade de atributos que podem ser extraídos com dados vetoriais. Para contornar o formato de arquivo NTF é constituído como tendo dois segmentos. Cada segmento consiste nos mesmos vetores, mas com atributos diferentes. O primeiro segmento de um arquivo vetorial NTF contém os vetores com o número do código de recurso como atributo. O segundo segmento contém os vetores com o valor como atributo.

### Sistema de referência de coordenadas
A biblioteca GDB representa dados raster e vetoriais com as características de projeção TM apropriadas:

- Longitude de referência: 49,0
- Latitude de referência: 2,0
- Falso Leste: 400000
- Falso Norte: -100000
- Escala: 0,9996012717
- Elipsóide: Airy 1830 (E009)
Não há suporte disponível para atualização ou gravação de arquivos NTF, nem os arquivos DTM podem ser vinculados.

### Exemplo Ogrinfo
O exemplo a seguir usa **ogrinfo** em um arquivo NTF para recuperar números de camada:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Referências

* [Formato de transferência nacional do Reino Unido (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Mapeamento da Web - ilustrado por Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustration/0596008651/re15.html)

