{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CONFIG - Configuration File",
  "description":"Learn about CONFIG file format with CONFIG example and APIs that can create and open CONFIG files.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-04-23"
}

## What is a CONFIG file?
A CONFIG file is known as configuration file; used to configure the parameters and primary settings for several computer softwares. Some softwares only read their **configuration files** at their startup. Others check the configuration files for changes periodically.

## CONFIG File format
The **CONFIG File format** is used for server processes, software applications, and operating system settings. A programmer can write code to instruct a software to read the configuration files again and again after certain time of period and apply the changes to the current process. There are no definitive standards or strong conventions for CONFIG file sysntax. For example, Microsoft's Web.config file belongs to the CONFIG file format, which consists of an [XML](/web/xml/) based tagsets; can be edited with Microsoft Visual Studio or any other text editor.

## Examples of configuration files:
Since, the configuration files are not created by following any rules, standrads or conventions, these files might have written by using different formats. A .config file might be based on XML, [JSON](/web/json/) or any other format. Following are the examples of configuration files for well known operating systems and softwares:

### Configuration files in Linux
 Every Linux program is an executable file keeping the list of **opcodes** the CPU executes to accomplish typical operations. The operations of almost every program can be customized to your requirements by changing its configuration files. Several configuration files in the Linux system are in the /etc directory. The configuration files can be classified into the following categories:
|Category|Example| Comments|
---|---|---|
|Access files|/etc/host.conf|Tells the network domain server how to look up hostnames.|
|Booting and login/logout|/etc/rc.d/rc.local|Not official. May be called from rc, rc.sysinit, or /etc/inittab.|
|File system|/etc/mtools.conf|Configuration for all the operations (mkdir, copy, format, etc.) on a DOS-type filesystem.|
|System administration|/etc/shells|Holds the list of possible “shells” available to the system.|
|Networking|/etc/gated.conf|Configuration for gated. Used only by the gated daemon.|
|System commands|/etc/logrotate.conf|Configuration for the Dynamic Linker.|
|Daemons|/etc/httpd.conf|The configuration file for Apache, the Web server. This file is typically not in /etc.|
|User programs| /etc/lynx.cfg| Proxy settings|
### AWS CONFIG file example
The frequently used configuration settings and credentials can be saved in CONFIG files that are maintained by the AWS CLI. The CONFIG file must be a plaintext file that uses the following format:
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
### SSH CONFIG file example
OpenSSH client-side configuration file is named CONFIG, and it is stored in the .ssh directory. The SSH CONFIG file consists of the following structure:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG file example
A Python CONFIG file could look like this:

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



## References

 * [Understanding Linux configuration files](https://developer.ibm.com/technologies/linux/articles/l-config/)
 * [Configuration and credential file settings](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
 * [Configuration files in Python](https://martin-thoma.com/configuration-files-in-python/)
