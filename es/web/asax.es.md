{
  "date" : "2019-10-11",
  "keywords" :[ "asax","archivo asax", "formato de archivo asax", "tipo de archivo asax", "archivo", "tipo", "qué es un archivo asax"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASAX - Archivo de aplicación de servidor ASP.NET",
  "description" :"Aprenda a saber qué es un archivo ASAX y las API que pueden crear y abrir archivos ASAX",
  "linktitle" : "ASAX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-07"
}

## ¿Qué es un archivo ASAX?

Un archivo con extensión .asax es un archivo utilizado por las aplicaciones ASP.NET que reside en el lado del servidor. Contiene código para responder a eventos de nivel de aplicación y nivel de sesión generados por ASP.NET o por módulos HTTP. Esto también incluye el manejo de ciertos eventos cuando la aplicación se inicia o se cierra. Los archivos ASAX son opcionales y solo se agrega un único archivo ASAX a las aplicaciones web para manejar los eventos y errores de nivel de aplicación a nivel global. A diferencia de las páginas ASPX, los archivos ASAX no contienen ningún código para implementar la funcionalidad de la aplicación.

## Formato de archivo ASAX

Los archivos ASAX están escritos en formato de archivo de texto sin formato y son legibles por humanos. El archivo ASAX más utilizado es Global.asax que reside en el directorio raíz de una aplicación ASP.NET. Los servidores web están configurados para rechazar cualquier llamada entrante a este archivo para prohibir a los usuarios descargar o ver el código de este archivo.

### Global.ASAX - Un ejemplo de formato de archivo ASAX

Un solo archivo ASAX consta de varias secciones que se escriben para manejar los eventos de nivel de aplicación. Estos son los siguientes.

* **Directivas de aplicación**: las directivas de aplicación son etiquetas que se utilizan para definir configuraciones opcionales específicas de la aplicación que utilizará el analizador ASP.NET al procesar el archivo Global.asax. Estas directivas se encuentran al inicio del archivo Global.asax y se definen de la siguiente manera.

```
<%@ directiva atributo=valor [atributo=valor … ]%>
```
* **Bloques de declaración de código**: los bloques de declaración de código se utilizan para definir secciones de código de servidor que están incrustadas en archivos de aplicación ASP.NET dentro de \<script> blocks marked with a runat="server" attribute. The following example shows how you can define event-handling logic for the EnterBtn_Click event.

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
* **Bloques de procesamiento de código**: definen el código en línea o las expresiones que se ejecutan cuando se procesa la página. Los dos estilos de bloques de procesamiento de código incluyen código en línea y expresiones en línea. El primero se usa para definir líneas independientes o bloques de código, mientras que el lateral se usa como atajo para llamar al método Write.

## Referencias

* [Descripción general de controladores HTTP y módulos HTTP](https://msdn.microsoft.com/en-us/library/bb398986(v=vs.100))
* [Sintaxis global.asax](https://learn.microsoft.com/en-us/previous-versions/dotnet/netframework-4.0/2027ewzw(v=vs.100))

