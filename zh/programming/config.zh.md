{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - 配置文件",
  "description":"通过 CONFIG 示例和可以创建和打开 CONFIG 文件的 API 了解 CONFIG 文件格式。",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## 什么是 .config 文件？
CONFIG 文件称为配置文件；用于配置多个计算机软件的参数和初始设置。有些软件只在启动时读取它们的**配置文件**。其他人会定期检查配置文件的更改。

## 配置文件格式
**CONFIG 文件格式** 用于服务器进程、软件应用程序和操作系统设置。程序员可以编写代码来指示软件在一段时间后一次又一次地读取配置文件，并将更改应用于当前进程。 CONFIG 文件的语法没有明确的标准或严格的约定。例如，微软的 Web.config 文件属于 CONFIG 文件格式，它由一个基于 [XML](/web/xml/) 的标签集组成；可以使用 Microsoft Visual Studio 或任何其他文本编辑器进行编辑。

## 配置文件示例：
由于配置文件不是按照任何规则、标准或约定创建的，因此这些文件可能是使用不同格式编写的。 .config 文件可能基于 XML、[JSON](/web/json/) 或任何其他格式。以下是知名操作系统和软件的配置文件示例：

### Linux 中的配置文件
每个 Linux 程序都是一个可执行文件，其中包含 CPU 执行以完成典型操作的 **opcodes** 列表。几乎每个程序的操作都可以通过更改其配置文件来根据您的要求进行定制。 Linux系统中的几个配置文件都在/etc目录下。配置文件可以分为以下几类：
|类别|示例|评论|
---|---|---|
|访问文件|/etc/host.conf|告诉网络域服务器如何查找主机名。|
|引导和登录/注销|/etc/rc.d/rc.local|不是官方的。可以从 rc、rc.sysinit 或 /etc/inittab 调用。|
|文件系统|/etc/mtools.conf|DOS 类型文件系统上所有操作（mkdir、复制、格式化等）的配置。|
|系统管理|/etc/shells|保存系统可用的可能“shell"列表。|
|网络|/etc/gated.conf|门控配置。仅由门控守护程序使用。|
|系统命令|/etc/logrotate.conf|动态链接器的配置。|
|守护进程|/etc/httpd.conf|Apache 的配置文件，Web 服务器。此文件通常不在 /etc 中。|
|用户程序| /etc/lynx.cfg|代理设置|
### AWS CONFIG 文件示例
经常使用的配置设置和凭证可以保存在由 AWS CLI 维护的 CONFIG 文件中。 CONFIG 文件必须是使用以下格式的纯文本文件：
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH CONFIG 文件示例
OpenSSH 客户端配置文件名为 CONFIG，存放在 .ssh 目录下。 SSH CONFIG 文件包含以下结构：
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG 文件示例
Python CONFIG 文件可能如下所示：

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## 参考

* [了解Linux配置文件](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [配置和凭证文件设置](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Python 中的配置文件](https://martin-thoma.com/configuration-files-in-python/)

