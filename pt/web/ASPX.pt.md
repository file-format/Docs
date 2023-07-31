{
  "date" : "2019-10-11",
  "keywords" :[ "aspx", "arquivo aspx", "formato de arquivo aspx", "tipo de arquivo aspx", "arquivo", "tipo", "o que é um arquivo aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo ASPX",
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo ASPX e APIs que podem criar e abrir arquivos ASPX.",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo ASPX?

Um arquivo com extensão .aspx é uma página da Web gerada usando o Microsoft ASP.NET framework executado em servidores da Web. ASPX significa Active Server Pages Extended e essas páginas são exibidas no navegador da Web no final do usuário quando a URL é acessada. É o sucessor da tecnologia [ASP](/pt/web/asp/) que também é gerada no servidor mas não usa o framework .NET. As páginas ASP.NET podem conter scripts [C#](/pt/programming/cs/) ou [VB.NET](/pt/programming/vb/) que são traduzidos para HTML pelo servidor web para apresentação ao usuário no navegador web. As páginas ASPX também são chamadas de .NET Web Forms. Eles podem ser abertos e criados com aplicativos como Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ e qualquer editor de texto.

## Formato de arquivo ASPX

Os formulários da Web do ASP.NET são baseados no modelo orientado a eventos para interações com o aplicativo da Web. O navegador, sendo um usuário final, envia um formulário da web ao servidor e o servidor retorna uma página de marcação completa ou uma página HTML em resposta. O modelo de componente ASP.NET oferece modelo de objeto para páginas ASPX. Este modelo descreve:

* Contrapartes do lado do servidor de quase todos os elementos ou tags HTML, como \<form> e \<input> .
* Controles de servidor, que ajudam no desenvolvimento de interface de usuário complexa. Por exemplo, o controle Calendar ou o controle Gridview.

Os arquivos ASPX usam o **modelo Code Behind** do ASP.NET para a construção dessas páginas.

### Código em linha

Código de exemplo que é incorporado em linha na página ASPX e fornece toda a funcionalidade para a implementação do usuário. O seguinte código [C#](/pt/programming/cs/) representa uma página ASP.NET de exemplo que inclui código em linha:

```
<%@ Language=C# %>
<HTML>
    <script runat="server" language="C#">
        void MyButton_OnClick(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextbox.Text.ToString();
    }
    </script>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextbox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" OnClick="MyButton_OnClick" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server"></asp:label>
        </form>
    </body>
</HTML>
```

### Código por trás

O código pode ser escrito e armazenado em arquivos de classe separados para uma separação limpa do HTML da lógica de apresentação. Isso torna a camada de apresentação independente do código executável. A seguir está o code-behind para apresentação ao usuário.

```
<%@ Language="C#" Inherits="MyStuff.MyClass" %>
<HTML>
    <body>
        <form id="MyForm" runat="server">
            <asp:textbox id="MyTextBox" text="Hello World" runat="server"></asp:textbox>
            <asp:button id="MyButton" text="Echo Input" Onclick="MyButton_Click" runat="server"></asp:button>
            <asp:label id="MyLabel" runat="server" />
        </form>
    </body>
</HTML>
```

A implementação C# da lógica real para a camada de apresentação é a seguinte.

```
using System;
using System.Web;
using System.Web.UI;
using System.Web.UI.WebControls;

namespace MyStuff
{
    public class MyClass : Page
    {
        protected System.Web.UI.WebControls.Label MyLabel;
        protected System.Web.UI.WebControls.Button MyButton;
        protected System.Web.UI.WebControls.TextBox MyTextBox;

        public void MyButton_Click(Object sender, EventArgs e)
        {
            MyLabel.Text = MyTextBox.Text.ToString();
    }
}
}
```

## Referências

* [ASP.NET WebApps - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

