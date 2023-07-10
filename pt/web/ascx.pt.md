{
  "date" : "2019-10-11",
  "keywords" :[ "ascx", "arquivo ascx", "formato de arquivo ascx", "tipo de arquivo ascx", "arquivo", "tipo", "o que é um arquivo ascx" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo ASCX",
  "description" :"Saiba mais sobre o que é um arquivo ASCX e APIs que podem criar e abrir arquivos ASCX.",
  "linktitle" : "ASCX",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo ASCX?

Um arquivo com extensão .ascx é um controle de usuário usado como um componente reutilizável em páginas da Web. Ele é referenciado em qualquer site ASP arrastando-o da caixa de controle para a página. Os controles de usuários ASCX são adicionados ao projeto como uma fonte central, resultando em qualquer alteração no controle de usuário a ser refletida em todo o site. Ao contrário dos arquivos ASMX que definem um mecanismo para se comunicar em 2 objetos pela Internet, os arquivos ASCX são controles de usuário para incorporação em páginas ou site.

## Formato de arquivo ASCX

Os arquivos ASCX são escritos em formato de texto simples e podem usar código por trás de recursos como páginas da Web que terminam com .ascx.cs. O código de marcação de controles de usuário começa com a diretiva @Control, conforme mostrado no exemplo a seguir.

```
<%@ Control Language="VB" AutoEventWireup="false" CodeFile="WebUserControl.ascx.vb" Inherits="WebUserControl" %>
<p>A simple web user control with static HTML only.</p>
```

Este controle de usuário da web pode ser reutilizado em muitas páginas, como rodapé de página, cabeçalho ou algum tipo de navegação no site. Os controles de usuário da Web têm propriedades, métodos e eventos como qualquer outro controle que os tornam úteis para definir seu comportamento visual.

### Exemplo de registro de controles de usuário em web.config

Para usar um controle de usuário único em muitas páginas, o controle da web pode ser registrado em web.config. Isso permite usar o controle sobre todo o site em vez de se registrar em cada página individualmente. O código de exemplo a seguir define como registrar um controle da Web em web.config para ser exibido como rodapé em todo o site.

```
<configuration>
  <system.web>
    <pages>
      <controls>
        <add src="Footer.ascx" tagPrefix="bs" tagName="footer" />
      </controls >
    </pages >
  </system.web>
</configuration>
```
## Referências

* [ASCX vs ASMX](https://social.msdn.microsoft.com/Forums/en-US/a27d4c2f-b972-439e-a7fe-f4b7e3637700/how-to-work-with-ascx-files?forum=aspwebforms)
* [Controle de usuário ASCX](http://www.beansoftware.com/ASP.NET-Tutorials/User-Control.aspx)

