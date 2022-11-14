{
  "date" : "2019-10-11",
  "keywords" :[ "aspx","archivo aspx", "formato de archivo aspx", "tipo de archivo aspx", "archivo", "tipo", "qué es un archivo aspx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de archivo ASPX",
  "description" :"Su guía de formato de archivo para aprender qué es un archivo ASPX y las API que pueden crear y abrir archivos ASPX",
  "linktitle" : "ASPX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## ¿Qué es un archivo ASPX?

Un archivo con extensión .aspx es una página web generada utilizando el marco Microsoft ASP.NET que se ejecuta en servidores web. ASPX significa Active Server Pages Extended y estas páginas se muestran en el navegador web en el extremo del usuario cuando se accede a la URL. Es sucesor de la tecnología [ASP](/es/web/asp/) que también se genera en el extremo del servidor pero no utiliza .NET Framework. Las páginas ASP.NET pueden contener scripts [C#](/es/programming/cs/) o [VB.NET](/es/programming/vb/) que el servidor web traduce a HTML para presentarlos al usuario en el navegador web. Las páginas ASPX también se denominan formularios web .NET. Estos pueden abrirse y crearse con aplicaciones como Microsoft Visual Studio, Adobe Dreamweaver, Notepad++ y cualquier editor de texto.

## Formato de archivo ASPX

Los formularios web de ASP.NET se basan en el modelo basado en eventos para las interacciones con la aplicación web. El navegador, al ser un usuario final, envía un formulario web al servidor y el servidor devuelve una página de marcado completa o una página HTML como respuesta. El modelo de componentes ASP.NET ofrece un modelo de objetos para páginas ASPX. Este modelo describe:

* Contrapartes del lado del servidor de casi todos los elementos o etiquetas HTML, como \<form> y \<input> .
* Controles del servidor, que ayudan a desarrollar una interfaz de usuario compleja. Por ejemplo, el control Calendar o el control Gridview.

Los archivos ASPX usan el **modelo de código subyacente** de ASP.NET para la construcción de estas páginas.

### Código en línea

Código de muestra que está incrustado en línea en la página ASPX y proporciona toda la funcionalidad para la implementación del usuario. El siguiente código [C#](/es/programming/cs/) representa una página ASP.NET de muestra que incluye código en línea:

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

### Código detrás

El código se puede escribir y almacenar en archivos de clase separados para una separación clara de HTML de la lógica de presentación. Esto hace que la capa de presentación sea independiente del código ejecutable. El siguiente es el código subyacente para la presentación al usuario.

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

La implementación en C# de la lógica real para la capa de presentación es la siguiente.

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

## Referencias

* [ASP.NET WebApps - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/webapps/welcome-webapps)

