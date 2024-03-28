{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "extensão", "arquivo", "formato", "sistema", "Cold Fusion Markup Language", "idioma", "páginas da Web CFM", "mecanismo CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Marcação de fusão a frio",
  "description":"Saiba mais sobre o formato de arquivo CFM e APIs que podem criar e abrir arquivos CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## O que é um arquivo CFM? ##

As páginas e arquivos da Web usados na **Cold Fusion Markup Language** contêm extensões do CFM e são chamadas de páginas da Web CFM. Essa linguagem de script de desenvolvimento da Web é executada no Google App Engine, estrutura .NET e JVM. Pode conter uma linguagem de programação ou código da linguagem. Quando qualquer uma de suas páginas é acessada pelo usuário, o servidor web do ColdFusion a executa. CFScript (que é próximo ao JavaScript) ou tags podem ser usadas para escrever CFML. CFML pode ser usado para gerar outras linguagens além de [HTML](/pt/web/html/) como [CSS](/pt/web/css/), [JavaScript](/pt/web/js/), [XML](/pt/web/xml/) e muito mais.

O uso desta linguagem e tags que ela suporta é principalmente no desenvolvimento de aplicações web dinâmicas. Os arquivos podem ser executados diretamente no navegador online caso ocorra algum erro durante o uso offline da plataforma de desenvolvimento da aplicação.
 

O CFML funciona de forma que extensões de arquivo de servidor específicas (.cfc, .cfm) são fornecidas para processamento no mecanismo CFML. Se os mecanismos são baseados em Java, isso é obtido usando servlets Java. O mecanismo do CFML processa apenas funções e tags e retorna funções e texto fora das tags CFML para o servidor web sem nenhuma alteração.


## Breve história ##

Em 1995, foi criado pela primeira vez por uma corporação chamada Allaire. Em 2005 a Adobe a adquiriu e ainda hoje presta serviços para o desenvolvimento do ColdFusion. Com o passar dos anos, foi desenvolvido e atualizado por muitas pessoas e empresas. Em 2012, uma fundação chamada OpenCFML foi lançada. Mais tarde, em 2015, o ex-Ralo prestou os seus serviços para melhorar o desempenho do CFM e diminuiu os recursos para uma melhor funcionalidade. A atualização mais recente foi lançada em 2020, e está anunciada para continuar até 2028.

## Formato de arquivo CFM ##

O código dos arquivos CFM e páginas da web compreende principalmente as tags como HTML, mas com uma pequena diferença. Esses arquivos são responsáveis por executar várias operações que os scripts do ColdFusion permitem executar.
* Esses arquivos podem ser acessados e executados diretamente no Windows e no macOS usando o navegador de qualquer sistema operacional.
* Adobe ColdFusion fornece a plataforma para o desenvolvimento de páginas da web e aplicativos dinâmicos no PC.
* Qualquer editor de texto como o Bloco de Notas ou qualquer outro editor de texto em um sistema operacional pode ser usado para abrir esses arquivos, pois esses arquivos são baseados em texto.
* Quando qualquer arquivo CFM é aberto em um editor de texto, ele exibe um código que consiste em tags e scripts que ninguém entenderia a menos que fosse um desenvolvedor web.

## Exemplo de uso do CFM ##

O seguinte mostra um arquivo CFM de exemplo de uso simples.

### Documento CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## Referências ##

- [CFM - Wikipedia](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

