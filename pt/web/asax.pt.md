{
  "date" : "2019-10-11",
  "keywords" :[ "asax", "arquivo asax", "formato de arquivo asax", "tipo de arquivo asax", "arquivo", "tipo", "o que é um arquivo asax" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - Arquivo de aplicativo do servidor ASP.NET",
  "description" :"Aprenda a saber o que é um arquivo ASAX e APIs que podem criar e abrir arquivos ASAX.",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## O que é um arquivo ASAX?

Um arquivo com extensão .asax é um arquivo usado por aplicativos ASP.NET que reside no lado do servidor. Ele contém código para responder a eventos de nível de aplicativo e de sessão gerados pelo ASP.NET ou por módulos HTTP. Isso também inclui o tratamento de determinados eventos quando o aplicativo é iniciado ou encerrado. Os arquivos ASAX são opcionais e apenas um único arquivo ASAX é adicionado aos aplicativos da Web para lidar com os eventos e erros no nível do aplicativo no nível global. Ao contrário das páginas ASPX, os arquivos ASAX não contêm nenhum código para implementar a funcionalidade do aplicativo.

## Formato de arquivo ASAX

Os arquivos ASAX são escritos em formato de arquivo de texto simples e são legíveis por humanos. O arquivo ASAX mais comumente usado é o Global.asax que reside no diretório raiz de um aplicativo ASP.NET. Servidores da Web são configurados para rejeitar quaisquer chamadas recebidas para este arquivo para proibir os usuários de baixar ou visualizar o código deste arquivo.

### Global.ASAX - Um exemplo de formato de arquivo ASAX

Um único arquivo ASAX consiste em várias seções que são escritas para lidar com os eventos no nível do aplicativo. Estes são os seguintes.

* **Diretivas de aplicativo** - Diretivas de aplicativo são marcas usadas para definir configurações opcionais específicas do aplicativo a serem usadas pelo analisador ASP.NET ao processar o arquivo Global.asax. Essas diretivas estão localizadas no início do arquivo Global.asax e são definidas a seguir.

```
<%@ diretiva atributo=valor [atributo=valor … ]%>
```
* **Blocos de declaração de código** - Os blocos de declaração de código são usados para definir seções de código do servidor que são incorporadas em arquivos de aplicativo ASP.NET dentro do \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

```
<html>
  <script language="C#" runat="server">
      void EnterBtn_Click(Object Src, EventArgs E) {
          Message.Text = "Hi " + Name.Text + ", welcome to ASP.NET!";
  }
  </script>

  <body>
   <form runat="server">
    Enter your name: <asp:textbox id="Name" runat=server/>
                     <asp:button text="Enter" Onclick="EnterBtn_Click" runat="server"/>
        <p>
        <asp:label id="Message" runat=server/>
    </form>
  </body>
</html>
```
* **Blocos de renderização de código** - definem o código embutido ou as expressões que são executadas quando a página é renderizada. Os dois estilos de blocos de renderização de código incluem código embutido e expressões em linha. O primeiro é usado para definir linhas ou blocos de código independentes, enquanto o lateral é usado como um atalho para chamar o método Write.

## Referências

* [Visão geral de manipuladores HTTP e módulos HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Sintaxe Global.asax](https://docs.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

