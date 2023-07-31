{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo MDMP - Formato de arquivo Minidump do Windows",
  "description":"Saiba mais sobre o formato de arquivo MDMP e APIs que podem criar e abrir arquivos MDMP.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2022-08-19"
}

## O que é um arquivo MDMP?

Um arquivo MDMP é um despejo de memória de um aplicativo no Microsoft Windows que é criado quando o aplicativo fecha de forma anormal ou trava. Ele contém informações e despejos de dados que podem ser usados para depurar a causa da falha. Os arquivos MDMP são aplicáveis em aplicativos criados por qualquer plataforma, como Java, C++, .NET e outros. Além do MDMP,

Os aplicativos que podem abrir arquivos MDMP incluem o Microsoft Visual Studio Debugger.

## Formato de arquivo MDMP

Os arquivos MDMP são salvos como arquivos binários no disco e podem ser abertos com o depurador do Microsoft Visual Studio. Ele contém as seguintes informações para ajudar a identificar o motivo da falha.

* Detalhes da mensagem Stop, seus parâmetros e outros dados
* Lista de drivers carregados
* Contexto do processador (PRCB) para o processador que parou de funcionar
* Informações do processo e contexto do kernel (EPROCESS) para o processo que parou
* Informações do processo e contexto do kernel (ETHREAD) para o segmento que parou
* Pilha de chamadas do modo kernel para o thread que parou

Essas informações ajudam a descobrir o que aconteceu, corrigir o problema e evitar que ele aconteça novamente.

### Analisar Minidespejo

O Windows requer um arquivo de paginação no volume de inicialização para criar um arquivo de despejo de memória. O arquivo de paginação é criado no volume de inicialização e deve ter pelo menos 2 megabytes (MB) de tamanho. O arquivo de despejo é criado quando um aplicativo falha. No caso de um segundo problema, um segundo arquivo de despejo de memória pequeno é criado enquanto o anterior é mantido preservado. O nome do arquivo de despejo é distinto para evitar qualquer substituição.

O Windows mantém uma lista de todos os arquivos de despejo de memória na pasta %SystemRoot%\Minidump. Você pode analisar arquivos MDMP executando-os no Visual Studio Debugger conforme listado nas etapas abaixo.

## Como faço para abrir um arquivo MDMP no Visual Studio?

As etapas a seguir podem ser usadas para abrir um arquivo MDMP no Visual Studio.

* No Visual Studio, no menu Arquivo, escolha Abrir | Despejo de memória .
* Navegue até o arquivo de despejo que deseja abrir.
* Selecione Abrir.

## Referência

* [Como ler o pequeno arquivo de despejo de memória que é criado pelo Windows se ocorrer uma falha](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump -Arquivo)

