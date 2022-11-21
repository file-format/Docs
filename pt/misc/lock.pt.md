{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo de bloqueio - O que é um arquivo de bloqueio?",
  "description":"Saiba mais sobre o formato de arquivo LOCK e seu .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## O que é um arquivo LOCK?

Um arquivo **LOCK** é um arquivo renomeado usado por aplicativos e sistemas operacionais para marcar um arquivo ou algum dispositivo como bloqueado. Isso diz a outros aplicativos para não usar o arquivo, a menos que esteja livre do aplicativo que o está usando. Na maioria dos casos, esses arquivos de bloqueio estão vazios, mas em outros casos, eles podem conter informações relacionadas ao bloqueio, como propriedades e configurações.

Às vezes, o arquivo .lock é usado pelo .NET Framework da Microsoft para criar cópias **bloqueadas** de um arquivo de banco de dados. Nesse caso, uma cópia do arquivo de banco de dados será aberta com a extensão .lock. Isso não permite que o usuário faça alterações no arquivo enquanto ele estiver sendo usado por outro usuário.

## Formato de arquivo LOCK - Mais informações

Um arquivo LOCK é criado por cada aplicativo e seu formato de arquivo é específico para o aplicativo. Esses arquivos de bloqueio podem ser salvos em formato de arquivo de texto e binário.

A presença de arquivos de bloqueio impede o acesso simultâneo de um recurso a vários arquivos que tentam acessar esse recurso. Uma cópia do arquivo original é criada com a extensão .lock com sufixo em seu nome. Isso informa outros aplicativos para ter acesso somente leitura ao arquivo. Por exemplo, resource.dat se tornará resource.data.lock.

Para a linguagem de programação Ruby, você pode encontrar o arquivo **gemfile.lock**. É aqui que o Bundler mantém o registro das versões exatas que foram instaladas. Assim, quando um projeto/biblioteca é movido para outra máquina, o bundle em execução examinará o Gemfile para a versão exata e relevante.

## Bloquear arquivo no Linux

O Linux suporta dois tipos de bloqueios de arquivo: bloqueios consultivos e bloqueios obrigatórios.

* **Advisory Locks**: Tipo de bloqueio que não é aplicado. Nesse caso, os processos participantes cooperam entre si adquirindo bloqueios explicitamente. Se isso não for possível, os bloqueios consultivos serão ignorados.

* **Bloqueios obrigatórios**: No caso de bloqueio obrigatório, o sistema operacional impõe o bloqueio do arquivo impedindo que outros processos leiam ou gravem o arquivo. Isso não requer qualquer cooperação entre os processos.

o bloqueio obrigatório não requer qualquer cooperação entre os processos participantes. Depois que um bloqueio obrigatório é ativado em um arquivo, o sistema operacional impede que outros processos leiam ou gravem o arquivo.

## Referências

* [GemFile e Gemfile.lock em Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Bloqueando no Linux](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)

