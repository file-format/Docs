{
  "date" : "2023-12-13",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo EAZ - O que é um arquivo EAZ e como abri-lo?",
  "description":"Aprenda sobre o formato de arquivo EAZ e APIs que podem criar e abrir arquivos EAZ.",
  "linktitle" : "EAZ",
  "menu" : {
    "docs" : {
      "parent" : "plugin",
      "identifier":"plugin-en-ea-ptz"
}
},
  "lastmod" : "2023-12-23"
}

## O que é um arquivo .EAZ?

O arquivo EAZ é um arquivo complementar utilizado pelo ArcGIS Explorer, um aplicativo gratuito desenvolvido pela ESRI para exploração, visualização e compartilhamento de mapas. Ele contém um arquivo compactado que inclui um [XML file](/web/xml/), código compilado e arquivos de suporte necessários para o suplemento. Esses arquivos são empregados para expandir a funcionalidade básica do software, incorporando novos botões, janelas encaixáveis e outras extensões.

## Formato de arquivo EAZ - Mais informações

Os arquivos EAZ são criados através da utilização do ArcGIS Explorer SDK, um kit de desenvolvimento projetado para criar funcionalidades personalizadas no ArcGIS Explorer. Esses arquivos utilizam compactação [ZIP](/compression/zip/) para empacotar seu conteúdo com eficiência. No núcleo do arquivo, o arquivo **Addins.xml** reside no diretório raiz, servindo como um componente vital que descreve e detalha as diversas personalizações incorporadas no arquivo EAZ.

O arquivo Addins.xml atua essencialmente como um roteiro, oferecendo insights sobre melhorias, modificações e extensões específicas que o arquivo EAZ introduz no ArcGIS Explorer. Através desta estrutura abrangente, os desenvolvedores podem encapsular e integrar perfeitamente novos recursos, botões e janelas encaixáveis, melhorando a funcionalidade geral e a experiência do usuário do aplicativo ArcGIS Explorer.

## Referências

 * [Sharing and installing add-ins](https://desktop.arcgis.com/en/arcmap/latest/analyze/python-addins/sharing-and-installing-add-ins.htm)
