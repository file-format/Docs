{
  "date" : "2021-08-24", 
  "keywords" :[ "vbs", "arquivo", "extensão", "formato de arquivo", "Script do Visual Basic", "Guia de programação", "exemplo de vbs", "Microsoft Visual Basic", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBS - Arquivo de script do Visual Basic",
  "description":"Saiba mais sobre o formato de arquivo VBS e APIs que podem criar e abrir arquivos VBS.",
  "linktitle" : "VBS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-08-24"
}

## O que é um arquivo VBS?

VBS ou VBScript está conectado com a edição de script do Microsoft Visual Basic. No ambiente de computação, o usuário tem permissão para acessar e controlar muitos aspectos dele. O VBScript tem permissão para usar um modelo chamado **Component Object Model** para aproveitar os elementos e ferramentas do ambiente. Este ambiente é especificado para trabalhar e executar o VBScript.

Funciona de forma semelhante ao Javascript quando é acessado pelo cliente na área de desenvolvimento Web. Também é usado pelos servidores para o processamento de páginas da web. Pode ser considerado em alguns outros tipos de arquivos de script, como aplicativos de [HTML](/pt/web/html/).


## Breve história ##

Foi lançado pela primeira vez em 1996, como parte das tecnologias usadas pela Microsoft especificadas para Windows Scripts. Ele foi desenvolvido especificamente para a ajuda de desenvolvedores da Web inicialmente. No mesmo ano, o explorador do Microsoft Windows chamado Internet Explorer foi lançado junto com os recursos do Visual Basic Script.

Com o progresso da tecnologia e desenvolvimento web, muitas versões do VBScript, juntamente com muitos recursos avançados, foram lançadas. Além disso, no próximo ano, essa linguagem de script fará parte do Microsoft Windows com novos recursos.

## Especificação Técnica ##

Para as páginas da Web no lado do servidor, as ferramentas como **Active Server Pages** são usadas junto com o VBScript. Essa linguagem de script também pode ser usada no componente de script do Windows. Os arquivos desta linguagem são armazenados com extensão .vbs no Windows.

Existem muitas estruturas de controle, como loops, que são usadas no código dessa linguagem. Ele também inclui argumentos que são de linha de comando e podem ser nomeados ou não. Os arquivos dessa linguagem podem ser armazenados simplesmente nas pastas ou na área de trabalho de um sistema operacional Windows. Embora não exista um ambiente de desenvolvimento integrado específico para VBScript, programas como o Microsoft Script Editor oferecem a facilidade de desenvolvimento desta linguagem.

Quando o VBScript é hospedado pelo host de scripts do Windows, ele fornece vários recursos que são bastante comuns às linguagens de script, mas não estão disponíveis no Visual Basic 6.0. Os recursos que envolvem acesso fácil ou direto envolvem impressoras de rede, argumentos de linha de comando não nomeados e nomeados, stdout e stdin, compartilhamentos de rede, instrumentação de gerenciamento do Windows, informações do usuário de redes como associação de grupo e muito mais.

## Exemplo de formato de arquivo VBS ##

```
<% Option Explicit %>
 <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
 <html>
 	<head>
 		<title>VBScript Example</title>
 	</head>
 	<body>
 		<div><% 
 			' Grab current time from Now() function.
 			' An '=' sign occurring after a context switch (<%) is shorthand 
 			' for a call to the Write() method of the Response object.
 			Dim timeValue : timeValue = Now %>
 			The time, in 24-hour format, is 
 			<%=Hour(timeValue)%>:<%=Minute(timeValue)%>:<%=Second(timeValue)%>.
 		</div>
 	</body>
 </html>
```

## Referência ##

* [VBS - pela Wikipedia](https://en.wikipedia.org/wiki/VBScript)



