{
  "date" : "2021-07-15",
  "keywords" :[ "LNK", "extensão", "arquivo", "formato", "sistema", "arquivo LNK", "link", "arquivos LNK", "documentos LNK", "aplicativo", "programas" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LNK - Formato de arquivo de link",
  "description":"Saiba mais sobre o formato de arquivo LNK e APIs que podem criar e abrir arquivos LNK.",
  "linktitle" : "LNK",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## O que é um arquivo LNK? ##

Um arquivo LNK, análogo a uma identidade no sistema Mac, é uma alternativa ou "link" do Windows que serve como uma conexão com uma pasta ou programa de documento de imagem original. Ele contém o tipo, a posição e o nome do arquivo do destino do atalho, bem como o aplicativo que abre o documento de destino e uma tecla de atalho adicional.

No Windows, direcione um arquivo, pasta ou programa executável e escolha Criar atalho. A localização do formato do arquivo e o diretório “Início” são dois recursos básicos dos arquivos LNK. O formato de arquivo dos arquivos LNK é mascarado e uma seta curva indica que são atalhos.

## Formato de arquivo LNK ##

Os formatos de arquivo LNK geralmente têm o mesmo ícone que seus arquivos de destino, mas com a adição de uma pequena seta curvada para mostrar que o arquivo aponta para um local diferente. Quando o atalho é clicado duas vezes, ele se comporta como se o usuário tivesse clicado duas vezes no arquivo real.

Os arquivos LNK que contêm atalhos de aplicativos podem ter propriedades que afetam a execução do programa. Para alterar os atributos, clique com o botão direito do mouse no arquivo de atalho e escolha **Propriedades** e altere o campo Destino.

Em vez de serem extensões de arquivo, os arquivos LNK são extensões do Windows Explorer. Como extensão de terminal, os documentos .lnk só podem ser usados no Windows Explorer para substituir um arquivo, e têm outras finalidades no Windows Explorer além de servir como atalho para um documento local. Esses arquivos também começam com a letra "L".

Embora os atalhos sejam vinculados a arquivos e diretórios específicos quando são criados, eles podem se tornar inoperantes se o destino for alterado para um local diferente. O Explorer começará a reparar uma pasta de atalho que aponta para um alvo morto quando for aberta.


## Especificação Técnica ##

Somente quando a configuração de exibição de pasta "Ocultar extensões para tipos de arquivo reconhecidos" está desmarcada, o Windows não mostra a extensão de documento .lnk para atalhos de documento. Embora não seja recomendado, você pode habilitar a extensão do arquivo a ser exibida removendo a propriedade "NeverShowExt" do item de registro do Windows do arquivo HKEY_CLASSES_ROOT\lnk.

Para isso, siga estes passos:

* Abra o "Editor de Registro" digitando "Regedit" no campo de pesquisa da barra de tarefas e escolhendo o programa
* No aplicativo, navegue até o local Computer\HKEY HKEY_CLASSES_ROOT\lnkfile
* Faça um backup do item clicando com o botão direito do mouse e escolhendo Exportar
* Selecione e exclua o atributo "NeverShowExt"
* O Windows deve ser reiniciado


## Referência ##

* [LNK - Wikipedia](https://en.m.wikipedia.org/wiki/Shortcut_(computing))
