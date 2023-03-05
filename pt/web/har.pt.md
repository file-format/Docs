{
  "date" : "2021-07-08",
  "keywords" :["HAR", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "JSON", "Arquivo de arquivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HAR - Formato de arquivo de arquivo HTTP",
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo HAR e APIs que podem criar e abrir um arquivo HAR.",
  "linktitle" : "HAR",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-08"
}

## O que é um arquivo HAR?

Um arquivo com arquivo .har ([HTTP](/pt/web/http/) Archive) é um arquivo HTTP que armazena dados de sessão transferidos por vários navegadores (como Chrome, Safari, IE, Firefox etc.) em [JSON](/pt/web/json/) formato de arquivo. Os dados transferidos pela internet entre o servidor e o cliente (neste caso o navegador do usuário) contêm cabeçalhos de solicitação e resposta HTTP que são armazenados no arquivo HAR. Ele também contém informações detalhadas sobre dados de desempenho sobre páginas da Web carregadas no navegador. Os arquivos HAR podem ser abertos em qualquer editor de texto, como o Bloco de Notas no sistema operacional Microsoft Windows e o TextEdit no Apple MacOS.

## Formato de arquivo HAR - Mais informações

Os arquivos HAR armazenam informações da sessão em arquivo de texto simples usando o popular formato JSON. As especificações para o formato de arquivo HAR foram produzidas pelo Web Performance Group do World Web Consortium (W3C), mas não puderam ser publicadas. No entanto, ele definiu com sucesso um formato de arquivamento para transações HTTP.

Além de monitorar a transferência de informações de solicitação e resposta, os arquivos HAR são usados pelos desenvolvedores para registrar o desempenho do navegador da Web em termos de velocidade de carregamento da página, duração do carregamento do conteúdo, conteúdo carregado, consultas executadas para obter a resposta do navegador e muitos outros .

## Por que usar arquivos HAR?

Os arquivos HAR podem ser úteis para melhorar o desempenho de um site, avaliando longos tempos de carregamento, tempos de renderização de página e tempos de resposta. Os arquivos HAR podem ser analisados para encontrar esses problemas e resolver quaisquer problemas com o site para melhorar o desempenho.

## Como gerar o arquivo HAR?

Então, como gerar um arquivo HAR? Bem, isso depende do tipo de navegador que você está usando para gerar um arquivo HAR. Neste guia, listamos as etapas para o navegador Google Chrome. Métodos para gerar arquivos HAR usando Safari, Firefox, etc. podem ser facilmente pesquisados na internet e seguidos.

### Etapas para gerar o arquivo HAR usando o Google Chrome

As etapas a seguir podem ser executadas em uma página da Web onde os problemas estão sendo enfrentados.

1. Abra a página da web no Google Chrome onde ocorreu o problema.
1. Abra a ferramenta do desenvolvedor (inspecione o elemento).
1. Vá para a esquerda do painel para iniciar a gravação do arquivo. Há um pequeno botão redondo vermelho nesta seção.
1. Clique no ícone "Limpar" para excluir quaisquer registros de log mantidos no navegador.
1. Para salvar o conteúdo desejado conforme mostrado acima, clique com o botão direito e clique em “Salvar como arquivo HAR”

## Referências

* [Formato de arquivo HAR - Wikipedia](https://en.wikipedia.org/wiki/HAR_(file_format))

