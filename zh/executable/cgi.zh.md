{
  "date" : "2021-06-28",
  "keywords" :["cgi 文件","什么是 cgi 文件","文件","cgi 示例","cgi 文件扩展名","扩展名","格式"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"了解 CGI 文件格式和可以创建和打开 CGI 文件的 API。",
  "title" :"CGI - 通用网关接口脚本文件",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## 什么是一 .cgi 文件？
CGI 文件称为通用网关接口脚本，Web 服务器使用它来运行外部程序来处理用户请求。保存在扩展名为 .cgi 的文件中的脚本通常是用 C 或 Perl 编程语言编写的。早在 Web 开发人员想要将数据库连接到他们的 Web 服务器时，它就已经被引入了。支持 Web 服务器和数据库之间的公共网关的服务器非常适合执行 CGI 代码。

## CGI 文件格式
Web 服务器使用 CGI 脚本来帮助所有者配置 URL 的处理方式。该过程通常通过将一个新目录（文件主要位于该目录）标记为包含 CGI 脚本来完成；它的俗称是cgi-bin。例如，/usr/local/apache/htdocs/cgi-bin 可以被选为 Web 服务器上的 CGI 目录。当 Web 浏览器请求指向 CGI 目录中文件的 URL 时，HTTP服务器执行指定的脚本并将脚本的输出返回给 Web 浏览器。简而言之，CGI 脚本发送到标准输出的任何内容都会被传输到 Web 客户端，而不是显示在窗口的终端中。

### CGI 示例

下面是用 Perl 编写的 CGI 脚本，它显示了 Web 服务器传递的所有环境变量：
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

输出将如下所示：
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## CGI 脚本的使用
包含 CGI 脚本的 CGI 文件通常用于处理来自用户的输入数据并生成相关的输出数据。实现 wiki 是 CGI 程序的示例之一。如果用户代理发送条目名称的请求，Web 服务器将运行 CGI 程序。 CGI 程序获取该条目页面的源，将其转换为 HTML，然后打印结果。 Web 服务器接收来自 CGI 程序的输出并将其返回给用户代理。然后，如果用户代理通过单击“编辑页面"按钮调用编辑函数，CGI 程序会显示一个 HTML 文本区域或其他带有页面内容的编辑控件。最后，如果用户代理单击“发布页面"按钮，CGI 程序会将更新后的 HTML 转换为该条目页面的源并保存。



## 参考

* [通用网关接口 - 维基百科](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

