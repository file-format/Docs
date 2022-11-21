{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "arquivo vdw", "formato de arquivo vdw", "tipo de arquivo vdw", "arquivo", "tipo", "o que é um arquivo vdw" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - Formato de arquivo do serviço gráfico do Visio",
  "description":"Saiba mais sobre o formato de arquivo VDW e APIs que podem criar e abrir arquivos VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}
## O que é um arquivo VDW?
VDW é o formato de arquivo do Visio Graphics Service que especifica os fluxos e armazenamentos necessários para renderizar um desenho da Web. Um desenho da web é uma coleção de páginas de desenho, formas, fontes, imagens, conexões de dados e informações de atualização de diagrama que podem ser renderizadas como um desenho vetorial ou raster. Os arquivos VDW também podem ser abertos no Microsoft Visio, mas são salvos principalmente para uso na web. O Microsoft Visio oferece a capacidade de converter arquivos do Visio em vários formatos de arquivo diferentes, incluindo [PNG](/pt/Image/PNG/), [BMP](/pt/Image/BMP/), [PDF](/pt/pdf/) e outros.

## **VDW** Formato de arquivo #

As especificações técnicas do formato de arquivo VDW estão disponíveis online pela [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) e podem ser referenciadas pelos desenvolvedores para criar formulários. O documento técnico descreve os dados contidos em um arquivo composto que contém armazenamentos e fluxos. A representação de um Web Drawing é possível através de um stream, denominado VisioServerData, através de um arquivo ZIP. Uma ShapGraphic XML Part no arquivo descreve os elementos gráficos exibidos no desenho da Web e são expressos em Extensible Application Markup Language (XAML). Uma coleção de partes XML no arquivo ZIP descreve a conexão de dados do desenho da Web, informações sobre sua forma e a lógica de atualização do diagrama. Essas partes são expressas como XML. A parte XML DataGraphic descreve as propriedades recalculadas que devem ser avaliadas depois que os dados no desenho da Web forem atualizados da fonte de dados. Itens adicionais no arquivo ZIP contêm informações sobre as fontes e imagens usadas no desenho da Web.

|![Possível implementação de um arquivo](/pt/web/vdw.png "Possível implementação de um arquivo")

## Referências ##

* [[MS-VGSFF]: formato de arquivo do Visio Graphics Service (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

