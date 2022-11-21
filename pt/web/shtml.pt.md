{
  "date" : "2021-05-20",
  "keywords" :[ "shtml", "arquivo shtml", "formato de arquivo shtml", "tipo de arquivo shtml", "arquivo", "tipo", "o que é um arquivo shtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SHTML - Arquivo HTML Incluir Lado do Servidor",
  "description":"Saiba mais sobre o formato de arquivo SHTML e APIs que podem criar e abrir arquivos SHTML.",
  "linktitle" : "SHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-20"
}

## O que é um arquivo SHTML?

Um arquivo com extensão .shtml é uma página da Web escrita em [HTML](/pt/web/html/) e inclui instruções do servidor. Ele também pode conter inclusões do lado do servidor semelhantes aos arquivos ASP para carregamento mais rápido. Os arquivos do lado do servidor também podem conter código executável que pode tornar o servidor mais lento do que o normal. Os arquivos SHTML são semelhantes ao HTML, mas também permitem o uso de comandos simples do servidor. Esses comandos do servidor são executados em uma linguagem de programação de computador simples chamada Server Side Include (SSI). O SHTML foi amplamente substituído por outras linguagens de programação do lado do servidor, como [PHP](/pt/programming/php/) includes.

## Formato de arquivo SHTML

Os arquivos SHTML são escritos em texto simples e usam os [comandos SSI](https://www.w3.org/Jigsaw/Doc/User/SSI.html) que são executados no lado do servidor. Esses comandos do lado do servidor podem ser usados até mesmo para conectar-se ao banco de dados usando os drivers do banco de dados e buscar dados dos usuários das tabelas.

## Exemplo SHTML

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

