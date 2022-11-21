{
  "date" : "2021-03-18",
  "author" : {
    "display_name" : "Muhammad Umar",
	"keywords" :[ "QGD", "Banco de Dados SQLite do Projeto QGIS", "extensão", "formato", "QGIS", "Banco de Dados Auxiliar", "O que é um arquivo QGD"]
},
  "draft" : "false",
  "toc" : true,
  "title" :"QGD - Banco de Dados SQLite do Projeto QGIS",
  "description":"Aprenda sobre o QGD, que é um banco de dados sqlite do projeto QGIS e APIs que podem criar e abrir arquivos QGD.",
  "linktitle" : "QGD",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-03-18"
}

## O que é um arquivo QGD?

O arquivo com extensão .QGD é na verdade o banco de dados sqlite associado ao projeto **QGIS** que acomoda os dados auxiliares do projeto. O arquivo QGD permanecerá vazio, caso não haja dados auxiliares para o projeto.

## Detalhes sobre o formato de arquivo QGD

No modo clássico, o banco de dados auxiliar é salvo como um arquivo com extensão .qgd junto com o arquivo xml. O sistema **Auxiliary Database** permite ler e escrever dados no sistema de forma alternativa. Ao criar o QGZ que é um container compactado, o arquivo .qgd inclui no .qgz.

## O que é Banco de Dados Auxiliar?
O Banco de Dados Auxiliar é, na verdade, um sistema de banco de dados em espera que é criado como resposta à duplicação do banco de dados de destino. O banco de dados auxiliar é na verdade um caso de banco de dados duplicado seria o banco de dados para o qual você está duplicando. Por exemplo, se você configurar um banco de dados em espera usando banco de dados duplicado, o banco de dados de origem será o destino e o banco de dados em espera será conhecido como auxiliar.


## Referências

* [QGZ – Um novo formato de arquivo de projeto padrão para QGIS](https://oslandia.com/en/2018/06/01/qgz-a-new-default-project-file-format-for-qgis/)
* [Formatos de arquivo QGIS](https://docs.qgis.org/3.16/en/docs/user_manual/appendices/qgis_file_formats.html)

