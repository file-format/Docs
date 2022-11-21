{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo HTACCESS - Formato de arquivo Apache HTACCESS",
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo HTACCESS",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo HTACCESS?

Um arquivo HTACCESS é um arquivo de configuração do Apache que fornece um mecanismo para permitir alterações de configuração para diferentes pastas/diretórios de um site. Inclui diretivas de configuração aplicáveis ao diretório e subdiretórios.

Um arquivo HTACCESS executa uma série de verificações, como definir a página de índice de um site, listar a página de erro 404 (Página não encontrada), executar os redirecionamentos de página 301 ou 302, bloquear o acesso de um endereço IP específico ou outros sites. O uso de arquivos .htaccess, portanto, diminui o desempenho geral do seu servidor Apache [HTTP](/pt/web/http/).

## Formato de arquivo HTACCESS

Os arquivos HTACCESS são armazenados no disco em formato de arquivo de texto simples. Isso significa que você pode abrir e editar esses arquivos em qualquer editor de texto. Não há nome antes do "." em um arquivo .htaccess, mostrando que é um arquivo oculto dentro da pasta.

## Usos comuns de um arquivo HTACCESS

Cinco usos comuns de um arquivo HTACCESS são os seguintes.

### Mod_Rewrite

Um arquivo HTACCESS pode ser usado para designar e alterar como os URLs e páginas da web em um site são exibidos aos usuários.

### Autenticação

A autenticação pode ser obtida com .htaccess criando um arquivo passowrd chamado .htpasswd. Isso permite que os visitantes do site forneçam uma senha se quiserem visitar uma determinada seção da página da web.

### Páginas de erro personalizadas

Você pode criar páginas de erro personalizadas, como 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File not Found e 500 Internal Error with .htaccess file. No entanto, isso diminuirá o desempenho do servidor, pois todas as verificações serão executadas à medida que as páginas forem acessadas.

### Tipos MIME

Os arquivos Apache HTACCESS podem ser modificados para incluir os tipos MIME (Multipurpose Internet Mail Extensions). Isso permite que seu servidor ofereça suporte à entrega de arquivos de aplicativo que não eram suportados pelo site.

### SSI

Server Side Include (SSI) atua como uma grande economia de tempo em um site. O SSI pode ser habilitado inserindo o seguinte código em seu arquivo .htaccess.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Exemplo de arquivo Apache HTACCESS

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referências

* [Tutorial do Apache HTTP Server: arquivos .htaccess](https://httpd.apache.org/docs/current/howto/htaccess.html)

