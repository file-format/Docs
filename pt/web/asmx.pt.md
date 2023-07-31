{
  "date" : "2019-10-11",
  "keywords" :[ "asmx", "arquivo asmx", "formato de arquivo asmx", "tipo de arquivo asmx", "arquivo", "tipo", "o que é um arquivo asmx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASMX - Arquivo de serviço da Web ASP.NET",
  "description" :"Saiba mais sobre o que é um arquivo ASMX e APIs que podem criar e abrir arquivos ASMX.",
  "linktitle" : "ASMX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-10"
}

## O que é um arquivo ASMX?

Um arquivo com extensões .asmx é um arquivo ASP.NET Web Service que fornece comunicação entre dois objetos pela Internet usando o Simple Object Access Protocol (SOAP). Ele é implantado como um serviço no servidor Web baseado em Windows para processar a solicitação de entrada e retornar a resposta. Ao contrário dos arquivos [ASPX](/pt/web/aspx/) que contêm o código para exibição visual de páginas da Web ASP.NET, os arquivos ASMX são executados no servidor em segundo plano e realizam diferentes tarefas, como conectar-se ao banco de dados, recuperar dados e retorná-los em um formato em que o pedido foi feito. Estes são usados especificamente para serviços web XML.

## Formato de arquivo ASMX

Os arquivos ASMX estão em formato de texto simples e podem ser abertos ou editados em aplicativos como o Microsoft Visual Studio ou editores de texto. É um formato de arquivo proprietário da Microsoft e possui uma sintaxe bem definida para criação de serviços web. Uma resposta de um arquivo ASMX na forma de SOAP XML possui os seguintes elementos.

* `Envelop` - Um elemento raiz que identifica o documento XML como uma mensagem SOAP.
* `Header` - Um elemento opcional que contém informações específicas do aplicativo, como dados de autenticação. Se o elemento Header estiver presente, ele deve ser o primeiro elemento filho do elemento Envelope.
* `Body` - Contém a mensagem SOAP destinada ao destinatário.
* `Fault` - Um elemento opcional que é usado para indicar mensagens de erro. Se o elemento Fault estiver presente, ele deve ser um elemento filho do elemento Body.

Os arquivos ASMX podem ser escritos em linguagens .NET como [C#](/pt/programming/cs/), [Visual Basic](/pt/programming/vb/) ou JScript.

## Como o ASMX é diferente do ASPX e do ASCX?

Os arquivos ASMX são diferentes dos arquivos ASPX e ASCX.

* ASPX, Active Server Pages, arquivos são arquivos de programação que são gerados usando o Microsoft ASP.NET framework rodando em servidores web. Eles são renderizados no navegador da web do cliente quando o usuário solicita o acesso a tal página.
* ASCX, Active Server User Control, define controles de usuário que são usados para definir controles reutilizáveis em páginas da Web ASP.NET ou em todo o site.

## Referências

* [Consumindo o serviço ASMX](https://learn.microsoft.com/en-us/xamarin/xamarin-forms/data-cloud/web-services/asmx)
* [Controle de usuário ASCX](https://beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

