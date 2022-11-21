{
  "date" : "2021-05-20",
  "keywords" :[ "stml", "arquivo stml", "formato de arquivo stml", "tipo de arquivo stml", "arquivo", "tipo", "o que é um arquivo stml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"STML - Arquivo HTML SSI",
  "description":"Saiba mais sobre o formato de arquivo STML e APIs que podem criar e abrir arquivos STML.",
  "linktitle" : "STML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## O que é um arquivo STML?

Um arquivo com extensão .stml é uma página da Web com instruções do lado do servidor que são executadas quando um usuário carrega a página no navegador da Web. As páginas STML contêm código do lado do servidor que contém inclusões do lado do servidor para executar tarefas que não são possíveis de realizar com HTML simples. Embora semelhante ao [HTML](/pt/web/html/), o STML oferece mais poder executando os comandos no servidor, também chamado de Server Side Include (SSI). Com a introdução de novas linguagens de programação com scripts do lado do servidor, como PHP, o uso de STML é reduzido, embora ainda seja suportado por todas as tecnologias do lado do servidor. Os arquivos STML podem ser abertos em qualquer editor de texto e editados para atualização dos comandos.

## Formato de arquivo STML

O STML é baseado no formato de arquivo de texto ASCII simples que é legível por humanos. No entanto, ele segue a sintaxe conforme definido e exercido usando os [comandos SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) que são executados no lado do servidor. Como qualquer outra linguagem de script do lado do servidor, o STML pode usar os comandos do lado do servidor para executar tarefas como contador de visitantes de página, calendário de página da Web, recuperar registros do banco de dados e outros semelhantes.

## Exemplo STML

As instruções do lado do servidor são usadas em aplicativos como para contador de visitantes de página ou calendário de página da web. O exemplo a seguir exibe as primeiras quatro colunas das três primeiras linhas do banco de dados de usuários.

```
<!--#jdbc name="result2" select="SELECT * FROM users"
          user="bmahe" password=""
          url="jdbc:msql://www43.inria.fr:4333/users"
          driver="com.imaginary.sql.msql.MsqlDriver"  -->

      <table border=2>
        <!--#cpt name="cpt1" init="0" -->
          <tr><td><b>Name </td><td><b>Login</td>
              <td><b>Email</td><td><b>Age  </td></tr>
          <!--#loop name="loop2" -->

          <!--#jdbc name="result2" next="true" -->

          <tr>
            <td>
              <!--#jdbc name="result2" column="1" -->
            </td><td>
              <!--#jdbc name="result2" column="2" -->
            </td><td>
              <!--#jdbc name="result2" column="3" -->
            </td><td>
              <!--#jdbc name="result2" column="4" -->
            </td>
          </tr>

          <!--#cpt name="cpt1" incr="1" -->
          <!--#exitloop name="loop2" command="cpt" var="cpt1" equals="3" -->
          <!--#endloop name="loop2" -->

      </table>

      counter value : <!--#cpt name="cpt1" value="true" -->
```
## Referências

* [Server Side Include](https://en.wikipedia.org/wiki/Server_Side_Includes)

