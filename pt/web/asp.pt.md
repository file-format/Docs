{
  "date" : "2019-10-11",
  "keywords" :[ "asp", "arquivo asp", "formato de arquivo asp", "tipo de arquivo asp", "arquivo", "tipo", "o que é um arquivo asp" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASP - Formato de arquivo de páginas de servidor ativo",
  "description" :"Saiba mais sobre o que é um arquivo ASP e APIs que podem criá-los e abri-los.",
  "linktitle" : "ASP",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo ASP?

ASP significa Active Server Pages, que é uma estrutura de desenvolvimento para criar páginas da web. Ele permite que o código do computador seja executado por um servidor interno para atender às solicitações da web. Quando uma solicitação é gerada para um arquivo ASP pelo navegador da web, o servidor lê o arquivo e executa qualquer código/script dentro dele para gerar o resultado **[HTML](/pt/web/html/)** que é retornado ao navegador para exibição.

Ao contrário das páginas HTML, que são páginas estáticas servidas pelo servidor, os arquivos ASP geram conteúdos dinâmicos em tempo de execução que podem envolver solicitações de dados de um banco de dados. As páginas ASP normalmente usam a extensão .asp em vez de .html. Como o código/script dentro de um arquivo ASP é executado no lado do servidor, o navegador solicitante não pode ver o código usado para construir a página servida. Todos os navegadores modernos são capazes de exibir as páginas geradas como resultado. Sendo construídas com tecnologia Microsoft, as páginas criadas com ASP são hospedadas em servidores Microsoft Internet Information Services (IIS).

## Breve História do Formato de Arquivo ASP
O ASP passou por apenas algumas revisões até que foi substituído pelo ASP.NET, que é uma maneira mais moderna e eficiente de desenvolver e gerenciar páginas do lado do servidor. O suporte para ASP está incluído por padrão junto com os Serviços de Informações da Internet (IIS). ASP foi publicado em três versões diferentes com melhorias em cada uma.

* ASP 1.0 foi lançado em dezembro de 1996 como parte do IIS 3.0
* ASP 2.0 foi lançado em setembro de 1997 como parte do IIS 4.0
* ASP 3.0 foi lançado em novembro de 2000 como parte do IIS 5.0

## Objetos funcionais ASP

Os arquivos ASP usam objetos do lado do servidor para processar solicitações de usuários e gerar páginas de saída a serem fornecidas aos usuários. Cada objeto possui um conjunto de coleções, propriedades e métodos para processar solicitações e respostas. Esses objetos incluem:

### Objeto de solicitação

Quando um navegador solicita uma página de um servidor, isso é chamado de solicitação. O objeto Request é usado para obter informações de um visitante.

### Objeto de resposta

O objeto ASP Response é usado para enviar saída para o usuário do servidor.

### Objeto de servidor

O objeto ASP Server é usado para acessar propriedades e métodos no servidor. Permite conexões com bancos de dados (ADO), sistema de arquivos e uso de componentes instalados no servidor.

### Objeto de sessão

Um objeto de sessão é como um link entre o navegador do usuário solicitando uma página do servidor e o próprio servidor. Isso é obtido por um cookie criado pelo ASP e enviado ao computador do usuário. O objeto Session armazena informações ou altera as configurações de uma sessão de usuário. As informações armazenadas em um objeto Session são compartilhadas em todas as páginas de um aplicativo. Informações comuns armazenadas em variáveis de sessão são nome, id e preferências. O servidor cria um novo objeto Session para cada novo usuário e destrói o objeto Session quando a sessão expira.

### Objeto de aplicativo

O objeto Application contém informações que serão usadas por muitas páginas no aplicativo (como informações de conexão do banco de dados). As informações podem ser acessadas de qualquer página. As informações também podem ser alteradas em um só lugar, e as alterações serão refletidas automaticamente em todas as páginas. O objeto Application é usado para armazenar e acessar variáveis de qualquer página, assim como o objeto Session.

### Objeto ASPError

O objeto ASPError foi implementado no ASP 3.0 e está disponível no IIS5 e versões posteriores. O objeto ASPError é usado para exibir informações detalhadas de qualquer erro que ocorra em scripts em uma página ASP.

**Observação:** O objeto ASPError é criado quando Server.GetLastError é chamado, portanto, as informações de erro só podem ser acessadas usando o método Server.GetLastError.

## Referências

* [ASP - Por W3C](https://www.w3schools.com/asp/default.asp)
* [Criando páginas ASP simples](https://learn.microsoft.com/en-us/previous-versions/iis/6.0-sdk/ms524741(v=vs.90))

