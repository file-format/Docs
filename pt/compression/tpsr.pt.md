{
  "date" : "2022-06-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo TPSR - Arquivo de relatório de sessão piloto do TeamViewer",
  "description":"Saiba mais sobre o formato de arquivo TPSR e APIs que podem criar e abrir arquivos TPSR.",
  "linktitle" : "TPSR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-06"
}

## O que é um arquivo TPSR?

Um TPSR é um arquivo de protocolo de conexão usado pelo TeamViewer Assist AR (anteriormente conhecido como TeamViewer Pilot). As informações armazenadas em um arquivo TPSR são armazenadas no formato de arquivo compactado [ZIP](/pt/compression/zip/). O TPSR contém um histórico detalhado da conexão do TeamViewer entre um especialista e um técnico para resolver problemas e fins de revisão. As informações contidas em um arquivo TPSR incluem tipo de dispositivo, nome, Assist AR ID, Expert ID, data e hora e duração da conexão. Esses dados são armazenados em um arquivo [JSON](/pt/web/json/) dentro do arquivo TPSR compactado.

## Formato de arquivo TPSR

Um arquivo TPSR é armazenado em disco no formato de arquivo ZIP, onde o conteúdo é armazenado dentro de um arquivo JSON. Ele é gerado automaticamente após a conclusão da conexão Assist AR, desde que a opção de relatório Connetion esteja habilitada no TeamViewer.

O TeamViewer Assist AR permite que os especialistas se conectem aos técnicos para obter um feed AO VIVO da extremidade remota por meio da câmera móvel. Eles podem ajudar os técnicos a resolver o problema por telefone.

## Abrir arquivos TPSR

Você pode abrir arquivos TPSR usando a versão desktop do software TeamViewer. Se instalado em seu computador, clicar duas vezes no arquivo TPSR o abrirá no software TeamViewer. Os arquivos TPSR também podem ser exportados para arquivos [PDF](/pt/pdf/) ou podem ser impressos para obter uma cópia impressa do arquivo de protocolo.

## Referências ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)

