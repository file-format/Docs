{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACCESS 文件 - Apache HTACCESS 文件格式",
  "description" :"了解什么是 HTACCESS 文件的文件格式指南",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## 什么是一 HTACCESS 文件？

HTACCESS 文件是一个 Apache 配置文件，它提供了一种允许对网站的不同文件夹/目录进行配置更改的机制。它包括适用于目录和子目录的配置指令。

HTACCESS 文件执行多项检查，例如定义网站的索引页面、列出 404（未找到页面）错误页面、执行 301 或 302 页面重定向、阻止来自特定 IP 地址或其他网站的访问。因此，使用 .htaccess 文件会降低 Apache HTTP 服务器的整体性能。

## HTACCESS 文件格式

HTACCESS 文件以纯文本文件格式存储到光盘。这意味着您可以在任何文本编辑器中打开和编辑这些文件。 “.”前没有名字。在 .htaccess 文件中，显示它是文件夹中的隐藏文件。

## HTACCESS 文件的常见用途

HTACCESS 文件的五种常见用途如下。

### 模组重写

HTACCESS 文件可用于指定和更改网站上的 URL 和网页向用户显示的方式。

＃＃＃ 验证

可以使用 .htaccess 通过创建一个名为 .htpasswd 的密码文件来实现身份验证。如果网站访问者想访问网页的特定部分，这可以让网站访问者提供密码。

### 自定义错误页面

您可以使用 .htaccess 文件创建自定义错误页面，例如 400 错误请求、401 需要授权、403 禁止页面、404 找不到文件和 500 内部错误。但是，这些会降低服务器性能，因为这些所有检查都将在访问页面时执行。

### MIME 类型

可以修改 Apache HTACCESS 文件以包含多用途 Internet 邮件扩展 (MIME) 类型。这使您的服务器能够支持站点不支持的应用程序文件的传送。

### SSI

服务器端包含 (SSI) 可以在网站上节省大量时间。可以通过将以下代码插入 .htaccess 文件来启用 SSI。

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS 文件示例

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## 参考

* [Apache HTTP 服务器教程：.htaccess 文件](https://httpd.apache.org/docs/current/howto/htaccess.html)

