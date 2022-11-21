{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "arquivo", "formato", "extensão", "API", "Conjunto de folhas do AutoCAD" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - Arquivo de conjunto de folhas do AutoCAD",
  "description" :"Saiba mais sobre o arquivo .dst e as APIs que podem criar e abrir arquivos DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## O que é um arquivo DST?

Um arquivo DST é um arquivo AutoCAD que contém associações e informações para definir conjuntos de folhas. Eles são armazenados na pasta de armazenamento de conjunto de folhas padrão, Conjuntos de folhas do AutoCAD. Os arquivos DST não contêm os layouts de desenho reais, mas referem-se a eles dos arquivos selecionados [DWG](/pt/cad/dwg/) e [DWT](/pt/cad/dwt/) associados a esses conjuntos de folhas. Em ambiente de rede, todos os membros da equipe devem ter acesso à rede a esses arquivos associados. Os arquivos DST são salvos no disco no formato de arquivo [XML](/pt/web/xml/).

## Formato de arquivo DST - Mais informações

Os arquivos DST são criados com a ferramenta AutoDesk Sheet Set Manager (SSM). Quando um arquivo é acessado por alguém da equipe, o arquivo DST é aberto brevemente e depois armazenado de volta com as informações atualizadas. O acesso simultâneo ao mesmo arquivo DST é gerenciado pela ferramenta SSM que mostra um ícone de cadeado quando o arquivo está em acesso.

Em qualquer momento específico, o status da planilha pode estar em qualquer um dos seguintes estados.

* A planilha está disponível para edição.
* A folha está bloqueada.
* A planilha está ausente ou foi encontrada em um local de pasta inesperado.

## Referências

* [Sobre o uso de conjuntos de folhas de horário de verão](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-577D8EA0-85F2 -4829-B4F9-8CAD6F7AAACC-htm.html)
* [Saiba mais sobre conjuntos de folhas](https://knowledge.autodesk.com/support/autocad-lt/learn-explore/caas/CloudHelp/cloudhelp/2017/ENU/AutoCAD-LT/files/GUID-34D889BC-19AD- 4CD1-ADB1-F359D9B515FB-htm.html)
* [Dominando conjuntos de folhas do AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

